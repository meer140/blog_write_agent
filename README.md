# Technical Blog Studio

A Python-based AI application that helps generate technical blog posts from a single topic.

## Overview

Technical Blog Studio combines a Streamlit frontend with a LangGraph backend to:

- decide whether web research is needed
- collect relevant evidence from the web
- build a structured blog outline
- write each section in Markdown
- assemble a final technical article for download

## Features

- Topic-driven blog generation
- Optional web research for current or fast-changing topics
- Structured planning with tasks, goals, and target word counts
- Markdown section generation using LLMs
- Final article assembly in a single output file
- Simple web UI for generating and downloading content

## Project Structure

- `frontend.py` — Streamlit interface
- `backend.py` — LangGraph workflow for planning, research, writing, and reduction
- `requirements.txt` — Python dependencies

## Requirements

- Python 3.10+
- Google API key for Gemini
- Tavily API key for research

## Setup

1. Clone the repository.
2. Create and activate a virtual environment.
3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root with:

```env
GOOGLE_API_KEY=your_google_api_key
TAVILY_API_KEY=your_tavily_api_key
```

## Run the app

```bash
streamlit run frontend.py
```

Then open the local URL shown in the terminal in your browser.

## How it works

The app uses a LangGraph pipeline:

1. Route the topic to determine whether research is required.
2. Search the web if needed.
3. Create a blog outline and section plan.
4. Generate each blog section individually.
5. Combine all sections into the final Markdown article.

## Notes

This project is intended for experimentation and content generation workflows. The output quality depends on the model and the quality of the input topic.

## License

This project is provided as-is for educational and personal use.
