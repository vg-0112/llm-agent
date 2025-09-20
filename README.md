# 🧠 Research Assistant AI Agent

This project is a simple **AI research assistant agent** built with [LangChain](https://www.langchain.com/) and **Google Gemini**.  
It can:
- Search the web 🌍  
- Pull information from Wikipedia 📖  
- Save results to a local text file 💾  

All research results are structured into a JSON-like format using **Pydantic models**, making them easy to parse or extend.

---

## ⚙️ Features
- Uses **Google Gemini** (via `langchain-google-genai`) as the LLM  
- Built with **LangChain’s agent framework**  
- Integrates with tools:
  - **DuckDuckGo Search**  
  - **Wikipedia**  
  - **Save results to a file**  
- Environment variables handled via `.env`

---

## 🚀 Getting Started (Local Setup)

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR-USERNAME/llm-agent.git
cd llm-agent
```

### 2. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate   # On Mac/Linux
venv\Scripts\activate      # On Windows
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up Environment Variables
Create a .env file in the root of the project:
```bash
GOOGLE_API_KEY=your_gemini_api_key_here
```

### 5. Run the Agent
```bash
python main.py
```
you'll be prompted: 
```bash
What can i help you research?
```
Type a query (e.g. "History of quantum computing”) and the agent will:
- Search online
- Pull Wikipedia info
- Save structured results into research_output.txt

### Project Structure
llm-agent/

│── main.py           # Entry point for the agent

│── tools.py          # Custom tools (search, wiki, save)

│── requirements.txt  # Python dependencies

│── .env              # API keys 

│── research_output.txt (generated after saving)
