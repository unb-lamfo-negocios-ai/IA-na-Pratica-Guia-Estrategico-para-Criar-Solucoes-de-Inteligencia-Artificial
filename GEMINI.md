# GEMINI.md

This file provides context and instructions for Gemini when working with this repository.

## Project Overview

**Title:** IA em Movimento (IA na Prática)
**Description:** A strategic e-book guide for creating Artificial Intelligence solutions, written in Brazilian Portuguese. It covers fundamentals, architectures, strategies, and practical tools like n8n and MCP (Model Context Protocol).
**Authors:** LAMFO + OtimizAI
**Type:** Jupyter Book (Documentation/Static Site)

## Environment & Setup

The project uses both Python and Node.js ecosystems.

### Dependencies
- **Book Build:** Requires `jupyter-book`. Can be installed via pip or npm.
  - Python: `pip install -r requirements.txt` (includes `jupyter-book`, `matplotlib`, `numpy`)
  - Node.js: `npm install -g jupyter-book`
- **MCP Example:** Located in `chatbot-papers-MCP/Servidores/`.
  - Python: `pip install -r chatbot-papers-MCP/Servidores/requirements.txt`

## Build & Run Commands

### Building the Book
To build the HTML version of the book:
```bash
jupyter-book build .
```
The output will be generated in `_build/html/`.

### Running the MCP Example
This project includes a Model Context Protocol (MCP) implementation example.

**Location:** `chatbot-papers-MCP/Servidores/`

1.  **Navigate:** `cd chatbot-papers-MCP/Servidores`
2.  **Install:** `pip install -r requirements.txt`
3.  **Configure:** Ensure `GOOGLE_API_KEY` is set in a `.env` file or environment.
4.  **Run Server:** `python mcp_papers_server.py`
5.  **Run Client:** `python mcp_papers_client.py`

## Directory Structure

- **`.` (Root)**
    - `myst.yml`: Main Jupyter Book configuration (TOC, metadata).
    - `intro.md`: Book landing page.
    - `CLAUDE.md`: Context for Claude AI.
    - `requirements.txt`: Root Python dependencies.
    - `NodeSet.json` & `Templates_n8n.xlsx`: n8n workflow resources.

- **`capitulos/`**: Content chapters (MyST Markdown).
    - `capCapa.md`: Cover.
    - `capComoUsarEsteEbook.md`: Usage guide.
    - `capFundamentos_de_IA.md`: AI Fundamentals.
    - `capArquiteturasTecnologias_ComponentesTecnicos.md`: Architecture & Tech.
    - `cap2MCP.md`: Model Context Protocol details.
    - `capEstrategiaConstrucao_e_Operacao.md`: Strategy.
    - `capEcossistema_Framework.md`: Tools & Frameworks.
    - `capn8n.md`: n8n automation.
    - `references.bib`: Bibliography.

- **`imagens/`**: Static assets (images, diagrams) used in the book.

- **`chatbot-papers-MCP/`**: Code examples for the MCP chapter.

## Conventions

- **Language:** All content must be in **Brazilian Portuguese**.
- **Format:** Use **MyST Markdown** (Markedly Structured Text) for chapters.
    - Use directives like `:::{note}`, `:::{tip}`, `:::{admonition}` for callouts.
- **Citations:** Use `references.bib` for academic citations.
- **Images:** Store all images in `imagens/` and reference them relatively.
