# OPA

https://play.openpolicyagent.org/

Add OPA Gatekeeper Helm Repo:
```bash
helm repo add gatekeeper https://open-policy-agent.github.io/gatekeeper/charts
```

Install OPA Gatekeeper:
```bash
helm upgrade -i gatekeeper gatekeeper/gatekeeper \
  --version 3.22.2 \
  --namespace gatekeeper-system \
  --create-namespace \
  --set replicas=1
```

 
