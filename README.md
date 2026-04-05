<div align="center">
<img src="https://img.shields.io/badge/🏥_Medical_Literature_Summarizer-Local_LLM_Powered-blue?style=for-the-badge&labelColor=1a1a2e&color=16213e" alt="Project Banner" width="600"/>

<br/>

<img src="https://img.shields.io/badge/Gemma_4-Ollama-orange?style=flat-square&logo=google&logoColor=white" alt="Gemma 4"/>
<img src="https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Streamlit-Web_UI-red?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit"/>
<img src="https://img.shields.io/badge/Click-CLI-green?style=flat-square&logo=gnu-bash&logoColor=white" alt="Click CLI"/>
<img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="License"/>

<br/><br/>

<strong>Part of <a href="https://github.com/kennedyraju55/90-local-llm-projects">90 Local LLM Projects</a> collection</strong>

</div>

<br/>
# 🔬 Medical Literature Summarizer

![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)
![LLM](https://img.shields.io/badge/LLM-Gemma%204-orange)
![Ollama](https://img.shields.io/badge/Ollama-Local-green)
![Streamlit](https://img.shields.io/badge/UI-Streamlit-red?logo=streamlit)
![License](https://img.shields.io/badge/License-MIT-yellow)

Production-grade medical literature analyzer with PICO framework extraction, evidence quality rating, citation formatting, and structured paper summarization.

## ✨ Features

- **Structured Extraction** — Title/authors, abstract, methodology, findings, statistics, conclusions, limitations, future work
- **PICO Framework** — Population, Intervention, Comparison, Outcome extraction
- **Evidence Quality Rating** — Study design, sample size, methodology rigor, bias risk assessment
- **Citation Formatter** — APA, MLA, Chicago, Vancouver citation styles
- **Adjustable Detail** — Brief, standard, or comprehensive summaries
- **Dual Interface** — CLI + Streamlit Web UI
- **Local & Private** — All processing via local Ollama

## 🚀 Installation

```bash
cd 14-medical-lit-summarizer
pip install -r requirements.txt
ollama serve && ollama pull gemma4
```

## 📋 CLI Usage

```bash
# Summarize a paper
python -m src.medical_summarizer.cli summarize --paper research.txt --detail standard

# PICO framework extraction
python -m src.medical_summarizer.cli pico --paper research.txt

# Evidence quality rating
python -m src.medical_summarizer.cli evidence --paper research.txt

# Format citation
python -m src.medical_summarizer.cli cite --paper research.txt --style APA
```

## 🌐 Web UI (Streamlit)

```bash
streamlit run src/medical_summarizer/web_ui.py
```

Features: Paper upload, structured summary, evidence table, PICO extraction, formatted citations.

## 🧪 Running Tests

```bash
python -m pytest tests/ -v
```

## 📁 Project Structure

```
14-medical-lit-summarizer/
├── src/medical_summarizer/
│   ├── __init__.py, core.py, cli.py, web_ui.py, config.py, utils.py
├── tests/
│   ├── __init__.py, test_core.py, test_cli.py
├── config.yaml, setup.py, requirements.txt, Makefile, .env.example, README.md
```

## Part of

[90 Local LLM Projects](../README.md) — A collection of projects powered by local language models.

## 📸 Screenshots

<div align="center">
<table>
<tr>
<td><img src="https://via.placeholder.com/400x250/1a1a2e/e94560?text=CLI+Interface" alt="CLI Interface"/></td>
<td><img src="https://via.placeholder.com/400x250/16213e/e94560?text=Web+UI" alt="Web UI"/></td>
</tr>
<tr>
<td align="center"><em>CLI Interface</em></td>
<td align="center"><em>Streamlit Web UI</em></td>
</tr>
</table>
</div>
