# 🌍 AI Trip Planner with CrewAI & Groq

An intelligent AI-based travel assistant that creates a complete **7-day travel itinerary** based on your preferences. From city selection to packing tips, this project uses **CrewAI agents**, **Groq LLM**, and **real-time internet search** to handle everything for your next adventure.

> ✈️ Just tell it where you're traveling from, your preferred destinations, dates, and interests – and let the AI crew do the rest!

---

## 🧠 How It Works

The system follows a structured crew-based architecture using [CrewAI](https://github.com/joaomdmoura/crewai). Each agent specializes in one part of the trip-planning process:

### 🧭 Crew Agents

| Role | Description |
|------|-------------|
| **Expert Travel Agent** | The captain who coordinates everything – builds the final itinerary |
| **City Selection Expert** | Chooses the ideal city based on weather, events, and cost |
| **Local Tour Guide** | Recommends local attractions, customs, and hidden gems |

### 🗂️ Tasks Performed
- ✅ Identify the best city based on cost, weather, and your interests
- ✅ Compile a complete city guide with recommendations and logistics
- ✅ Generate a daily itinerary including:
  - Places to visit 🏛️  
  - Food & hotels 🍽️🏨  
  - Packing list 🎒  
  - Budget estimates 💰  
  - Safety tips 🚨  

---

## 🛠️ Tech Stack

- 🧠 [CrewAI](https://github.com/joaomdmoura/crewai) – Autonomous AI agents
- 🔗 [LangChain](https://www.langchain.com/) – Tool and agent integration
- ⚡ [Groq LLM](https://groq.com/) – Ultra-fast inference backend for conversation
- 🌐 [Serper.dev](https://serper.dev/) – Google Search API for real-time results
- 📦 Python 3.10+ with [Poetry](https://python-poetry.org/) for dependency management

---

## ⚙️ Setup Instructions

### 1. 🔧 Install Poetry & Platformdirs

```bash
pip install poetry platformdirs
```
> ✅ Poetry is used for dependency and virtual environment management.
✅ Platformdirs ensures correct OS path handling for cache and config storage.


### 2. 📦 Install Project Dependencies
```bash
poetry install --no-root
```
> Installs all dependencies listed in `pyproject.toml`, excluding the current project itself (no-root mode is useful for tools-only execution).

### 3. 🐚 Activate the Poetry Virtual Environment
```bash
poetry shell
```
>Launches a shell with all dependencies and tools in the correct environment context.

### 4. 🔑 Set Environment Variables
Create a `.env` file at the root:

```env
GROQ_API_KEY="your_groq_key_here"
SERPER_API_KEY="your_serper_key_here"
```

> You can get the [Groq API key](https://console.groq.com/home) and [Serper API key](https://serper.dev/).

---

## 🧪 Run the App
```bash
poetry run python main.py
```
Follow the interactive prompts:
- Enter your origin city
- Choose multiple destination cities
- Input travel dates
- Mention your interests
🎉 Get a full itinerary printed in the terminal!

---

## 🧠 Project Structure
```bash
├── agents.py              # Defines all the AI agents
├── tasks.py               # Task logic and goals assigned to agents
├── tools/
│   ├── calculator_tools.py # Mathematical calculator tool
│   └── search_tools.py     # Real-time web search tool
├── main.py                # Entry point of the app
├── .env                   # Environment variables (Not tracked in Git)
├── pyproject.toml         # Poetry dependency file
```

---

## 💡 Example Use-Case
**Input:**
- Origin: Mumbai
- Cities: Goa, Jaipur, Coorg
- Dates: July 10–16
- Interests: Beaches, Culture, Food

**Output:**
- Chooses Goa (ideal for monsoon)
- Suggests local food joints, beach activities, cultural festivals
- Recommends hotels and daily budget
- Adds weather & packing tips

---

## 🤝 Contributing
Pull requests are welcome! If you'd like to improve tasks, agents, or UI/UX, feel free to fork and contribute.

---

## 📜 License
This project is licensed under the **MIT License**.

---

## 🌟 Star This Repo
If you found this helpful, a ⭐ on GitHub would mean the world! 🚀
