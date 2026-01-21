# 🎓 Stubby AI Learning Assistant

> An intelligent, personality-driven AI tutor powered by Google Gemini AI and ElevenLabs TTS, designed to make learning engaging and personalized for students of all ages.

![React](https://img.shields.io/badge/React-19. 1.1-61DAFB?style=flat&logo=react)
![Vite](https://img.shields.io/badge/Vite-7.1.7-646CFF?style=flat&logo=vite)
![Gemini AI](https://img.shields.io/badge/Gemini_AI-2. 0_Flash-4285F4?style=flat&logo=google)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs-TTS-orange?style=flat)
![License](https://img.shields.io/badge/license-MIT-green?style=flat)

---

## 📖 Overview

**Stubby AI** is an innovative AI-powered learning assistant that transforms traditional studying into an interactive, personalized experience.  With **8 distinct AI personalities**, students can choose the teaching style that resonates with them—from a friendly tutor to a brainrot buddy who speaks pure Gen Z. 

### ✨ Key Features

🎭 **8 Unique AI Personalities** - Choose from friendly tutors, serious professors, storytellers, motivators, and more  
🎤 **Voice-Enabled Learning** - Speech-to-text input and text-to-speech responses with personality-matched voices  
📄 **Document Upload Support** - Upload PDFs and DOCX files for context-aware study assistance  
💬 **Conversational Interface** - Natural, engaging dialogue optimized for educational effectiveness  
🎯 **Personalized Learning Paths** - Tailored responses based on education level, grade, and study topics  
🌐 **Fully Client-Side** - No backend server required—runs entirely in your browser

---

## 🎭 AI Personalities

| Personality | Description | Best For |
|------------|-------------|----------|
| 🌟 **Friendly Tutor** | Bubbly, patient teacher with real-life examples and emojis | Grades 4–8 |
| 🎓 **Serious Professor** | Calm, precise educator with academic rigor and structured explanations | High school & university |
| 📚 **Storyteller** | Creative explainer who turns lessons into imaginative stories | Visual learners |
| 💪 **Coach Commander** | High-energy motivator with military-level discipline | Students needing motivation |
| 💼 **Visionary CEO** | Strategic leader connecting learning to real-world innovation | Career-focused learners |
| 🎮 **Pro Gamer** | Gaming legend using game terminology and quest vibes | Gamers |
| 🔥 **Brainrot Buddy** | Chronically online bestie speaking fluent Gen Z with memes | Gen Z students |
| 🎤 **Rhyming Rapper** | Cool educator explaining concepts in catchy rhymes | Auditory learners |

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v16 or higher)
- **npm** or **yarn**
- **Google Gemini API Key** ([Get one here](https://makersuite.google.com/app/apikey))
- **ElevenLabs API Key** ([Sign up here](https://elevenlabs.io/))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/zorojuro12/StubbyAI-learning-assistant.git
   cd StubbyAI-learning-assistant/study-buddy/studyAI
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the `study-buddy/studyAI` directory:
   ```env
   VITE_GEMINI_API_KEY=your_gemini_api_key_here
   VITE_ELEVEN_LABS_API_KEY=your_elevenlabs_api_key_here
   ```

4. **Run the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   
   Navigate to `http://localhost:5173`

---

## 🛠️ Tech Stack

### Frontend
- **React 19.1.1** - Modern UI library with hooks and context
- **Vite 7.1.7** - Lightning-fast build tool
- **React Router DOM** - Client-side routing
- **Tailwind CSS** - Utility-first styling

### AI & APIs
- **Google Gemini AI (2.0 Flash)** - Advanced language model for intelligent tutoring
- **ElevenLabs API** - High-quality text-to-speech with 8 unique voices

### Document Processing
- **PDF. js** - Client-side PDF parsing and text extraction
- **Mammoth.js** - DOCX document reading and conversion

### Browser APIs
- **Web Speech API** - Speech recognition for voice input
- **Audio API** - Audio playback control with mute/unmute

---

## 📊 Project Metrics

- ✅ **8 distinct AI personalities** with unique system prompts
- ✅ **8 voice profiles** mapped to personality types
- ✅ **1000-character response limit** for optimal performance
- ✅ **2+ file formats** supported (PDF, DOCX)
- ✅ **6 education levels** (Elementary to Professional)
- ✅ **3 main application routes** with context persistence

---

## 🏗️ Project Structure

```
StubbyAI-learning-assistant/
├── study-buddy/
│   └── studyAI/
│       ├── src/
│       │   ├── components/
│       │   │   ├── navbar.jsx          # Auto-hiding navigation bar
│       │   │   ├── setup.jsx           # User profile setup
│       │   │   ├── PersonalitiesPage.jsx  # Personality selection
│       │   │   └── chatbox.jsx         # Main chat interface
│       │   ├── context/
│       │   │   └── UserProfileContext.jsx  # Global state management
│       │   ├── App.jsx                 # Main app component
│       │   └── main.jsx                # Entry point
│       ├── . env                        # API keys (not committed)
│       ├── package.json
│       └── vite.config.js
└── README.md
```

---

## 🎯 How It Works

1. **Setup Profile** - Students select their education level, grade, and main study topic
2. **Choose Personality** - Pick an AI tutor personality that matches their learning style
3. **Upload Materials** - Optionally upload PDF or DOCX study materials
4. **Interactive Learning** - Chat with the AI using text or voice input
5. **Audio Responses** - Receive spoken explanations with personality-matched voices

### Core Features

#### 🎤 Voice Interaction
- **Speech-to-Text**: Click the microphone to speak your questions
- **Text-to-Speech**: Hear responses in personality-specific voices
- **Mute Control**: Toggle audio on/off for quiet study sessions

#### 📄 Document Context
- Upload study materials for context-aware assistance
- Supports PDF and DOCX formats
- Client-side processing for privacy

#### 💾 Session Persistence
- User profiles stored in localStorage
- Chat history maintained during session
- Personality preferences remembered

---

## 🔧 Configuration

### Adjusting Response Length
Edit `OUTPUT_CHAR_LIMIT` in `chatbox.jsx`:
```javascript
const OUTPUT_CHAR_LIMIT = 1000; // Increase or decrease as needed
```

### Customizing Personalities
Modify the `PERSONALITIES` object in `chatbox.jsx` to adjust system prompts:
```javascript
const PERSONALITIES = {
  "custom_personality": {
    name: "Custom Tutor",
    description: "Your custom tutor description",
    systemPrompt: "Your custom system prompt here..."
  }
};
```

### Adding New Voice IDs
Update `PERSONALITY_VOICE_IDS` in `chatbox.jsx` with ElevenLabs voice IDs:
```javascript
const PERSONALITY_VOICE_IDS = {
  "custom_personality": "your_voice_id_here"
};
```

---

## 🚧 Known Limitations

- **Browser Compatibility**: Speech recognition works best in Chrome and Edge
- **API Rate Limits**: Subject to Google Gemini and ElevenLabs rate limits
- **Response Length**: Limited to 1000 characters for optimal TTS performance
- **File Size**: Large PDFs may take time to process

---

## 🛣️ Roadmap

- [ ] Add progress tracking and analytics
- [ ] Implement quiz generation from uploaded documents
- [ ] Support for additional file formats (PPT, TXT)
- [ ] Multi-language support
- [ ] Mobile app version
- [ ] Collaborative study sessions
- [ ] Flashcard generation from conversations
- [ ] Export chat history as study notes

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Google Gemini AI** for powerful language models
- **ElevenLabs** for realistic text-to-speech
- **Mozilla PDF.js** for PDF parsing
- **Mammoth.js** for DOCX support
- **React Team** for the amazing framework

---

## 📧 Contact

**Project Creator**:  [@zorojuro12](https://github.com/zorojuro12)

**Project Link**: [https://github.com/zorojuro12/StubbyAI-learning-assistant](https://github.com/zorojuro12/StubbyAI-learning-assistant)

---

<div align="center">

**⭐ Star this repo if you find it helpful! ⭐**

Made with ❤️ for learners everywhere

</div>
