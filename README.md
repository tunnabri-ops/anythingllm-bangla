# AnythingLLM Bangla — নিজের ডকুমেন্ট নিয়ে বাংলায় চ্যাট

Bangla-ready self-hosted AnythingLLM setup, built on **Mintplex-Labs/anything-llm**.

- **Original repo:** https://github.com/Mintplex-Labs/anything-llm (stop renting your intelligence — local-first AI agent: chat with your documents, multi-user, workspaces)

## কী আছে / What is inside

- `docker-compose.bangla.yml` — runs AnythingLLM on http://localhost:3001 with storage in `./anythingllm-storage`, telemetry off, and Ollama wired in as the local LLM (`OLLAMA_BASE_URL=http://host.docker.internal:11434`).

## যা ঠিক করা হয়েছে / What was fixed

- Upstream's Docker setup needs several manual choices (storage location, LLM provider, telemetry). This compose file pins the working combination: image `mintplexlabs/anythingllm:latest` (verified on Docker Hub, 5.2M+ pulls), local Ollama as the free LLM, telemetry disabled.
- The upstream README's own default is a cloud LLM key. Here no key is needed if Ollama runs locally — see the `ollama-bangla` repo for the Bangla model.

## ব্যবহার / How to use

```bash
# 1. Start Ollama on this machine first (ollama-bangla)
# 2. Start AnythingLLM
docker compose -f docker-compose.bangla.yml up -d
```

Open http://localhost:3001, create a workspace, upload a PDF/document, pick the Ollama model, and ask questions about your documents in Bangla.
