# 🧠 The Cognitive Pipeline

The Cognitive Pipeline is the central nervous system of EVA. It is responsible for taking raw, unstructured input (like a continuous stream of human voice) and transforming it into structured understanding, actionable plans, and ultimately, real-time responses.

Unlike traditional chatbots that use a simple "request-response" loop, EVA operates on a continuous, stateful pipeline designed for real-time interaction.

## Core Stages of the Pipeline

### 1. Sensory Ingestion (Perception)
EVA constantly monitors input channels. For voice, it doesn't wait for a button press. It analyzes the audio stream in real-time, detecting speech boundaries, pauses, and interruptions. 
*   **Barge-in Detection:** If EVA is speaking and the user interrupts, the pipeline instantly halts the audio output, updates the context with the interruption, and shifts back to listening mode.

### 2. Intent & Context Extraction
Raw text or transcribed audio is passed into an understanding layer. This layer doesn't just parse keywords; it evaluates the input against:
*   The current conversation history.
*   The user's known preferences.
*   The active environment (e.g., what files are open, what time it is).
It determines the *true intent* behind the words.

### 3. Orchestration & Routing
Once the intent is clear, the Core Orchestrator decides the next step. 
*   Is this a simple conversational reply? Route directly to the language model.
*   Does this require fetching data? Route to the Execution Layer.
*   Is this a complex, multi-step goal? Route to the Reasoning Engine and Agent Supervisor.

### 4. Synthesis & Response
Data gathered from tools, memory, or agents is synthesized into a coherent response. If the interaction is voice-based, the response is streamed back as audio chunk-by-chunk, ensuring the lowest possible latency between the system's "thought" and its "speech."

## Design Principles
*   **Asynchronous by Default:** The pipeline never blocks. While one part of the system is researching a topic, another part can be preparing the audio stream.
*   **Stateful Awareness:** The pipeline always knows its current state (Listening, Thinking, Executing, Speaking) and manages transitions gracefully.
