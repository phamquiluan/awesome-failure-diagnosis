# How to deploy Tsinghua Train Ticket

Steps:

1. Export env var

```bash
export AWS_PROFILE="aaa"
export INSTANCE_ID="i-001e25e5b4f9f7e51"
export REGION="ap-southeast-2"
```

2. Change instance type

```bash
aws ec2 modify-instance-attribute --instance-id $INSTANCE_ID --region $REGION --instance-type "{\"Value\":\"c5.12xlarge\"}"
```

3. Start instance

```bash
aws ec2 start-instances --instance-ids $INSTANCE_ID --region $REGION
```

4. Watch

```bash
watch -n 1 "aws ec2 describe-instances --region $REGION | jq .Reservations[0].Instances[0].State.Name"
```

5. SSH to the instance

```bash
ssh that@instance_ip
```

6. Clone

```bash
git clone https://github.com/FudanSELab/train-ticket.git && cd train-ticket
```

7. Start a K8s cluster

```bash
 minikube start --cpus=max --memory=max
 minikube addons enable metrics-server

 # start dashboard
 minikube dashboard --url
```

<img src="https://user-images.githubusercontent.com/24642166/212908441-6a3493fd-c34b-49da-a697-c333342a83dd.png" width=700>

8. prepare local registry

```bash
make registry-data
docker run -d --rm -it --name registry -v $PWD/registry-data:/var/lib/registry --network=host alpine ash -c "apk add socat && socat TCP-LISTEN:5000,reuseaddr,fork TCP:$(minikube ip):5000"
```

9. make

```bash
sudo apt install maven
make package
make build-image
make push-image
```

11. Deploy train-ticket system

```bash
# create namespace
k create namespace tt

# deploy pv
k apply -f deployment/kubernetes-manifests/k8s-with-jaeger/mongo_pv.yml -n tt
# check with
k get pvc -n tt

# deploy
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part1.yml
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part2.yml
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part3.yml


```

9. Observe K8S dashboard, wait for a few minutes
   <img src="https://user-images.githubusercontent.com/24642166/212910066-91919b79-77e4-4b55-b0bd-42e148adae2a.png" width=700>
   <img src="https://user-images.githubusercontent.com/24642166/212910351-6344cd3e-40cc-4294-8536-bb88758f95f9.png" width=700>
   <img src="https://user-images.githubusercontent.com/24642166/212911087-6c8d151e-24eb-418c-b51d-0e69d2b7f552.png" width=700>
   <img src="https://user-images.githubusercontent.com/24642166/212911087-6c8d151e-24eb-418c-b51d-0e69d2b7f552.png" width=700>
   <img src="https://user-images.githubusercontent.com/24642166/212925764-6becbc79-131e-4bc8-8dca-e626d1f45663.png" width=700>
