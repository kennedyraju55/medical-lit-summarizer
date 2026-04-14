# 🏥 Medical Literature Summarizer

![Python 3.11+](https://img.shields.io/badge/Python-3.11+-blue?style=flat-square&logo=python&logoColor=white)
![MIT License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)
![Gemma 4](https://img.shields.io/badge/Gemma_4-LLM-orange?style=flat-square&logo=google&logoColor=white)
![Privacy-First](https://img.shields.io/badge/Privacy-100%25_Local-brightgreen?style=flat-square)
![Ollama](https://img.shields.io/badge/Ollama-Inference-blueviolet?style=flat-square)

> AI-powered medical research paper analysis with PICO extraction, evidence grading, and citation generation — running 100% locally.

## Architecture

```
┌──────────────────────────────────────────────┐
│         Medical Paper Input (text)           │
│                    │                          │
│            ┌──────▼───────┐                  │
│            │   Section    │                  │
│            │   Extractor  │                  │
│            └──────┬───────┘                  │
│                   │                          │
│            ┌──────▼───────┐                  │
│            │   Ollama     │                  │
│            │  (Gemma 4)   │                  │
│            └──────┬───────┘                  │
│   ┌───────────────┼───────────────┐          │
│ ┌─▽──────┐ ┌──────▽──────┐ ┌─────▽────┐    │
│ │Summary │ │    PICO     │ │ Evidence │    │
│ │Sections│ │  Extractor  │ │  Grader  │    │
│ └────────┘ └─────────────┘ └──────────┘    │
│                   │                          │
│   ┌───────────────┼───────────────┐          │
│ ┌─▽──────┐ ┌──────▽──────┐ ┌─────▽────┐    │
│ │Citation│ │ Statistics  │ │  Detail  │    │
│ │  APA/  │ │   Results   │ │  Levels  │    │
│ │MLA/etc │ │  Extractor  │ │ Brief/   │    │
│ └────────┘ └─────────────┘ │ Standard │    │
│                              └──────────┘    │
└──────────────────────────────────────────────┘
```

## Features

1. **Section-by-Section Analysis** — Extracts title, abstract, methodology, findings, conclusions, limitations, and future work
2. **PICO Framework Extraction** — Identifies Population, Intervention, Comparison, and Outcome from clinical studies
3. **Evidence Quality Grading** — Rates study design, sample size, methodology rigor, and bias risk using Oxford CEBM levels
4. **Statistical Results Extraction** — Pulls p-values, confidence intervals, effect sizes, and quantitative outcomes
5. **Multi-Style Citations** — Generates formatted citations in APA, MLA, Chicago, and Vancouver styles
6. **Configurable Detail Levels** — Choose brief, standard, or comprehensive summaries for each paper
7. **Rich CLI Interface** — Beautiful terminal output with color-coded sections and structured panels
8. **Streamlit Web UI** — Browser-based dashboard for uploading papers and browsing analysis results
9. **FastAPI REST Endpoint** — Programmatic API for batch paper analysis and integration into research workflows
10. **100% Local & Private** — All inference runs through Ollama locally; sensitive medical research data never leaves your machine

## Quick Start

### Prerequisites

- Python 3.11 or higher
- [Ollama](https://ollama.com/) installed and running
- Gemma 4 model pulled: `ollama pull gemma4`

### Installation

```bash
git clone https://github.com/kennedyraju55/medical-lit-summarizer.git
cd medical-lit-summarizer
pip install -r requirements.txt
```

### Running the Application

**CLI:**
```bash
python -m src.medical_summarizer.cli summarize --file paper.txt --detail standard
```

**Web UI:**
```bash
streamlit run src/medical_summarizer/web_ui.py
```

**Docker:**
```bash
docker-compose up
```

## Tech Stack

| Technology | Purpose |
|-----------|---------|
| Gemma 4 + Ollama | Local LLM inference for paper analysis and evidence grading |
| Click + Rich | CLI framework with structured panels and colored output |
| Streamlit | Interactive web dashboard for paper uploads and analysis |

## Project Structure

- `src/medical_summarizer/` — Core application: section extraction, PICO analysis, evidence grading, CLI, web UI, API
- `common/` — Shared LLM client utilities for Ollama integration
- `tests/` — Unit and integration test suite
- `docs/` — Documentation and architecture diagrams
- `examples/` — Sample medical papers and generated analyses

## Author

**Nrk Raju Guthikonda** — [GitHub: kennedyraju55](https://github.com/kennedyraju55) · [Dev.to](https://dev.to/kennedyraju55) · [LinkedIn](https://www.linkedin.com/in/nrk-raju-guthikonda-504066a8/)
