# GPU version
Added GPU resource to docker compose to improve performance of the model running in Ollama.

Code added to the Ollama service:
```yaml
    deploy:
      resources:
        reservations:
          devices:
            - driver: nvidia
              capabilities: [gpu]
              count: 1
```