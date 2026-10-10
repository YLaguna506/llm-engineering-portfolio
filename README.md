# LLM Engineering Portfolio

My work from [Ed Donner's LLM Engineering course](https://github.com/ed-donner/llm_engineering), organized by week.

The course uses GPT and Claude. I call Gemini, OpenRouter, and a local Ollama server instead,
all through the `openai` Python package. Gemini's OpenAI-compatible endpoint is
`https://generativelanguage.googleapis.com/v1beta/openai/`.

## Week 1

| Notebook | What it does |
| --- | --- |
| [day1-website-summarizer](week1/day1-website-summarizer.ipynb) | Scrape a web page and get a snarky Gemini summary, plus a humorous-psychologist prompt |
| [day2-chat-completions-and-ollama](week1/day2-chat-completions-and-ollama.ipynb) | The Chat Completions API over raw HTTP and through the `openai` client, then the same client on a local Ollama model |
| [day4-tokens-and-memory](week1/day4-tokens-and-memory.ipynb) | Tokenizing with `tiktoken`, and why LLM calls are stateless |
| [day5-company-brochure](week1/day5-company-brochure.ipynb) | Multi-step brochure generator: Gemini picks relevant links (JSON), writes a brochure, translates it to Spanish, and streams |
| [week1-exercise-technical-tutor](week1/week1-exercise-technical-tutor.ipynb) | Technical Q&A tool answered by Gemini (streamed) and Llama 3.2 |

`week1/scraper.py` is the small BeautifulSoup helper the week 1 notebooks import.

## Week 2

| Notebook | What it does |
| --- | --- |
| [day1-three-providers](week2/day1-three-providers.ipynb) | Same prompts on Gemini, Ollama (Llama 3.2 and Qwen 2.5), and OpenRouter; Gemini reasoning effort, token cost, prompt caching on Hamlet, an argumentative chat, and a three-kid conversation |
| [day2-gradio](week2/day2-gradio.ipynb) | Gradio UIs: a text transform, a Gemini chat, a streaming Gemini or Llama selector, and a company brochure generator |

## Tech stack

- Python 3.12, managed with [uv](https://docs.astral.sh/uv/)
- `openai` client library pointed at Gemini, OpenRouter, and a local Ollama server
- `litellm` for Gemini token cost and prompt caching
- `requests` + `beautifulsoup4` for scraping, `tiktoken` for tokenization
- `gradio` for the week 2 chat and brochure interfaces
- Jupyter notebooks

## Setup

1. Install [uv](https://docs.astral.sh/uv/getting-started/installation/), then from the repo root run:

   ```bash
   uv sync
   ```

2. Copy `.env.example` to `.env` and add your `GEMINI_API_KEY` from [Google AI Studio](https://aistudio.google.com/api-keys) and your `OPENROUTER_API_KEY` from [OpenRouter](https://openrouter.ai/keys).
3. For the local-model cells, install [Ollama](https://ollama.com) and run `ollama pull llama3.2` and `ollama pull qwen2.5:3b`.
4. Open a notebook and select the `.venv` kernel in the repo root.

## Repo structure

```text
.
├── week1/
│   ├── scraper.py
│   └── *.ipynb
├── week2/
│   ├── day1-three-providers.ipynb
│   ├── day2-gradio.ipynb
│   ├── hamlet.txt
│   └── scraper.py
├── pyproject.toml
├── uv.lock
└── .env.example
```

Each later week of the course will get its own `weekN/` folder.
