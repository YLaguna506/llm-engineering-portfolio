# LLM Engineering Portfolio

My own work from [Ed Donner's LLM Engineering course](https://github.com/ed-donner/llm_engineering).

This repo is **not** a copy of the course. Labs stay in a local clone of the course. Finished notebooks that I want to share go here, organized by week.

## Week 1

| Notebook | What it does |
| --- | --- |
| [day1-website-summarizer.ipynb](week1/day1-website-summarizer.ipynb) | Fetch a web page and summarize it with an LLM |
| [day2-open-source-models.ipynb](week1/day2-open-source-models.ipynb) | Same idea with local / open-source models (Ollama) |
| [day4-tokenizing.ipynb](week1/day4-tokenizing.ipynb) | Tokenize text with tiktoken |
| [day5-company-brochure.ipynb](week1/day5-company-brochure.ipynb) | Generate a company brochure from a website |
| [exercise-technical-tutor.ipynb](week1/exercise-technical-tutor.ipynb) | End-of-week exercise: technical Q&A with Gemini (streaming) and Llama 3.2 via Ollama |

## Setup

1. Use the course environment from the original repo (Python, `uv`, Jupyter).
2. Copy `.env.example` to `.env` and add your API keys.
3. For the Ollama cells, run Ollama locally (`ollama run llama3.2`).

## Notes

- API keys are loaded from `.env`. They are not stored in this repo.
- Course materials, solutions, and community contributions stay in the local course clone.
