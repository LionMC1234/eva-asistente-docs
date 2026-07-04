# 🧬 Multi-Layer Memory System

A true assistant must remember. EVA implements a sophisticated, multi-tiered memory architecture that mirrors human cognitive processes, allowing it to maintain context over seconds, days, and months.

## The Five Layers of Memory

### 1. Working Memory (Immediate)
This is the fastest layer, operating purely in RAM. It tracks the exact state of the current interaction: the last few turns of conversation, the tools currently in use, and the immediate context window. It is highly volatile and designed for millisecond access.

### 2. Conversation History (Short-Term)
This layer records the chronological flow of the active session. If the user disconnects and reconnects, this cache is instantly restored, allowing the conversation to continue seamlessly. When the context window gets too large, this layer automatically compresses older turns into dense summaries to save processing power.

### 3. Project Memory (Spatial)
When working on specific tasks, like coding or data analysis, EVA builds a "spatial" awareness of the environment. It remembers the directory structure, the files it has opened, and the relationships between them. This allows the user to say "check that file we edited earlier" without needing to specify the exact path.

### 4. Semantic Memory (Long-Term)
This is the core of EVA's long-term knowledge. Important facts, user preferences, and past solutions are embedded as vectors and stored in a persistent database. When a user asks a question, EVA performs a semantic search across this database, retrieving memories that share *meaning* with the current topic, even if the exact keywords don't match.

### 5. Sleep Cycle (Consolidation)
Memory requires maintenance. When a user ends a session or the system goes idle, EVA initiates a background "Sleep Cycle." During this process, it reviews the recent conversation history, extracts valuable new knowledge, updates the semantic memory, and discards useless conversational filler. This prevents the database from bloating and keeps EVA's long-term recall sharp.
