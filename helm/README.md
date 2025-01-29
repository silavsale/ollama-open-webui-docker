1. Add Helm Repositories

```sh
helm repo add ollama-helm https://otwld.github.io/ollama-helm/
helm repo add open-webui https://helm.openwebui.com/
helm repo update

```

2. kubectl create namespace ollama

```sh
kubectl create namespace ollama
```

kubectl apply -f ollama/ollama-pvc.yaml

kubectl apply -f ollama/ollama-deployment.yaml
kubectl apply -f ollama/ollama-service.yaml
kubectl apply -f ollama/ollama-nodeport.yaml

kubectl apply -f open-webui/open-webui-deployment.yaml
kubectl apply -f open-webui/open-webui-service.yaml
kubectl apply -f open-webui/open-webui-nodeport.yaml

kubectl apply -f ingress/ingress.yaml

### To restart:

kubectl rollout restart deployment ollama -n ollama
