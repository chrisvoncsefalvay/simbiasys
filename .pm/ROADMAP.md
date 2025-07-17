# Simbiasys Project Roadmap

## Overview
A tool to simulate and examine the effect of biases in healthcare interactions, focusing on homophily effects similar to Schelling's model of segregation.

## Phase 1: Foundation (Weeks 1-3)
### Milestone 1.1: Core Architecture
- **ARCH-001**: Set up project structure and base configuration
- **ARCH-002**: Define core data models (Patient, Physician, TestResult, MedicalHistory)
- **ARCH-003**: Implement BiasProfile and Interaction classes
- **ARCH-004**: Create configuration management system

### Milestone 1.2: LLM Integration
- **LLM-001**: Design abstract LLM interface
- **LLM-002**: Implement LMStudio connector (OpenAI-compatible API)
- **LLM-003**: Build model manager for MedGemma and Gemma
- **LLM-004**: Create prompt templating system
- **LLM-005**: Add error handling and retry logic

## Phase 2: Bias and Simulation Engine (Weeks 4-6)
### Milestone 2.1: Bias System
- **BIAS-001**: Create bias taxonomy with weighted parameters
- **BIAS-002**: Implement bias-to-prompt translation
- **BIAS-003**: Build Likert scale integration
- **BIAS-004**: Design homophily measurement system
- **BIAS-005**: Create prompt injection strategies per bias type

### Milestone 2.2: Character Generation
- **CHAR-001**: Implement demographic generator
- **CHAR-002**: Build personality profiler with bias integration
- **CHAR-003**: Create medical knowledge simulator
- **CHAR-004**: Design background story generator

### Milestone 2.3: Adjudicator System
- **ADJ-001**: Implement ground truth determination
- **ADJ-002**: Create understanding assessment metrics
- **ADJ-003**: Build semantic similarity evaluator
- **ADJ-004**: Design comprehension scoring system
- **ADJ-005**: Implement conversation annotation framework

## Phase 3: Interaction Simulation (Weeks 7-8)
### Milestone 3.1: Conversation Engine
- **CONV-001**: Build turn-taking mechanism
- **CONV-002**: Implement context management
- **CONV-003**: Create flow controller
- **CONV-004**: Design termination conditions
- **CONV-005**: Build state management

### Milestone 3.2: Understanding Tracker
- **TRACK-001**: Implement understanding extractor
- **TRACK-002**: Create comprehension evolution tracker
- **TRACK-003**: Build divergence measurement
- **TRACK-004**: Design visualisation data preparation

## Phase 4: Frontend Development (Weeks 9-12)
### Milestone 4.1: Frontend Setup
- **FE-001**: Set up modern web framework
- **FE-002**: Create responsive layout system
- **FE-003**: Implement WebSocket communication
- **FE-004**: Design component architecture
- **FE-005**: Set up state management

### Milestone 4.2: User Interface
- **UI-001**: Build conversation display
- **UI-002**: Create character profile cards
- **UI-003**: Implement bias configuration sliders
- **UI-004**: Design test result input interface
- **UI-005**: Build medical history panel

### Milestone 4.3: Controls and Analytics
- **CTRL-001**: Create simulation parameter controls
- **CTRL-002**: Implement play/pause/reset functionality
- **CTRL-003**: Build turn navigation
- **CTRL-004**: Design export functionality
- **CTRL-005**: Create preset scenarios

### Milestone 4.4: Dashboard
- **DASH-001**: Build bias-comprehension visualiser
- **DASH-002**: Create understanding progression charts
- **DASH-003**: Implement homophily visualisation
- **DASH-004**: Design comparative analysis tools
- **DASH-005**: Build report generation

## Phase 5: Integration (Weeks 13-14)
### Milestone 5.1: Backend API
- **API-001**: Create RESTful API for simulation
- **API-002**: Implement WebSocket endpoints
- **API-003**: Build data persistence layer
- **API-004**: Design simulation history storage
- **API-005**: Create export/import functionality

### Milestone 5.2: Testing
- **TEST-001**: Unit tests for bias calculations
- **TEST-002**: Integration tests for LLM interactions
- **TEST-003**: End-to-end simulation tests
- **TEST-004**: Bias effect validation framework
- **TEST-005**: Performance benchmarking

## Phase 6: Enhancement and Polish (Weeks 15-16)
### Milestone 6.1: Advanced Features
- **ADV-001**: Multi-scenario batch running
- **ADV-002**: A/B testing framework
- **ADV-003**: Bias intervention simulator
- **ADV-004**: Recommendation engine
- **ADV-005**: Educational mode

### Milestone 6.2: Optimisation and Deployment
- **OPT-001**: LLM response caching
- **OPT-002**: Frontend performance optimisation
- **OPT-003**: Progressive loading
- **OPT-004**: Performance monitoring
- **OPT-005**: Deployment preparation

## Key Deliverables by Phase
1. **Phase 1**: Working LLM integration with basic data models
2. **Phase 2**: Functional bias system with character generation
3. **Phase 3**: Complete simulation engine with tracking
4. **Phase 4**: Full frontend with analytics dashboard
5. **Phase 5**: Integrated system with persistence
6. **Phase 6**: Production-ready application

## Success Criteria
- Accurate simulation of healthcare bias effects
- Clear correlation between bias strength and patient understanding
- Engaging, intuitive user interface
- Reliable LLM integration
- Comprehensive analytics and reporting