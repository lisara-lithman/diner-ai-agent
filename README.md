# 🍔 The Diner AI Agent

A fully functional AI Restaurant Assistant that manages menus, provides real-time pricing, and processes orders using **OpenAI Function Calling**.

## ✨ Key Features
* **Live Menu Retrieval:** The agent queries a SQLite database via a tool to ensure it never "hallucinates" fake menu items.
* **Order Processing:** Calculates totals and saves customer orders directly into a database.
* **Smart UI:** A clean chat interface built with Gradio.
* **Data Persistence:** Uses SQLite to store the menu and order history.

## 🛠️ Architecture
The project follows a **Tool-Use (Agentic) Flow**:
1. **User** asks a question.
2. **AI** determines if it needs a tool (Menu lookup, Price check, or Order placement).
3. **Python** executes the SQL query and returns the data to the AI.
4. **AI** generates a friendly, accurate response based on that data.

## 🚀 Quick Start
1. **Clone the repo.**
2. **Install dependencies:** `pip install -r requirements.txt`
3. **Set up keys:** Create a `.env` file and add `OPENAI_API_KEY=your_key_here`.
4. **Run:** `python app.py`
