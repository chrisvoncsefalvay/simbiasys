# Simbiasys Todo List

## Phase 1: Foundation

### Core Architecture
- [ ] **ARCH-001**: Create project directory structure with src/, tests/, docs/, frontend/, backend/. Set up environment using uv.
- [ ] **ARCH-002**: Define Patient, Physician, TestResult, MedicalHistory data models with type hints
- [ ] **ARCH-003**: Implement BiasProfile class with bias types and strength parameters
- [ ] **ARCH-004**: Create Interaction class to store conversation history and metadata
- [ ] **ARCH-005**: Set up configuration management using environment variables and config files

### LLM Integration
- [ ] **LLM-001**: Create abstract base class for LLM interface with standard methods
- [ ] **LLM-002**: Implement LMStudio connector with OpenAI-compatible API client
- [ ] **LLM-003**: Build model manager to handle MedGemma (physician) and Gemma (patient) instances
- [ ] **LLM-004**: Create Jinja2-based prompt templating system with bias injection points
- [ ] **LLM-005**: Implement exponential backoff retry logic and error handling

## Phase 2: Bias and Simulation Engine

### Bias System
- [ ] **BIAS-001**: Define bias taxonomy with patient biases (self-diagnosis, gender, ethnicity, medical system, recency)
- [ ] **BIAS-002**: Define physician biases (recency, false consensus, frequency, status quo, confirmation, gender, ethnicity, education)
- [ ] **BIAS-003**: Implement bias strength mapping from Likert scale (1-5) to prompt modifiers
- [ ] **BIAS-004**: Create homophily calculator to measure similarity between patient and physician
- [ ] **BIAS-005**: Build prompt injection system to apply biases to conversation prompts

### Character Generation
- [ ] **CHAR-001**: Create demographic generator for sex, age, education, socioeconomic status
- [ ] **CHAR-002**: Build personality profiler that incorporates bias settings into character traits
- [ ] **CHAR-003**: Implement medical knowledge level simulator based on education and background
- [ ] **CHAR-004**: Create background story generator for realistic character contexts

### Adjudicator System
- [ ] **ADJ-001**: Implement ground truth determination using neutral LLM analysis
- [ ] **ADJ-002**: Create metrics for assessing patient understanding accuracy
- [ ] **ADJ-003**: Build semantic similarity evaluator using embeddings
- [ ] **ADJ-004**: Design scoring system (0-100) for patient comprehension levels
- [ ] **ADJ-005**: Create annotation system to mark each conversation turn with understanding scores

## Phase 3: Interaction Simulation

### Conversation Engine
- [ ] **CONV-001**: Implement turn-taking mechanism with physician-patient alternation
- [ ] **CONV-002**: Build context manager to maintain conversation history between turns
- [ ] **CONV-003**: Create conversation flow controller with state machine
- [ ] **CONV-004**: Define termination conditions (max turns, understanding threshold, natural end)
- [ ] **CONV-005**: Implement state persistence for resumable simulations

### Understanding Tracker
- [ ] **TRACK-001**: Build patient understanding extractor from conversation responses
- [ ] **TRACK-002**: Create comprehension evolution tracker across conversation turns
- [ ] **TRACK-003**: Implement divergence measurement from ground truth
- [ ] **TRACK-004**: Prepare data structures for frontend visualisation

## Phase 4: Frontend Development

### Frontend Setup
- [ ] **FE-001**: Set up React/Vue/Svelte project with TypeScript
- [ ] **FE-002**: Create responsive layout with shadcn/ui components
- [ ] **FE-003**: Implement WebSocket client for real-time simulation updates
- [ ] **FE-004**: Design component architecture with reusable UI elements
- [ ] **FE-005**: Set up Redux/Vuex/Svelte stores for state management

### User Interface Components
- [ ] **UI-001**: Build conversation display with message bubbles and annotations
- [ ] **UI-002**: Create character profile cards showing demographics and biases
- [ ] **UI-003**: Implement bias configuration sliders with Likert scale UI
- [ ] **UI-004**: Design test result input form with common medical tests
- [ ] **UI-005**: Build medical history configuration panel

### Simulation Controls
- [ ] **CTRL-001**: Create simulation parameter controls (turn limit, models, etc.)
- [ ] **CTRL-002**: Implement play/pause/reset buttons for simulation control
- [ ] **CTRL-003**: Build turn-by-turn navigation with replay capability
- [ ] **CTRL-004**: Design JSON/CSV export for simulation results
- [ ] **CTRL-005**: Create preset scenario selector with common bias configurations

### Analytics Dashboard
- [ ] **DASH-001**: Build bias-comprehension correlation chart using Chart.js/D3
- [ ] **DASH-002**: Create line chart for understanding progression over turns
- [ ] **DASH-003**: Implement homophily effect visualisation with scatter plot
- [ ] **DASH-004**: Build comparative analysis view for multiple simulations
- [ ] **DASH-005**: Create PDF report generation with simulation summary

## Phase 5: Integration

### Backend API
- [ ] **API-001**: Create FastAPI application with simulation endpoints
- [ ] **API-002**: Implement WebSocket server for real-time updates
- [ ] **API-003**: Build SQLite/PostgreSQL persistence for simulation data
- [ ] **API-004**: Design simulation history API with search and filter
- [ ] **API-005**: Create import/export endpoints for simulation configurations

### Testing Suite
- [ ] **TEST-001**: Write unit tests for bias calculation functions
- [ ] **TEST-002**: Create integration tests for LLM API interactions
- [ ] **TEST-003**: Build end-to-end tests for complete simulation flow
- [ ] **TEST-004**: Design validation suite for bias effect measurement
- [ ] **TEST-005**: Implement performance benchmarks for response times

## Phase 6: Enhancement and Polish

### Advanced Features
- [ ] **ADV-001**: Implement batch simulation runner for multiple scenarios
- [ ] **ADV-002**: Create A/B testing framework for bias interventions
- [ ] **ADV-003**: Build bias mitigation simulator with suggested improvements
- [ ] **ADV-004**: Create recommendation engine for optimal physician-patient matching
- [ ] **ADV-005**: Design educational mode with bias awareness training

### Performance and Deployment
- [ ] **OPT-001**: Implement Redis caching for LLM responses
- [ ] **OPT-002**: Add React.memo/computed for frontend optimisation
- [ ] **OPT-003**: Implement lazy loading for dashboard components
- [ ] **OPT-004**: Set up logging to ELK stack or files
- [ ] **OPT-005**: Create Docker containers and deployment scripts

## Priority Order
1. Start with Phase 1 (Foundation) - ARCH and LLM tasks
2. Move to Phase 2 (Bias System) - Core simulation logic
3. Implement Phase 3 (Interaction) - Get basic simulation working
4. Build Phase 4 (Frontend) - Make it usable
5. Complete Phase 5 (Integration) - Make it robust
6. Enhance with Phase 6 - Polish and advanced features