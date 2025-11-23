# 🤖 AI Company Research Agent

An intelligent, conversational AI research assistant that generates strategic account plans for companies through natural dialogue. Built for the **Eightfold.ai AI Agent Assignment (Nov 2024)**.

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-green.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18+-61DAFB.svg)](https://reactjs.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 🌟 Key Features

```bash
cd frontend
npm run dev
```
*Frontend runs at `http://localhost:5173`*

Open `http://localhost:5173` in your browser and start chatting!

## 💬 Usage Examples

- **Simple**: "Tell me about Google"
- **Specific**: "Research Tesla's AI and autonomous driving strategy"
- **Voice**: Click the 🎤 microphone button and speak
- **Follow-up**: "Can you dig deeper into their risks?"
- **Update**: "Update the opportunities section to focus on emerging markets"
- **View Sources**: Click "X sources used" to see research URLs

## 🎭 User Persona Demonstrations

This agent handles diverse user types as required by the assignment:

### 1. The Confused User ✅
```
User: "I need help with something"
Agent: "I can help you research companies and generate strategic account plans. 
       Which company are you interested in?"
User: "Um, maybe something in tech?"
Agent: "Could you tell me the specific company name? For example, Apple, Microsoft, or Google?"
```

### 2. The Efficient User ✅
```
User: "Research Salesforce"
Agent: "Great! I'll research Salesforce for you. This will take a moment..."
[Generates full plan in ~15 seconds with 20+ sources]
```

### 3. The Chatty User ✅
```
User: "Hey! How's your day going?"
Agent: "I specialize in researching companies and creating strategic account plans. 
       Which company would you like to learn about?"
```

### 4. The Edge Case User ✅
```
User: "Write me a poem"
Agent: "I specialize in researching companies and creating strategic account plans. 
       Could you tell me which company you'd like to learn about?"
```

## 🏗️ Architecture & Design Decisions

### Why LangGraph?
- **Agentic Loops**: Unlike simple LLM chains, LangGraph allows the agent to critique its own research and refine it
- **State Management**: Clean way to track conversation history, research data, and plan sections
- **Extensibility**: Easy to add new nodes (e.g., "Conflict Resolution" for contradictory data)

### Why Conversational Interface?
- **Evaluation Criteria**: The assignment prioritizes "Conversational Quality" over functionality
- **User Experience**: Natural language is more accessible than forms
- **Flexibility**: Handles ambiguous requests, follow-ups, and clarifications

### Why Streaming?
- **Real-Time Feedback**: Users see progress ("📊 Researching...", "🛍️ Analyzing...")
- **Transparency**: Meets the requirement to "Provide updates during research"
- **Engagement**: Keeps users informed during the 15-20 second research process

### Why Tavily over DuckDuckGo?
- **Quality**: Tavily is purpose-built for LLM research (returns structured, relevant data)
- **Reliability**: More consistent results for company research
- **Fallback**: DuckDuckGo is still available if Tavily API is unavailable

## 📊 Requirements Alignment

| Assignment Requirement | Implementation | Evidence |
|------------------------|----------------|----------|
| **Gather from multiple sources** | ✅ 4 parallel web searches + Tavily API | Shows "20 sources used" |
| **Synthesize findings** | ✅ LLM-powered synthesis into 6 sections | Strategic Account Plan output |
| **Provide updates during research** | ✅ 4 real-time progress messages + conflict detection | "📊 Researching...", "⚠️ Conflict found..." |
| **Allow section updates** | ✅ Chat-based + UI-based editing | "Update the risks section" or click pencil icon |
| **Chat interaction** | ✅ Full conversational interface | Natural language parsing, clarifying questions |
| **Voice interaction** | ✅ Web Speech API | Microphone button + TTS responses |
| **Conversational Quality** | ✅ Intent parsing, context awareness | Handles 4 user personas |
| **Agentic Behaviour** | ✅ LangGraph cyclic workflow | Research → Critique → Synthesize loop |
| **Technical Implementation** | ✅ FastAPI streaming, React state mgmt | Real-time event streaming |
| **Intelligence & Adaptability** | ✅ Handles confused, efficient, chatty, edge-case users | Demonstrated in examples above |

## 📁 Project Structure

```
ai-research-agent/
├── server.py              # FastAPI backend with conversational logic
├── agent.py               # LangGraph agent (Research → Critique → Synthesize)
├── requirements.txt       # Python dependencies
├── .env                   # API keys (not in Git)
├── .env.example           # Example env file
├── frontend/
│   ├── src/
│   │   ├── App.jsx        # React main component (chat UI + voice)
│   │   ├── index.css      # Tailwind styles
│   │   └── main.jsx       # React entry point
│   ├── package.json       # Node dependencies
│   └── vite.config.js     # Vite configuration
├── README.md              # This file
├── DEPLOYMENT.md          # Deployment guide for Render
└── .gitignore             # Git ignore rules
```

## 🌐 Deployment

See [DEPLOYMENT.md](DEPLOYMENT.md) for detailed instructions on deploying to Render (free hosting).

**Quick Deploy to Render:**
1. Push to GitHub
2. Connect to Render
3. Add environment variables (API keys)
4. Deploy!

## 🎥 Demo Video

[Add your demo video link here after recording]

**Demo Script (10 minutes):**
1. Confused User (0:00-2:00)
2. Efficient User (2:00-4:00)
3. Voice Feature (4:00-6:00)
4. Edit Feature (6:00-8:00)
5. Edge Cases (8:00-10:00)

## 📝 Future Enhancements

- [ ] Multi-turn research refinement ("Dig deeper into X")
- [ ] Export to PDF/DOCX
- [ ] Comparison mode (compare 2 companies side-by-side)
- [ ] Multi-language support
- [ ] Custom research templates

## 🤝 Contributing

This is a submission for the Eightfold.ai assignment. For questions or feedback, please contact [your email].

## 📄 License

MIT License - see LICENSE file for details

## 🙏 Acknowledgments

- Built for the **Eightfold.ai AI Agent Assignment (Nov 2025)**
- Powered by Google Gemini, LangGraph, and Tavily
- UI inspired by modern conversational AI interfaces

---

**Made with ❤️ for Eightfold.ai**