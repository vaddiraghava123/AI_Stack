### N8N Automation Agentic AI Framework Tool

n8n is a workflow automation platform that uniquely combines AI capabilities with business process automation, giving technical teams the flexibility of code with the speed of no-code. 

https://n8n.io/
  - Free trail 14 days
  UserId / password :   raghava.vaddi@****.com / ******
   vaddi.app.n8n.cloud
   

 
 
 Download and Install N8N in localhost
 -----------------------------------------
 Download
    > npx n8n   [ or]
	> npm install -g n8n
	  http://localhost:5678/

n8n@1.103.2

Components of an n8n workflow
-----------------------------------------
1. Trigger Node -> What starts the workflow? [ Eg - form filled, new row in a sheet)
2. Action Node -> What should happend next? [ Eg - Send email, post to Discord ]
3. Logic Node -> 	Conditions

Who should learn n8n
-----------------------------------------
Non-tech , any one , Developers who want a fast way to build integration

Agentic AI framework capabilities
-----------------------------------------
Component       Description
1. Agents      -> Autonomous system that can perceive, decide and act to achieve a goal
2. Environment -> The context in which agent operates ( web, APIs , user interfaces, etc)
3. Perception -> How the agent gathers information ( APIs, sensors, user input, etc)
4. Memory ->
			short-term  ( contexual) -  It stores recent information,
			long-term ( factual / task )- Its stores history information
5. Planning -> The agents ability to break goals into tasks or steps (task decomposition)
6. Decision Engine -> Uses rules, logic or LLMs to determine next best action
7. Tool use -> Invokes external tools like web search, APIs, database, calculators 
8. Learning -> Adapts from past results ( feedback  loops, reinforcement, fine-tuning)
9. Goal Alignment -> Ensures actions are relevant to the user-defined goal or prompt

Framework
----------------------------------------------------
LangGraph, CrewAI, Autogen(Microsoft), OpenAgents ( OpenAI)
Smol-AI, MetaGPT, AutoGPT, BabyAGI, SuperAGI, AgentVerse, Camel-AI

LangGraph
     Description - Event-driven multi-agent framework built on top of LangChain
	 Keyfeatures - Directed cyclic graphs, agent memory, retries, tool use

CrewAI
	Description - Multi-agent collabration with role-based agents
	Keyfeatures - Role, goal, task assignment, memory, hierarchical agents
	
Autogen
	Description - Conversational agent framework for multi-agent systems
	Keyfeatures - Group chats, human-AI feedback, agent roles, tools
	
OpenAgents [ OpenAI ]
	Description - Prototype agent system for task delegation using GPTs
	Keyfeatures - Tool usage, search, file browsing, calendar integration

Smol-AI 
	Description -  Lightweight AI agents that build software 
	Keyfeatures - Task breakdown, planning, codegen agents

MetaGPT
	Description - Multi-role collabrative agents for software development
	Keyfeatures - PM, Engineer, QA roles, Git style workflows
	
AutoGPT
	Description - Open-source autonomous agent powered by GPT+ memory
	Keyfeatures - Long-term memory, web search, tool use

BabyAGI
	Description - Minimal agent with taks planning and prioritization
	Keyfeatures - Todo-list manager, feedback loops

SuperAGI
	Description - Production-grade agent framework with GUI and marketplace
	Keyfeatures - Web UI, memory, agent templates, docker support
	
AgentVerse
	Description - Simulation platform for multi-agent environments
	Keyfeatures - Environment-based agent interaction

Practicles
----------------------------------------------------
			1. Build bot using n8n agents
			2. Build how to access daily planner sheet using n8n
			
 1. Build bot using n8n agents
			1.   Add "On Chat message" 
			2.  Add "AI Agent"
					Show features ( Memory, tools)
					Chat models
			  
			  [Using google gemini chat and its api key in n8n production environment ] 
			3. AIzaSyBWAig4HZ5ZfvelG6LT8Pjm_xrE3pGRfoI

			4. Add memory  [ Simple Memory ]
				Short memory - Stored in Vector DB or local

2.  Build how to access daily planner sheet using n8n  [ Access Daily planner ] 
				1.   Add "On Chat message" 
				2.  Add "AI Agent"
						Show features ( Memory, tools)
						Chat models
				3. Retrieve the URL while click "On Chat Message"
				Click on "active" chat	https://vaddi.app.n8n.cloud/webhook/b0e08663-12c6-4a5c-8473-2619af441835/chat
                
				4. Download the text excelfile "Planner"
				5. Add "Tools"
				   Google sheet link 

			Failed on getting rows using google chat bot..use openchat 
			also, failed in local n8n
			installed and created a start-n8n.bat file and then add below contents
			
			@echo off
			set N8N_BASIC_AUTH_ACTIVE=true
			set N8N_BASIC_AUTH_USER=admin
			set N8N_BASIC_AUTH_PASSWORD=yourpassword
			set N8N_PORT=5678

			n8n



Pull image and Installed n8n into docker desktop
--------------------------------------------

pull the image
> docker pull n8nio/n8n

run the n8n 
	> docker run -it --rm  -p 5678:5678 -e TZ=UTC n8nio/n8n 
	
Access 
	http://localhost:5678








Install the ollama image in docker
>   docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama

run the n8n after ollama image install
>   docker run -it --rm --add-host host.docker.internal:host-gateway --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n


Connect in n8n
--------------
http://host.docker.internal:11434

> after that run the ollama local llama models
   > ollama serve 
   Verify the models list in localhost 
   http://127.0.0.1:11434/api/tags
   
 Internal API key
 ---------------
 eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIzNTE2NWUxOS0xMmJkLTQ2NzgtOTg2NS0yM2VmMjIzYzFmNGUiLCJpc3MiOiJuOG4iLCJhdWQiOiJwdWJsaWMtYXBpIiwiaWF0IjoxNzUzNTU2OTc4fQ.AxAirg7gkQlOYp_vKXqk4FBh-0k1DtdgPM2Cbfj5i1w




















	
	 
