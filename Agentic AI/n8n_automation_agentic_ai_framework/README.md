# 🤖 N8N Automation Agentic AI Framework Tool

n8n is a workflow automation platform that uniquely combines AI capabilities with business process automation, giving technical teams the flexibility of code with the speed of no-code.  
🔗 [n8n.io](https://n8n.io/) — *Free Trial: 14 days*

- **User ID / Password**:  
  `raghava.vaddi@****.com / ******`

- **External Hosted Site**:  
  `https://vaddi.app.n8n.cloud`

---

## ⚙️ Components of an n8n Workflow

| Node Type       | Description                                      | Example                                   |
|------------------|--------------------------------------------------|-------------------------------------------|
| **Trigger Node** | What starts the workflow?                        | Form filled, new row in a sheet           |
| **Action Node**  | What should happen next?                         | Send email, post to Discord               |
| **Logic Node**   | Conditional checks that determine workflow paths | If status is "approved", then send email  |

---

## 👥 Who Should Learn n8n?

- Non-technical users  
- Business analysts  
- Developers who want a faster way to build integrations and automate processes

---

## 🧠 Agentic AI Framework Capabilities

### Key Components of Agent Systems

| Component          | Description                                                                                       |
|--------------------|---------------------------------------------------------------------------------------------------|
| **Agents**         | Autonomous systems that can perceive, decide, and act to achieve a goal                           |
| **Environment**    | The context in which the agent operates (web, APIs, user interfaces, etc.)                        |
| **Perception**     | How the agent gathers information (APIs, sensors, user input, etc.)                               |
| **Memory**         | - **Short-term (contextual)**: Stores recent info<br> - **Long-term (factual/task)**: Stores history |
| **Planning**       | The agent’s ability to break goals into tasks or steps (task decomposition)                       |
| **Decision Engine**| Uses rules, logic, or LLMs to determine the next best action                                      |
| **Tool Use**       | Invokes external tools like web search, APIs, databases, calculators                              |
| **Learning**       | Adapts from past results (feedback loops, reinforcement, fine-tuning)                             |
| **Goal Alignment** | Ensures actions are relevant to the user-defined goal or prompt                                   |

---

## 🔗 Multi-Agent Frameworks Comparison

| Framework     | Description                                                               | Key Features                                                   |
|---------------|---------------------------------------------------------------------------|----------------------------------------------------------------|
| **LangGraph** | Event-driven multi-agent framework built on top of LangChain              | Directed cyclic graphs, agent memory, retries, tool use        |
| **CrewAI**    | Multi-agent collaboration with role-based agents                          | Role, goal, task assignment, memory, hierarchical agents        |
| **Autogen**   | Conversational agent framework for multi-agent systems                    | Group chats, human-AI feedback, agent roles, tools              |
| **OpenAgents** (OpenAI) | Prototype agent system for task delegation using GPTs           | Tool usage, search, file browsing, calendar integration         |
| **Smol-AI**   | Lightweight AI agents that build software                                 | Task breakdown, planning, codegen agents                        |
| **MetaGPT**   | Multi-role collaborative agents for software development                  | PM, Engineer, QA roles, Git style workflows                     |
| **AutoGPT**   | Open-source autonomous agent powered by GPT + memory                      | Long-term memory, web search, tool use                          |
| **BabyAGI**   | Minimal agent with task planning and prioritization                       | Todo-list manager, feedback loops                               |
| **SuperAGI**  | Production-grade agent framework with GUI and marketplace                 | Web UI, memory, agent templates, Docker support                 |
| **AgentVerse**| Simulation platform for multi-agent environments                          | Environment-based agent interaction                             |

---

## 🔬 Practicals

### 🧠 n8n Agent Bot & Daily Planner Integration Guide

---

## ✅ 1. Build a Bot Using n8n Agents

### Steps:

1. **Add "On Chat Message" Node**
2. **Add "AI Agent" Node**
   - **Features**:
     - Memory
     - Tools
   - **Chat Models**:
     - Google Gemini Chat  
       API Key:  
       `AIzaSyBWAig4HZ5ZfvelG6LT8Pjm_xrE3pGRfoI`
3. **Add Memory Node**
   - Type: Simple Memory  
   - Storage: Vector DB or local (short-term)

---

## ✅ 2. Access the Daily Planner Sheet Using n8n

### Steps:

1. **Add "On Chat Message" Node**
2. **Add "AI Agent" Node**
   - Features: Memory, Tools
3. **Retrieve the Planner URL**
   - Click "Active Chat":  
     [https://vaddi.app.n8n.cloud/webhook/b0e08663-12c6-4a5c-8473-2619af441835/chat](https://vaddi.app.n8n.cloud/webhook/b0e08663-12c6-4a5c-8473-2619af441835/chat)
4. **Download the Excel File**  
   - File Name: `Planner`
5. **Add "Tools" Node**
   - Connect to Google Sheets

> ❌ **Issues**:
- Failed to retrieve rows via Google Chat Bot
- Failed in local n8n
- Temporary workaround: **Use OpenChat**

---

## 🛠️ 3. Install & Run n8n Locally (Docker Preferred)

### 🐳 Using Docker Desktop

#### Step 1: Run Ollama in Docker

```bash
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

#### Step 2: Pull & Run n8n Docker Image

```bash
# Pull n8n image
docker pull n8nio/n8n

# Run n8n
docker run -it --rm -p 5678:5678 -e TZ=UTC n8nio/n8n

# OR run with Ollama and volume
docker run -it --rm --add-host host.docker.internal:host-gateway \
  --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```

📍 Access: [http://localhost:5678](http://localhost:5678)

---

## 🔧 4. Configure Ollama with Local n8n

- **Ollama API URL**:  
  `http://host.docker.internal:11434`

- **Start Ollama Service**:
  ```bash
  ollama serve
  ```

- **Verify Installed Models**:  
  [http://127.0.0.1:11434/api/tags](http://127.0.0.1:11434/api/tags)

---

## ⚙️ 5. Batch File for Starting n8n (Windows)

Create a file named `start-n8n.bat`:

```bat
@echo off
set N8N_BASIC_AUTH_ACTIVE=true
set N8N_BASIC_AUTH_USER=admin
set N8N_BASIC_AUTH_PASSWORD=yourpassword
set N8N_PORT=5678
n8n
```

---

## 🧪 Optional: Install n8n via npm/npx

```bash
# Run using npx
npx n8n

# OR install globally
npm install -g n8n
```

📍 Access: [http://localhost:5678](http://localhost:5678)

> ⚠️ *Note: Local Ollama connection failed using this method.*

---

## 📸 Screenshots

> *(Add visual documentation here as needed.)*

<img width="841" height="216" alt="image" src="https://github.com/user-attachments/assets/c511cdb1-944f-403e-9825-8102a06e77f7" />

<img width="614" height="466" alt="image" src="https://github.com/user-attachments/assets/41641227-eadc-4272-8afb-618a88a56328" />

<img width="1119" height="111" alt="image" src="https://github.com/user-attachments/assets/8266357c-bc84-4312-83a5-b17af9c7c18c" />

<img width="691" height="191" alt="image" src="https://github.com/user-attachments/assets/99ebb4f5-0e70-463c-a1c8-cb31ca842dff" />

<img width="1104" height="389" alt="image" src="https://github.com/user-attachments/assets/6c1999d1-d7c4-4cc9-bae9-912f18fd3e79" />

<img width="1590" height="677" alt="image" src="https://github.com/user-attachments/assets/6783a9f6-a68e-4557-bf7f-cf6fe6b96c65" />

<img width="380" height="599" alt="image" src="https://github.com/user-attachments/assets/da1be7c5-14cc-4a41-b477-449935defdb5" />

http://localhost:5678/webhook/02a6d54c-7e81-4cdc-b100-f0886fa63c60/chat

<img width="1575" height="720" alt="image" src="https://github.com/user-attachments/assets/8c62ab65-ace4-4421-9f3f-c96d02bccab4" />


