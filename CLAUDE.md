# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jupyter Book project for an AI e-book titled "IA em Movimento" (AI in Motion) - a strategic guide for creating AI solutions. The book is written in Portuguese and authored by LAMFO + OtimizAI.

## Build Commands

```bash
# Install dependencies
npm install -g jupyter-book

# Build the book (generates HTML in _build/html/)
jupyter-book build --html

# For Python dependencies (optional, used in legacy workflow)
pip install -r requirements.txt
```

## Project Structure

- **`myst.yml`** - Main configuration file defining the book structure, table of contents, and export settings
- **`capitulos/`** - Book chapters in Markdown format:
  - `capCapa.md` - Cover
  - `capComoUsarEsteEbook.md` - How to use this e-book
  - `capFundamentos_de_IA.md` - AI fundamentals
  - `capArquiteturasTecnologias_ComponentesTecnicos.md` - Technical architectures and components
  - `cap2MCP.md` - MCP (Model Context Protocol) chapter
  - `capEstrategiaConstrucao_e_Operacao.md` - Construction and operation strategies
  - `capEcossistema_Framework.md` - Ecosystem and frameworks
  - `capn8n.md` - n8n automation platform
  - `capRecursosDeApoio.md` - Support resources
  - `Sobre_os_Autores.md` - About the authors
- **`capitulos/references.bib`** - BibTeX bibliography file
- **`imagens/`** - Image assets for the book
- **`chatbot-papers-MCP/`** - Example MCP implementation for the book

## MCP Example Code

The `chatbot-papers-MCP/Servidores/` directory contains a working MCP (Model Context Protocol) server/client example:

- **`mcp_papers_server.py`** - FastMCP server that searches ArXiv papers and analyzes them using Google Gemini
- **`mcp_papers_client.py`** - Interactive client for testing the MCP server

To run the MCP example:
```bash
cd chatbot-papers-MCP/Servidores
pip install -r requirements.txt
# Set GOOGLE_API_KEY in .env file
python mcp_papers_server.py    # Run server
python mcp_papers_client.py    # Run interactive client
```

## Deployment

The book auto-deploys to GitHub Pages on push to `main` via `.github/workflows/deploy.yml`. The workflow:
1. Installs jupyter-book via npm
2. Builds HTML assets
3. Deploys to GitHub Pages

## Content Guidelines

- All content is in Brazilian Portuguese
- Chapters follow MyST Markdown syntax
- Citations reference `capitulos/references.bib`
- Images should be placed in `imagens/` directory
