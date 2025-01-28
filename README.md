1. Run Ollama - CPU only. Docs - https://hub.docker.com/r/ollama/ollama

```sh
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

2.  Access and interact with a running Docker container

```sh
docker exec -it ollama /bin/bash
```

3.  Run model inside of ollama container

```sh
ollama run deepseek-r1:1.5b
```

3.1 List of models - https://ollama.com/search

4.  Run open webui in Docker container on port 3000

````sh
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

4.1  Open-webui  docs - https://github.com/open-webui/open-webui

````
