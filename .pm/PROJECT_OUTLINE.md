
I'd like to build a tool to simulate and examine the effect of biases in healthcare interactions in the interpretation of results, and in particular the critical strength of homophily, similar to Schelling's model of segregation. For this, I would like to set up the following simulator in Python, with a frontend. 

1) we select a test result or set of test results, together with a medical history.
2) We then instantiate a patient and a physician. The physician's job is to explain the results to the patient. 
3) For the patient and the physician, we simulate some immutable characteristics. These for now should be sex, age, education, socioeconomic status.
4) We also add a slider to determine how strong the bias is. This can be with a Likert scale. 
5) We create prompts to the physician and the patient that reflects the strength of their bias. 
6) We begin by a separate agent, the adjudicator, determining the correct diagnosis/meaning of the results. 
7) We then simulate an itneraction, and at every stage, the patient describes his understanding of the results. We annotate every stage of the interaction by the adjudicator's assessment of how close the patient's udnerstanding is to the actual meaning of the results. 
8) The interaction ends after a few turns. 
9) We then compare the level of bias and homophily to how close the patient's understanding of the results were. 

We're using MedGemma for the doctor and a regular Gemma model for the patient. We'll be using both via LMStudio running locally that we access through the openai compatible api. The app is in python and runs with a clear, modern frontend that shows the simulated conversation in a nice engaging way, as well as allows users to customise the interaction parameters like maximum length, the patient and physician biases etc. 

Set of biases for patient:
* self-diagnosis confirmation (pt seen this on the internet)
* gender (allow for positive and negative: patient trusts physician's gender, vs distrusts)
* ethnicity (allow for positive and negative)
* bias vs medical system
* recency/availability (patient knows a relative who has a certain condition)

Set of biases for physician:
* recency,false consensus, frequency, status quo, confirmation
* gender (physician regards patient's gender as inferior)
* ethnicity
* education (physician is opposed to people the further away they are of his educational status)

We can expand on these later. 

I find this a fascinating project that echoes Schelling's segregation model in healthcare contexts. The interplay between homophily and bias in medical communication is indeed a critical area to explore. Let me outline a comprehensive implementation plan, breaking it into discrete, manageable steps.

## Implementation Plan: Healthcare Bias Simulation Tool

### Phase 1: Foundation

#### Step 1: Core Data Models and Architecture
- Define data structures for Patient, Physician, TestResult, MedicalHistory
- Create BiasProfile class with configurable parameters
- Design Interaction class to store conversation history
- Implement configuration management for simulation parameters
- Set up project structure with clear separation of concerns

#### Step 2: LLM Integration Layer
- Create abstract LLM interface for model-agnostic design
- Implement LMStudio connector using OpenAI-compatible API
- Build model manager to handle MedGemma and Gemma instances
- Implement prompt templating system
- Add error handling and retry logic for API calls

### Phase 2: Bias and Simulation Engine

#### Step 3: Bias System Implementation
- Create bias taxonomy with weighted parameters
- Implement bias-to-prompt translation logic
- Build bias strength calculator (Likert scale integration)
- Design homophily measurement system
- Create prompt injection strategies for each bias type

#### Step 4: Character Generation and Profiling
- Implement demographic characteristic generator
- Build personality profile creator based on bias settings
- Create medical knowledge level simulator
- Design background story generator for contextualisation

#### Step 5: Adjudicator System
- Implement ground truth determination logic
- Create understanding assessment metrics
- Build semantic similarity evaluator
- Design scoring system for patient comprehension
- Implement annotation framework for conversation turns

### Phase 3: Interaction Simulation

#### Step 6: Conversation Orchestrator
- Build turn-taking mechanism
- Implement context management between turns
- Create conversation flow controller
- Design termination conditions
- Build state management for multi-turn interactions

#### Step 7: Understanding Tracker
- Implement patient understanding extractor
- Create comprehension evolution tracker
- Build divergence measurement from ground truth
- Design visualisation data preparation

### Phase 4: Frontend and Visualisation

#### Step 8: Frontend Framework Setup
- Set up modern web framework (React/Vue/Svelte)
- Create responsive layout system
- Implement WebSocket for real-time updates
- Design component architecture
- Set up state management (Redux/Vuex/stores)

#### Step 9: Interaction Interface
- Build conversation display component
- Create character profile cards
- Implement bias configuration sliders
- Design test result input interface
- Build medical history configuration panel

#### Step 10: Simulation Controls
- Create simulation parameter controls
- Implement play/pause/reset functionality
- Build turn-by-turn navigation
- Design export functionality for results
- Create preset scenario selector

#### Step 11: Analytics Dashboard
- Build bias-comprehension correlation visualiser
- Create understanding progression charts
- Implement homophily effect visualisation
- Design comparative analysis tools
- Build report generation system

### Phase 5: Integration and Enhancement

#### Step 12: Backend API Development
- Create RESTful API for simulation management
- Implement WebSocket endpoints for real-time updates
- Build data persistence layer
- Design simulation history storage
- Create export/import functionality

#### Step 13: Testing and Validation
- Implement unit tests for bias calculations
- Create integration tests for LLM interactions
- Build end-to-end simulation tests
- Design bias effect validation framework
- Implement performance benchmarking

#### Step 14: Advanced Features
- Add multi-scenario batch running
- Implement A/B testing framework
- Create bias intervention simulator
- Build recommendation engine for reducing bias
- Design educational mode for healthcare training

### Phase 6: Polish and Deployment

#### Step 15: Performance Optimisation
- Implement caching for LLM responses
- Optimise frontend rendering
- Add progressive loading
- Implement efficient state management
- Create performance monitoring

#### Step 16: Documentation and Deployment
- Write comprehensive API documentation
- Create user guide with examples
- Build deployment scripts
- Set up continuous integration
- Design maintenance procedures

## Individual Feature Requirements

For each step, you'll want to create specific requirement documents. For instance:

**Step 3 (Bias System) Requirements:**
- Input: Bias type, strength (1-5 Likert), character profile
- Output: Modified prompt with bias-appropriate language
- Special considerations: Ensure biases are realistic but not offensive
- Testing: Validate bias manifestation in generated text

**Step 6 (Conversation Orchestrator) Requirements:**
- Handle asynchronous LLM calls
- Maintain conversation context
- Implement turn timeout handling
- Store full interaction history
- Provide hooks for adjudicator assessment

This modular approach allows you to tackle each component independently whilst maintaining a clear vision of the integrated system. The beauty of this design is that it mirrors the complexity of real healthcare interactions whilst providing controlled experimental conditions, much like Schelling's original model did for residential segregation.
