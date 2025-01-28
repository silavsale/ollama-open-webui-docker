# To run Ollama + model + open-webui in Kubernetes namespace AI

# Commands to apply the configuration:

# 1. Create the namespace:

# kubectl apply -f namespace.yaml

# 2. Create the Persistent Volume Claims:

# kubectl apply -f ollama-pvc.yaml

# kubectl apply -f open-webui-pvc.yaml

# 3. Deploy Ollama:

# kubectl apply -f ollama.yaml

# 4. Deploy Open-WebUI:

# kubectl apply -f open-webui.yaml
