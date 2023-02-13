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

# deploy Persistent Volumes (PV)
k apply -f deployment/kubernetes-manifests/k8s-with-jaeger/mongo_pv.yml -n tt
# check PV with
k get pvc -n tt

# deploy
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part1.yml

# TODO: update this one
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part2.yml
k apply -n tt -f deployment/kubernetes-manifests/k8s-with-jaeger/ts-deployment-part3.yml


```

9. Observe K8S dashboard, wait for a few minutes
   <img src="https://user-images.githubusercontent.com/24642166/212910066-91919b79-77e4-4b55-b0bd-42e148adae2a.png" width=700>
