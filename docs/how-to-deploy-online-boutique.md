# How to deploy online boutique

Github: https://github.com/GoogleCloudPlatform/microservices-demo

<img src="https://user-images.githubusercontent.com/24642166/213623458-1f140b52-d364-46cd-8e28-430305619226.png" width=700>

**TODOLIST:**

- [ ] Try this: Enable GCP APIs for Cloud Monitoring, Tracing, Profiler
- [ ] How to do fault injection
- [ ] Add reference papers

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

## Clone

```bash
git clone https://github.com/GoogleCloudPlatform/microservices-demo && cd microservices-demo

# git checkout 58b6cd21c3f050d064598575d3df6c525a7ceaea
```

## Start a K8s cluster

```bash
 minikube start --cpus=max --memory=max
 minikube addons enable metrics-server

 # start dashboard
 minikube dashboard --port 30001 --url
```

```bash
# verify your cluster
kubectl get nodes
```

## Deploy the online boutique system

```bash
# first time will be slow, it can take ~20 minutes). This will build and deploy the application.
skaffold run
```

If you need to rebuild the images automatically as you refactor the code.

```bash
skaffold dev
```

## Observe K8S dashboard, wait for a few minutes

<img src="https://user-images.githubusercontent.com/24642166/213350396-553b812e-b6f6-49c0-96c7-94e7af03df9a.png" width=700>

## Forward frontend port and access the website

```bash
kubectl port-forward deployment/frontend 8080:8080
```

## Clean up

```bash
skaffold delete
```

## Papers

- ASE'22 - Graph based Incident Extraction and Diagnosis in Large-Scale Online Systems
- WWW'21 - MicroRank: End-to-End Latency Issue Localization with Extended Spectrum Analysis in Microservice Environments, https://github.com/yuxiaoba/Hipster-Shop
- IWQOS'21 - TraceRCA: Practical root cause localization for microservice systems via trace analysis
