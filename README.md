# 📄 AnythingLLM Bangla

**Chat with your own documents in Bangla — upload a PDF, ask questions, get answers from your files.**

## ✨ Features

- `docker-compose.bangla.yml` — runs on http://localhost:3001 with storage in `./anythingllm-storage` and telemetry disabled.
- Wired to local Ollama out of the box (`OLLAMA_BASE_URL=http://host.docker.internal:11434`), so no cloud key is needed if Ollama runs on the same machine.
- Multi-user workspaces — keep different document sets separate.

## 🚀 How to use

```bash
# 1. Start Ollama on this machine first (see ollama-bangla)
# 2. Start AnythingLLM
docker compose -f docker-compose.bangla.yml up -d
```

Open http://localhost:3001, create a workspace, upload a PDF or document, pick the Ollama model, and ask questions about your documents in Bangla.

## ⚠️ Honest limits

- The free path needs Ollama running locally — without a model behind it, the app has nothing to answer with.
- Answers come from your uploaded documents plus the model — the model can still misread a document, so check important facts in the source file.
- Large documents take a while to embed on first upload, especially on CPU-only machines.

## 🇧🇩 বাংলা

**এনিথিংএলএলএম বাংলা — নিজের ডকুমেন্ট নিয়ে বাংলায় চ্যাট।**

- PDF বা ডকুমেন্ট আপলোড করুন, বাংলায় প্রশ্ন করুন, ফাইল থেকেই উত্তর পাবেন
- লোকাল Ollama দিয়ে চলে — ক্লাউড key লাগে না
- ডকার দিয়ে এক কমান্ডে চালু হয় — http://localhost:3001

## 📄 License

MIT — use it however you like.
