# How to prepare a minikube cluster on EC2

## 1. Export env var

```bash
export AWS_PROFILE="aaa"
```

## 2. Change instance type

```bash
aws ec2 modify-instance-attribute --instance-id i-001e25e5b4f9f7e51 --region ap-southeast-2 --instance-type "{\"Value\":\"c5.12xlarge\"}"
```

## 3. Start instance

```bash
aws ec2 start-instances --instance-ids i-001e25e5b4f9f7e51 --region ap-southeast-2
```

## 4. Watch

```bash
watch -n 1 "aws ec2 describe-instances --region ap-southeast-2 | jq .Reservations[0].Instances[0].State.Name"
```

## 5. SSH to the instance

```bash
ssh that@instance_ip
```

## 6. Start a K8s cluster

```bash
# restart_minikube.sh
minikube delete
minikube start --cpus=max --memory=max
minikube addons enable dashboard
minikube addons enable registry
minikube addons enable metrics-server
minikube dashboard --port 39563 --url
```
