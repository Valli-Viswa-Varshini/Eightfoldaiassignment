# 🤖 AI Company Research Agent

An intelligent conversational AI assistant that researches companies in real-time, synthesizes insights, and generates a structured Strategic Account Plan — through natural dialogue using chat + voice.

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Backend-brightgreen.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-Frontend-61DAFB.svg)](https://reactjs.org/)
[![Gemini](https://img.shields.io/badge/LLM-Gemini-blueviolet)]()
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## ✨ Key Capabilities

✔ Natural conversation understanding  
✔ Voice-enabled research + responses  
✔ Real-time business research from the web  
✔ Organized strategic account plan with 6 sections  
✔ Section-level editing using follow-up instructions  
✔ Clarification guidance for confused users  
✔ Safety guardrails against invalid or unrelated requests  
✔ Live progress streaming during research

---

## 📌 System Architecture

📍 *Architecture Diagram*  
<img width="1014" height="1614" alt="Untitled diagram-2025-11-24-033751" src="https://github.com/user-attachments/assets/7675602b-0b8e-4f50-a535-09260d63005e" />


### Architecture Summary

| Component | Purpose |
|----------|---------|
| React UI | Chat + voice interface |
| FastAPI Server | Intent parsing + conversation management |
| LangGraph Agent | Research → Critique → Synthesis loop |
| Web Search | Online data retrieval |
| Streaming Events | Live progress while researching |
| Voice Interface | Web Speech API (browser native) |

🧠 Research Loop:

1️⃣ Understand user intent  
2️⃣ Search multiple high-quality sources  
3️⃣ Validate data (detect gaps / conflicts)  
4️⃣ Synthesize final structured business plan  
5️⃣ Allow follow-up modifications anytime  

---

## 🗣️ Example User Commands

- “Tell me about Tesla”
- “Update the risks to focus on privacy concerns”
- “I don’t know… suggest a major AI company?”
- “Research Netflix and recommend actions for subscriber retention”

🎤 Voice Input also supported — click the Mic button!

---

## 👥 User Persona Handling

| User Type | Bot Behavior |
|----------|--------------|
| Confused user | Suggests companies + asks clarification |
| Efficient user | Immediately performs full research |
| Chatty user | Redirects politely back to task |
| Edge-case user | Refuses unsupported actions safely |

---

---

## 🚀 Local Development

Clone the repository:

```bash
git clone <repo-url>
cd ai-research-agent
pip install -r requirements.txt
uvicorn server:app --reload
```

## Then start the frontend:

cd frontend
npm install
npm run dev


➡ Visit UI: http://localhost:5173

## 🌍 Live Deployment

Public Render Deployment:
🔗 [https://company-account-planner-ai.onrender.com/](https://company-account-planner-ai.onrender.com/)

⚠️ Note: Render Free plans may take 15–30 sec to “Wake Up” if idle


## 🎬 Demo Video

📹 Full Project Walkthrough (Voice + Screen Recording):
🔗 [https://drive.google.com/file/d/1io0Krqgh1MM0QlENgNqqd7iw5xChC70W/view?usp=sharing](https://drive.google.com/file/d/1io0Krqgh1MM0QlENgNqqd7iw5xChC70W/view?usp=sharing)

## 📂 Project Structure

```text
ai-research-agent/
├── agent.py            # LangGraph research workflow (autonomous loop)
├── server.py           # FastAPI backend (streaming API)
├── requirements.txt    # Python dependencies
├── frontend/           # React UI (chat + voice)
│   ├── src/App.jsx     # Main chat+voice component
│   ├── src/index.css   # Styling
│   └── src/main.jsx    # Frontend entry point
└── README.md           # Documentation

```

## 📈 Technical Highlights
✔ Uses Gemini for factual reasoning + structured synthesis  
✔ LangGraph autonomous cycle → Research → Critique → Synthesize  
✔ Streaming keeps users engaged during plan generation  
✔ State memory → Allows follow-up edits to specific sections  
✔ Voice support via Web Speech API 🎤  
✔ Clean frontend-backend separation for maintainability  

## 🚧 Future Improvements

Multi-turn refinement (“dig deeper into AI strategy”)

Export to PDF / PowerPoint

Compare companies side-by-side

Personalized recommendations based on context

Multi-language conversation support

## 📜 License

Open-source under MIT License
Free to modify and extend 💡

✨ Built with passion to make enterprise research intelligent & interactive!
