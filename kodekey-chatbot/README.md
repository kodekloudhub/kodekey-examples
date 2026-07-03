
# 🤖 KodeKey AI Chatbot 

A beautiful, modern ChatGPT-style chatbot with persistent conversation memory, multiple AI models, and an enhanced Streamlit interface powered by KodeKey's unified API.

![KodeKey Chatbot Interface](https://res.cloudinary.com/dezmljkdo/image/upload/v1752086507/Screenshot_2025-07-09_at_2.40.54_PM_aairko.png)

## ✨ Features

### 🎯 **Core Functionality**
- **Multiple AI Models**: Switch seamlessly between:
  - Claude Opus 4.8
  - Claude Sonnet 4.6
  - Claude Haiku 4.5
  - GPT 5.5
  - Gemini 3.5 Flash
  - DeepSeek V4 Pro
- **Persistent Conversation Memory**: All conversations saved locally as JSON files
- **Multiple Conversations**: Create unlimited chat sessions with easy switching
- **Streaming Responses**: Real-time typing effect for natural conversation flow
- **Personality System**: Choose from 5 AI personalities:
  - 🤖 Assistant - Helpful, harmless, and honest
  - 💻 Developer - Expert in coding and technical topics
  - 📚 Teacher - Patient educator who explains concepts clearly
  - 🎨 Creative - Imaginative and artistic
  - 📊 Analyst - Data-driven and analytical

### 🎨 **Beautiful Interface**
- **Modern Design**: Clean, minimalist interface inspired by ChatGPT
- **Vibrant Colors**: Purple/indigo gradients with smooth shadows
- **Professional UI**: Clean message bubbles with distinct user/AI styling
- **Responsive Design**: Works perfectly on desktop and mobile
- **Smooth Animations**: Hover effects, transitions, and loading states
- **Auto-load API Key**: Automatically loads from `.env` file if available

### 💾 **Data Management**
- **Local Storage**: Conversations saved as JSON files in `conversations/` directory
- **Search Functionality**: Search through all conversations by title or content
- **Auto-Save**: Every message automatically saved
- **Easy Management**: Delete conversations with one click
- **Smart Titles**: Automatic conversation titles based on content

### ⚡ **Quick Actions**
Start conversations quickly with built-in prompts:
- **🔍 Explain**: Get detailed explanations of concepts
- **🐛 Debug**: Help with code debugging and troubleshooting
- **✨ Create**: Assistance with creative projects
- **📈 Analyze**: Data analysis and insights

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- KodeKey API key (Get yours [here](https://learn.kodekloud.com/user/playgrounds/keyspace))

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd chatbot
```

2. Install dependencies:
```bash
pip install streamlit openai python-dotenv
```

3. Set up your API key (choose one method):

**Option A: Environment File (Recommended)**
Create a `.env` file in the project directory:
```bash
KODEKEY_API_KEY="your-kodekey-api-key-here"
KODEKEY_BASE_URL="https://api.ai.kodekloud.com/v1"
```

**Option B: Manual Entry**
Enter your API key in the sidebar when you run the app

4. Run the application:
```bash
streamlit run chatbot_stream.py
```

5. Open your browser to `http://localhost:8501`

## 🔧 Configuration

### Environment Variables
- `KODEKEY_API_KEY`: Your KodeKey API key (auto-loaded if present)
- `KODEKEY_BASE_URL`: KodeKey API endpoint (default: https://api.ai.kodekloud.com/v1)

### Customization
You can customize the chatbot by modifying:
- **Models**: Add or remove models in `AVAILABLE_MODELS`
- **Personalities**: Customize or add new personalities in `PERSONALITIES`
- **Quick Actions**: Modify quick action prompts in `QUICK_ACTIONS`
- **Styling**: Update CSS variables in the style section

## 📂 Project Structure
```
chatbot/
├── chatbot.py      # Main application file
├── conversations/        # Stored conversation JSON files
│   ├── uuid1.json
│   ├── uuid2.json
│   └── ...
├── .env                 # API key configuration (create this)
├── requirements.txt     # Python dependencies
└── README.md           # This file
```

## 🎯 Usage Guide

### Starting a New Chat
1. Click "➕ New Chat" in the sidebar
2. Choose a personality from the dropdown
3. Select your preferred AI model
4. Start typing or use quick actions

### Managing Conversations
- **Switch**: Click any conversation in the sidebar
- **Search**: Use the search box to find conversations
- **Delete**: Click the 🗑️ icon next to any conversation
- **Export**: Conversations are automatically saved as JSON files

### Adjusting Settings
- **Model**: Change AI model from the dropdown
- **Temperature**: Adjust creativity with the slider (0.0 = focused, 1.0 = creative)
- **Personality**: Switch personalities anytime from the sidebar

## 🔄 Comparison with Original

| Feature | Original | Improved |
|---------|----------|-----------|
| **Welcome Screen** | Large, takes up space | Minimal, shows chat immediately |
| **Storage** | Session only (volatile) | Persistent JSON files |
| **Search** | Export/Import only | Full-text search across all chats |
| **UI Style** | Basic gradient/glassmorphism | Modern, vibrant ChatGPT-inspired |
| **Conversation List** | Hidden in tabs | Always visible in sidebar |
| **Auto-save** | Manual export | Automatic after each message |
| **Title Generation** | Manual | Automatic based on content |
| **API Key** | Always prompted | Auto-loads from .env |
| **Personalities** | Fixed assistant | 5 selectable personalities |
| **Quick Actions** | None | 4 quick action buttons |

## 🛠️ Troubleshooting

### Common Issues

**API Key Not Working**
- Ensure your KodeKey API key is valid
- Check that the `.env` file is in the correct directory
- Verify the API endpoint URL is correct

**Conversations Not Saving**
- Check write permissions for the `conversations/` directory
- Ensure sufficient disk space

**Models Not Loading**
- Verify your API key has access to the selected models
- Check your internet connection

**UI Issues**
- Clear browser cache
- Try a different browser
- Ensure JavaScript is enabled

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
