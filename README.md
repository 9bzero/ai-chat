# ai-chat

Minimal OpenAI-compatible chat interface. Just the conversation.

I built this because I wanted a clean chat UI I could run locally with my own key — no accounts, no data leaving my machine, no features I don't need.

## Features

- Streaming responses (tokens appear as they generate)
- Markdown and code block rendering with syntax highlighting
- Model selector (any model name — it's just a string passed to the API)
- Editable system prompt
- Enter to send, Shift+Enter for newline
- Copy any message

## Setup

```bash
npm install
cp .env.example .env
npm run dev
```

`.env`:
```
VITE_API_KEY=your-key-here
VITE_API_BASE_URL=https://api.openai.com/v1
```

Works with OpenAI, Anthropic (via compatible proxy), Ollama (`http://localhost:11434/v1`), or anything else speaking the OpenAI chat completions API.

## Notes

History lives in memory — no localStorage, no database. Refresh to start fresh.
