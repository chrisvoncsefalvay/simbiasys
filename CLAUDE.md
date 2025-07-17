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

```bash
# Python virtual environment setup (once established)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies (once requirements.txt exists)
pip install -r backend/requirements.txt

# Run backend server (once implemented)
uvicorn backend.main:app --reload

# Run tests (once test framework is set up)
pytest
```

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
* 
