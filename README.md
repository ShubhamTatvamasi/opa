# opa

Launch minikube:
```bash
multipass launch minikube --name minikube --cpus 4
```

SSH into minikube:
```bash
multipass shell minikube
```

Add auto complete:
```bash
echo "source <(kubectl completion bash)" >> ~/.bashrc
```

get inside minikube container:
```bash
docker exec -it minikube bash
```
