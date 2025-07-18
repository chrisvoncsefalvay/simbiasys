## FEATURE: Project Structure and Base Configuration

Set up the foundational project directory structure and development environment for Simbiasys, establishing a clean separation between backend API, frontend UI, and supporting resources. Configure the Python environment using uv package manager and establish the base configuration system.

## EXAMPLES:

### Expected Directory Structure:
```
simbiasys/
├── backend/
│   ├── src/
│   │   ├── api/
│   │   ├── models/
│   │   ├── services/
│   │   ├── bias/
│   │   └── llm/
│   ├── tests/
│   └── requirements.txt
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
├── docs/
│   ├── api/
│   └── user-guide/
├── .scratches/
├── .pm/
│   ├── features/
│   ├── PRPs/
│   ├── TODO.md
│   └── ROADMAP.md
├── .vibe/
├── .env.example
├── pyproject.toml
└── README.md
```

### Environment Configuration Example:
```env
# LLM Configuration
LLM_PROVIDER=lmstudio
LMSTUDIO_HOST=127.0.0.1
LMSTUDIO_PORT=1234
OLLAMA_HOST=localhost
OLLAMA_PORT=11434
PHYSICIAN_MODEL=MedGemma
PATIENT_MODEL=Gemma

# API Configuration
API_HOST=0.0.0.0
API_PORT=8096

```

## DOCUMENTATION:

- **uv Documentation**: https://github.com/astral-sh/uv - For Python package management
- **FastAPI Project Structure**: https://fastapi.tiangolo.com/tutorial/bigger-applications/ - Best practices for structuring FastAPI applications
- **Python Project Layout**: https://packaging.python.org/en/latest/tutorials/packaging-projects/ - Standard Python project structure
- **Environment Variables**: https://12factor.net/config - 12-factor app configuration principles

## OTHER CONSIDERATIONS:

1. **Package Manager**: Use `uv` instead of `pip` or `poetry` for all Python dependencies as specified in CLAUDE.md
2. **PyCharm Integration**: Ensure the structure works well with PyCharm's project detection and run configurations
3. **Scratch Directory**: The `.scratches/` directory should be gitignored for temporary files
4. **Cross-Platform**: Ensure paths work on both Windows and Unix-like systems
5. **Configuration Hierarchy**: Support configuration loading from:
   - Environment variables (highest priority)
   - `.env` file
   - `config.yml` or `config.json`
   - Default values in code (lowest priority)
6. **Logging Setup**: Initialize basic file-based logging structure in `logs/` directory
7. **Type Hints**: Ensure all Python files are set up to use type hints from the start
8. **Import Structure**: Set up proper Python import paths using `__init__.py` files
9. **Git Configuration**: Include appropriate `.gitignore` for Python, Node.js, and IDE files
10. **Development vs Production**: Clear separation of development and production configurations
