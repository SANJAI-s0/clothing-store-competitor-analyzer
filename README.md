# Conversational AI — Clothing Store Competitor Analyzer

A conversational AI pipeline that helps clothing store owners identify nearby competitors, analyze footfall trends and peak hours, and generate structured market intelligence reports.

## Problem Statement

Clothing stores in competitive areas like Koramangala, Bangalore need real-time insights into their local competition. This tool addresses that by combining a Gemini LLM with live web search to deliver competitor analysis and actionable business recommendations through a natural conversational interface.

## Intended Beneficiaries

- **Business Owners & Managers** — Identify key competitors and adjust strategies based on peak traffic data
- **Marketing & Strategy Teams** — Optimize promotions around competitor high-traffic periods
- **Real Estate & Location Analysts** — Assess footfall patterns to recommend store locations
- **Investors & Market Analysts** — Evaluate market saturation and retail potential in target areas

## Features

- Multi-turn conversational interface with persistent chat history
- Real-time competitor discovery via DuckDuckGo search
- Footfall and peak hours analysis for competitor stores
- Structured markdown report generation with executive summary, competitor overview, peak hours analysis, and strategic recommendations
- Auto-saves reports to the `reports/` folder on request

## Tech Stack

- [Gemini 2.5 Flash](https://deepmind.google/technologies/gemini/) — LLM for reasoning and report generation
- [LangChain](https://www.langchain.com/) — Agent framework with tool calling
- [DuckDuckGo Search](https://pypi.org/project/duckduckgo-search/) — Real-time web search (no API key required)
- [python-dotenv](https://pypi.org/project/python-dotenv/) — Environment variable management

## Project Structure

```
Conversational_AI/
├── conversational_ai.py   # Main application
├── requirements.txt       # Python dependencies
├── .env.example           # Environment variable template
├── .env                   # Your API keys (not committed)
└── reports/               # Auto-generated competitor reports
```

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

The generated report covers:
- Executive Summary
- Competitor Overview (stores, malls, key retail hubs)
- Footfall & Peak Hours Analysis
- Strategic Recommendations

Reports are saved to `reports/competitor_report_<location>.md`.

## Environment Variables

| Variable | Description |
|---|---|
| `GEMINI_API_KEY` | Google Gemini API key — get one at [aistudio.google.com](https://aistudio.google.com) |
