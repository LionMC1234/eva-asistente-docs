# 💡 The Reasoning System

EVA's Reasoning System is what elevates it from a simple assistant to an autonomous operator. When presented with a complex problem, EVA does not immediately guess the answer; it stops to think, plan, and evaluate.

## How EVA Reasons

### 1. Task Decomposition
When given a high-level goal (e.g., "Analyze the latest tech news and write a summary to my desktop"), the Reasoning Engine breaks this down into a structured dependency tree.
*   Step 1: Search the web for tech news.
*   Step 2: Read the top 3 articles.
*   Step 3: Synthesize the information.
*   Step 4: Access the local file system.
*   Step 5: Write the file.

### 2. Structured Planning
The engine evaluates the dependencies of each step. It knows that Step 3 cannot begin until Steps 1 and 2 are complete, but it also knows that reading multiple articles can happen in parallel. It builds an execution graph to optimize for speed and reliability.

### 3. Meta-Reasoning and Confidence
Before executing any plan, EVA evaluates its own strategy. 
*   *Do I have all the necessary context?* 
*   *Is this plan safe?* 
*   *What is the likelihood of failure?*
If the internal confidence score for a step is too low, the Reasoning System will proactively halt and ask the user for clarification before proceeding.

### 4. Self-Correction
If a step fails during execution (e.g., a website is unreachable, or a shell command throws an error), the Reasoning System intercepts the failure. Instead of crashing or simply saying "I failed," it analyzes the error output, adjusts its strategy, and attempts an alternative approach.

## Separation of Concerns
To achieve high-quality reasoning without sacrificing response time, EVA separates *conversational thinking* from *deep reasoning*. Fast, chat-like responses bypass the heavy planning engine, while complex tasks are routed to specialized reasoning models optimized for logic and code generation.
