# opa

Launch minikube:
```bash
multipass launch minikube --name minikube --cpus 4
```

SSH into minikube:
```bash
multipass shell minikube
```

Update `~/.bashrc` file to get auto complete:
```bash
source <(kubectl completion bash)
alias k=kubectl
complete -o default -F __start_kubectl k
```

get inside minikube container:
```bash
docker exec -it minikube bash
```
