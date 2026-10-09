# LLM Engineering Portfolio

My work from [Ed Donner's LLM Engineering course](https://github.com/ed-donner/llm_engineering), organized by week.

The course uses GPT; I use Gemini instead, called through the `openai` Python package via Gemini's
OpenAI-compatible endpoint (`https://generativelanguage.googleapis.com/v1beta/openai/`).

## Week 1

| Notebook | What it does |
| --- | --- |
| [day1-website-summarizer](week1/day1-website-summarizer.ipynb) | Scrape a web page and get a snarky Gemini summary, plus a humorous-psychologist prompt |
| [day2-chat-completions-and-ollama](week1/day2-chat-completions-and-ollama.ipynb) | The Chat Completions API over raw HTTP and through the `openai` client, then the same client on a local Ollama model |
| [day4-tokens-and-memory](week1/day4-tokens-and-memory.ipynb) | Tokenizing with `tiktoken`, and why LLM calls are stateless |
| [day5-company-brochure](week1/day5-company-brochure.ipynb) | Multi-step brochure generator: Gemini picks relevant links (JSON), writes a brochure, translates it to Spanish, and streams |
| [week1-exercise-technical-tutor](week1/week1-exercise-technical-tutor.ipynb) | Technical Q&A tool answered by Gemini (streamed) and Llama 3.2 |

`week1/scraper.py` is the small BeautifulSoup helper the notebooks import.

## Setup

1. Python 3.12 with `openai`, `python-dotenv`, `requests`, `beautifulsoup4`, `tiktoken`, `ipython`.
2. Copy `.env.example` to `.env` and add `GEMINI_API_KEY` (from [Google AI Studio](https://aistudio.google.com/api-keys)).
3. For the local-model cells, install [Ollama](https://ollama.com) and run `ollama pull llama3.2`.
