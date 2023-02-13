# How to deploy Tsinghua Train Ticket

## 1. Prepare Minikube Cluster

Follow [this tutorial](./how-to-prepare-a-minikube-cluster-on-ec2.md)

## 2. SSH to the instance

```bash
ssh that@instance_ip
```

## 3. Clone Tsinghua Train Ticket code

```bash
git clone https://github.com/phamquiluan/tsinghua-train-ticket.git && cd tsinghua-train-ticket
```

## 3. Prepare a local Docker registry

```bash
mkdir registry-data
docker run -d --rm -it --name registry -v $PWD/registry-data:/var/lib/registry --network=host alpine ash -c "apk add socat && socat TCP-LISTEN:5000,reuseaddr,fork TCP:$(minikube ip):5000"
```

## 4. Build package, docker and push into the local registry

```bash
sudo apt install maven
make package
make build-image
make push-image
```

## 5. Deploy train-ticket system

```bash
# create namespace
k create namespace tt
```

Forward remote port 39563 to local machine and open the dashboard here: http://127.0.0.1:39563/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/workloads?namespace=tt

```bash
# deploy Persistent Volumes (PV)
k apply -f deployment/kubernetes-manifests/k8s-with-jaeger/mongo_pv.yml -n tt
# check PV with
k get pvc -n tt

# deploy part 1
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part1.yml
```

<img src="https://user-images.githubusercontent.com/24642166/218472867-7269227d-aed6-4fcd-b7d1-f6125ef8da37.png" width=700>

```bash
# deploy part 2
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part2.yml
```

<img src="https://user-images.githubusercontent.com/24642166/218474004-ac22d615-a6e5-4558-b816-a02124a95578.png" width=700>

```bash
# deploy part 3, ts-ui-dashboard
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part3.yml

# expose the service
minikube service ts-ui-dashboard -n tt --url

# (ins)(env) ubuntu@ip-172-31-27-139:~/tsinghua-train-ticket$ minikube service ts-ui-dashboard -n tt --url
# http://192.168.49.2:32677
```

9. Forward and open the url

<img src="https://user-images.githubusercontent.com/24642166/218474593-0eb08cab-29ee-4714-a2a9-9e56f1e9837b.png" width=700>
