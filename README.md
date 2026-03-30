# Conversational AI — Clothing Store Competitor Analyzer

A conversational AI pipeline that helps clothing store owners monitor nearby competitors, analyze footfall trends, and generate actionable market intelligence reports.

## Features

- Multi-turn conversational interface with memory
- Real-time competitor discovery via DuckDuckGo search
- Footfall and peak hours analysis for competitor stores
- Auto-saves structured markdown reports on request

## Setup

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Copy `.env.example` to `.env` and add your Gemini API key:
   ```bash
   cp .env.example .env
   ```

3. Run the assistant:
   ```bash
   python conversational_ai.py
   ```

## Example Usage

```
You: What clothing stores are near Koramangala, Bangalore?
You: What are the busiest hours for those stores?
You: Generate a competitor report for Koramangala
```

Reports are saved to the `reports/` folder as markdown files.

## Environment Variables

| Variable | Description |
|---|---|
| `GEMINI_API_KEY` | Google Gemini API key |
