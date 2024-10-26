# Ollama NextJS Chatbot

## Getting Started

### Run Ollama with the `openhermes` model

You should make sure you have Ollama installed before running this code.

You should install the `openhermes` model by running the following command:

```bash
ollama run openhermes
```

### Run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

If all goes well, you should see something like this:

![](docs/images/screenshot-1.png)

---

## What we use

- [Vercel AI SDK](https://github.com/vercel/ai) - provides React hooks for creating chats (useChat) as well as streams that forward AI responses to the frontend (StreamingTextResponse).
- [ModelFusion](https://github.com/vercel/modelfusion) - a library for building multi-modal AI applications that I've been working on. It provides a streamText function that calls AI models and returns a streaming response. ModelFusion also contains an Ollama integration that we will use to access the OpenHermes 2.5 Mistral model.
- [ModelFusion Vercel AI SDK Integration](https://github.com/vercel/modelfusion/tree/main/packages/%40modelfusion-vercel-ai) - provides a ModelFusionTextStream that adapts ModelFusion's text streaming to the Vercel AI SDK's streaming response.

Should I use ModelFusion? ModelFusion is now part of Vercel and is being merged into Vercel AI SDK, so you can trust it.

---

## Todos

- Add memory support
  - App remembers conversations
- Add support of AWS Bedrock integration