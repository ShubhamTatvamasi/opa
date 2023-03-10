# opa

### Cluster Setup

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

Delete minikube when you are done:
```bash
multipass delete --purge minikube
```

---

### Gatekeeper Setup

https://open-policy-agent.github.io/gatekeeper/website/docs/install

Deploy gatekeeper:
```bash
kubectl apply -f https://raw.githubusercontent.com/open-policy-agent/gatekeeper/master/deploy/gatekeeper.yaml
```

Deploy ConstraintTemplate:
```bash
kubectl apply -f https://raw.githubusercontent.com/open-policy-agent/gatekeeper/master/demo/basic/templates/k8srequiredlabels_template.yaml
```

Check CRDs:
```bash
kubectl get crd
```

Create Constraint:
```bash
kubectl apply -f https://raw.githubusercontent.com/open-policy-agent/gatekeeper/master/demo/basic/constraints/all_ns_must_have_gatekeeper.yaml
```
