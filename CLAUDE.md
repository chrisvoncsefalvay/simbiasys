## Project Conventions

- **British English**: No em dashes, no Oxford commas
- **Python Style**: Well-written, idiomatic Python
- **Headings**: Use title case, do not capitalise every word
- **Run Configurations**: Create PyCharm run configurations for all scripts
- **Package Manager**: Use uv for running scripts, not python directly
- **Data Access**: For Huggingface, use the `datasets` library (don't download)
- **Scratch Files**: All temporary files go in `.scratches/` directory
- **Feature Outlines**: Always prefix with `FEAT_` and place in `.pm/features/`
- **PRPs**: go into `.pm/PRPs/`
- **Todo list**: is in `.pm/TODO.md`.
- **Project roadmap**: is in `ROADMAP.md`.
- **No unicode or emojis**: no unicode or emojis in anything that goes into the 

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is Simbiasys, a web application that simulates and examines the effects of biases in healthcare interactions, particularly focusing on homophily effects similar to Schelling's model of segregation.

The project simulates physician-patient interactions around test result interpretation, measuring how various biases affect patient understanding of medical information.

**Project Name**: Simbiasys

## Key Architecture

- **Backend**: Python with FastAPI
- **Frontend**: React/Vue/Svelte
- **LLM Integration**: LMStudio or Ollama
- **Simulation Engine**: Bias injection system, conversation orchestrator, and adjudicator for ground truth assessment

## Development Commands

Since this is a new project, commands will be established as features are implemented:

## Project Conventions

- **British English**: No em dashes, no Oxford commas
- **Python Style**: Well-written, idiomatic Python
- **Headings**: Use title case, do not capitalise every word
- **Run Configurations**: Create PyCharm run configurations for all scripts
- **Package Manager**: Use uv for running scripts, not python directly
- **Data Access**: For Huggingface, use the `datasets` library (don't download)
- **Scratch Files**: All temporary files go in `.scratches/` directory
- **Feature Outlines**: Always prefix with `FEAT_` and place in `.scratches/`


## Bias Types to Implement

**Patient Biases:**
- Self-diagnosis confirmation
- Gender (trust/distrust)
- Ethnicity (positive/negative)
- Medical system bias
- Recency/availability

**Physician Biases:**
- Recency, false consensus, frequency, status quo, confirmation
- Gender bias
- Ethnicity bias
- Education bias

## Key Technical Considerations

### LLM integration

* Ollama or LMStudio
* Ollama - via Python package
* LMStudio - via API
* Allow LLM provider to be set by env var, as well as host and port
* Serve API on port 8096, web frontend on standard ports.

### Web development

Use the browsermcp MCP server to verify changes to the frontend. 

### Aesthetics

Use for inspiration:

* https://ui.shadcn.com/themes#themes

### Logging

Frontend and backend should log extensively. Initially just log to files but provide for logging to ELK stack or Sentry later.

### Language models

For now we'll set doctor and patient models as environment variables but we'll eventually set them in the frontend.

### MCP servers

* use browsermcp for browser access
* use context7 for documentation

## Key Libraries and Tools

### Backend
- **FastAPI**: Web framework for building the API (port 8096)
- **uv**: Package manager for Python dependencies
- **OpenAI Python client**: For LMStudio/Ollama API integration
- **Jinja2**: Template engine for prompt generation
- **SQLite/PostgreSQL**: Database for simulation persistence
- **Redis**: Caching layer for LLM responses
- **WebSockets**: Real-time communication with frontend
- **Pydantic**: Data validation and models
- **python-dotenv**: Environment variable management

### LLM Integration
- **LMStudio**: Local LLM server (OpenAI-compatible API)
- **Ollama**: Alternative local LLM server (Python package)
- **MedGemma**: Model for physician simulation
- **Gemma**: Model for patient simulation

### Frontend
- **React/Vue/Svelte**: Modern web framework (TBD)
- **TypeScript**: Type safety for frontend
- **shadcn/ui**: UI component library
- **Chart.js/D3.js**: Data visualisation
- **WebSocket client**: Real-time updates
- **Redux/Vuex/Stores**: State management

### Testing & Development
- **pytest**: Python testing framework
- **PyCharm**: IDE with run configurations
- **Git**: Version control
- **Docker**: Containerisation

### Logging & Monitoring
- **Python logging**: Initial file-based logging
- **ELK Stack**: Future log aggregation
- **Sentry**: Future error tracking
