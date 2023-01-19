# How to deploy Sock Shop

- Homepage: https://microservices-demo.github.io/
- Github: https://github.com/phamquiluan/sock-shop

<img src="https://user-images.githubusercontent.com/24642166/213437581-873841e2-826e-4b70-889b-99148aeb8725.png" width=700/>

## Prepare an EC2 Instance

<details>
  <summary>Expand me</summary>
  
### Export env var
```bash
export AWS_PROFILE="aaa"
export INSTANCE_ID="i-001e25e5b4f9f7e51"
export REGION="ap-southeast-2"
```

### Change instance type

```bash
aws ec2 modify-instance-attribute --instance-id $INSTANCE_ID --region $REGION --instance-type "{\"Value\":\"t2.xlarge\"}"
```

### Start instance

```bash
aws ec2 start-instances --instance-ids $INSTANCE_ID --region $REGION
```

### Watch

```bash
watch -n 1 "aws ec2 describe-instances --region $REGION | jq .Reservations[0].Instances[0].State.Name"
```

### SSH to the instance

```bash
ssh that@instance_ip
```

</details>

## Clone the application repository

```bash
git clone https://github.com/phamquiluan/sock-shop
cd sock-shop
```

## Start a K8s cluster

```bash
minikube start --cpus=max --memory=max
minikube addons enable metrics-server

# start dashboard
minikube dashboard

# verify your cluster
kubectl get nodes
```

## Increase the virtual memory limits

https://www.elastic.co/guide/en/elasticsearch/reference/current/vm-max-map-count.html

```bash
minikube ssh
sudo sysctl -w vm.max_map_count=262144
```

## Start Fluentd + ELK based logging

```bash
kubectl create -f deploy/kubernetes/manifests-logging
```

```bash
# create a tunnel
minikube service kibana -n kube-system
```

<img src="https://user-images.githubusercontent.com/24642166/213435121-5659badc-2de2-433c-8075-103f22a720ff.png" width=700>

## Deploy the Sock Shop system

```bash
kubectl apply -f deploy/kubernetes/manifests/00-sock-shop-ns.yaml -f deploy/kubernetes/manifests
```

## Observe K8S dashboard, wait for a few minutes

<img src="https://user-images.githubusercontent.com/24642166/213435753-e66010fa-35fb-44bd-9981-e2487bc29c68.png" width=700>
<img src="https://user-images.githubusercontent.com/24642166/213436472-f147721c-c538-4819-84aa-82c27cc6a210.png" width=700>

## Create a tunnel for frontend service access the website

```bash
minikube service front-end -n sock-shop
```

<img src="https://user-images.githubusercontent.com/24642166/213437386-ceafaaed-bfab-4d1d-9426-b90a2f21442a.png" width=700/>
<img src="https://user-images.githubusercontent.com/24642166/213437581-873841e2-826e-4b70-889b-99148aeb8725.png" width=700/>

## Clean up

```bash
minikube delete
```
