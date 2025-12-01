# VYNTAL-I
VYNTAL-I is an autonomous multi-agent intelligence engine that transforms natural-language queries into real-time, actionable data insights.

VYNTAL-I transforms natural language questions into instant, accurate data insights. No SQL or Python knowledge required—just ask your questions in plain English and let specialized AI agents handle the rest.
Built with Google's Agent Development Kit (ADK) and powered by Gemini 2.0, VYNTAL-I orchestrates multiple specialized agents that work together like an analytics team:

🔍 SQL Agent - Generates and executes optimized SQL queries
🐼 Pandas Agent - Performs complex Python-based data analysis
🌐 Search Agent - Retrieves real-time external insights via Google Search

💡 Why VYNTAL-I?
The Problem

Barrier to entry: Most people lack SQL/Python expertise
Slow workflows: Analysts spend hours writing and debugging queries
Tool fragmentation: Constant switching between querying, analyzing, and visualizing
Bottlenecks: Non-technical users depend entirely on data teams
Stale insights: External/real-time data requires manual searching

The Solution
VYNTAL-I provides a unified, intelligent, and automated analytics system that:

✅ Accepts natural language queries
✅ Automatically routes to the right specialist agent
✅ Executes queries and analysis
✅ Generates visualizations
✅ Provides actionable insights in seconds

┌─────────────────────────────────────────────────────────────┐
│                      User Interface                         │
│          (Gradio / Web UI / Notebook / API)                 │
└────────────────────┬────────────────────────────────────────┘
                     │ Natural language queries
                     ▼
┌─────────────────────────────────────────────────────────────┐
│              InMemoryRunner (ADK Orchestrator)              │
│          Plans → Routes → Executes → Synthesizes            │
└────────┬────────────────────────┬────────────────────┬──────┘
         │                        │                    │
    ┌────▼─────┐          ┌──────▼──────┐      ┌─────▼──────┐
    │   SQL    │          │   Pandas    │      │   Search   │
    │  Agent   │          │   Agent     │      │   Agent    │
    └────┬─────┘          └──────┬──────┘      └─────┬──────┘
         │                       │                    │
    ┌────▼─────────────────┬─────▼─────────┬─────────▼───────┐
    │  execute_sql tool    │ execute_pandas│  google_search  │
    │  (FunctionTool)      │ (FunctionTool)│  (AgentTool)    │
    └──────────┬───────────┴───────────────┴─────────────────┘
               │
          ┌────▼─────┐                    ┌──────────────┐
          │  DuckDB  │                    │   Gemini     │
          │ Database │◄───────────────────┤  LLM (2.5)   │
          └──────────┘                    └──────────────┘

✨ Key Features
🤖 Multi-Agent Intelligence

Specialized agents for SQL, Pandas, and web search
Collaborative workflow - agents can call each other
Automatic routing based on query complexity

🛠️ Advanced Tool Integration

FunctionTool: Safe SQL and Pandas code execution
AgentTool: Nested agent invocation for search
Retry logic: Resilient API calls with exponential backoff

📊 Comprehensive Analytics

Automated data querying and analysis
Built-in visualization generation (Matplotlib, Seaborn)
Real-time external data via Google Search grounding

💻 User-Friendly Interface

Gradio UI for interactive exploration
Notebook integration for data scientists
API/CLI support for automation

          
🎯 Example Queries
 Simple aggregation
"Show me the top 5 categories by revenue"

# Trend analysis
"What are the monthly revenue trends for 2024?"

# Regional comparison
"Compare revenue across all regions"

# External insights
"What are current market trends in electronics?"

# Complex analysis
"Show profit margins by category and region for Q4"

🎓 Technical Highlights
ADK Features Implemented
✅ Multiple Agent Orchestration
✅ FunctionTool Integration (SQL & Pandas execution)
✅ AgentTool Wrapping (Search agent as tool)
✅ InMemoryRunner (Central orchestration)
✅ Retry Configuration (Resilient API calls)
✅ Tool Safety (Sandboxed code execution)
Advanced Capabilities

Dynamic agent selection based on query type
Cross-agent tool invocation
Automated visualization generation
Real-time external data grounding
Conversation history tracking
Error handling and recovery

🛣️ Roadmap
Phase 1 (Current)

 Core multi-agent system
 SQL and Pandas agents
 Search integration
 Gradio UI

Phase 2 (Planned)

 Visualization Agent (specialized charting)
 Memory/RAG integration for context
 Multi-user support with authentication
 Dashboard builder
 Scheduled reports and alerting

Phase 3 (Future)

 Enterprise deployment
 Cloud data source connectors
 Advanced NLP query understanding
 Custom agent marketplace
 Mobile app



Acknowledgments

Google ADK Team for the Agent Development Kit
Google DeepMind for Gemini
DuckDB for fast in-memory analytics
Gradio for easy UI creation

