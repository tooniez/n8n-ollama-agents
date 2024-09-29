# n8n Ollama Agents

**n8n Ollama Agents** a collection of my used credentials and workflows with Ollama.

See [INFO.md](INFO.md) for upstream details.


## 🧩 Components

- **n8n**: Low-code automation platform
- **Ollama**: Cross-platform LLM runner
- **Qdrant**: Vector database for AI applications
- **PostgreSQL**: Relational database for data storage
## 🚀 Connecting to localhost services

When integrating with other services running on your local machine (outside of the Docker network), use the special DNS name `host.docker.internal` instead of `localhost`. This allows containers to communicate with services on your host machine.

For example, if you have a service running on port 3000 on your local machine, you would access it from within a container using:


```shell
http://host.docker.internal
```

## 📜 License

This project is licensed under the Apache License 2.0 - see the
[LICENSE](LICENSE) file for details.
