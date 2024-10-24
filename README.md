# n8n Ollama Agents

**n8n Ollama Agents** a collection of my used credentials and workflows with Ollama.

See [INFO.md](INFO.md) for upstream details.

## 🧩 Components

- **n8n**: Low-code automation platform
- **Ollama**: Cross-platform LLM runner
- **Qdrant**: Vector database for AI applications
- **PostgreSQL**: Relational database for data storage
- **Redis**: In-memory data structure store, used for caching and session management
- **Supabase**: Open-source alternative to Firebase, used for real-time data sync and storage

## 🛠 Project Workflow

1. **Setup**: The Docker Compose file initializes all necessary services.
2. **Data Ingestion**: Use n8n workflows to load data into Qdrant or Supabase.
3. **AI Processing**: Leverage Ollama for local LLM inference within n8n workflows.
4. **Workflow Creation**: Build custom AI agents and RAG systems using n8n's visual editor.
5. **Integration**: Connect your AI workflows with external services and APIs.
6. **Execution**: Run your workflows on-demand or on a schedule within the self-hosted environment.

## 🚀 Connecting to localhost services

When integrating with other services running on your local machine (outside of the Docker network), use the special DNS name `host.docker.internal` instead of `localhost`. This allows containers to communicate with services on your host machine.

For example, if you have a service running on port 3000 on your local machine, you would access it from within a container using:


```shell
http://host.docker.internal
```

## Included Workflows

- Local RAG AI Agent
- Supabase RAG AI Agent
- Base RAG AI Agent
- Demo Agent Workflow
- Qdrant Vector Store Loader
- Supabase Vector Store Loader
- Flux Image Generator
- Company Research Workflow
- Appointment Booking Agent
- LinkedIn Post Automation
- Reddit Trend Analysis
- Hacker News Insights
- News Aggregator
- Notion to LinkedIn Poster
- Siri Ollama Agent

## Getting Started

```shell
docker compose up -d
```

## Backup and Restore

Workflow and Credential backups are stored in `./backups` and can be restored using the `n8n-restore` container.

### Backup

```shell
docker compose up n8n-backup
```

### Restore

```shell
docker compose up n8n-restore
```

## 📜 License

This project is licensed under the Apache License 2.0 - see the
[LICENSE](LICENSE) file for details.
