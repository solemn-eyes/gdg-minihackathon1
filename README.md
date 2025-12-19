# EmoWell 🧠💚

**Empowering Emotional Wellness Through Technology**

EmoWell is a comprehensive emotional support platform that combines modern web technology with AI-powered emotional intelligence to provide accessible mental health support. Our mission is to make emotional wellness tools available to everyone through an intuitive, secure, and engaging web application.

## 🌟 Features

### Core Functionality
- **AI-Powered Emotional Support Chatbot**: Intelligent conversations using OpenAI GPT-4o-mini and Anthropic Claude APIs
- **Mood Tracking**: Real-time mood selection with visual feedback and personalized responses
- **Goal Setting & Tracking**: Set wellness goals and monitor progress with visual charts
- **Interactive Games**: Therapeutic games including Tic-Tac-Toe, Memory Game, and Sudoku for stress relief
- **Secure Authentication**: User registration and login with local storage for demo purposes

### User Experience
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Intuitive Interface**: Clean, modern UI with smooth animations and transitions
- **Accessibility**: Screen reader support and keyboard navigation
- **Privacy-First**: All data stored locally in the browser

## 🛠 Tech Stack

### Frontend
- **HTML5**: Semantic markup and accessibility
- **CSS3**: Modern styling with gradients, animations, and responsive design
- **JavaScript (ES6+)**: Vanilla JavaScript for interactive functionality
- **Chart.js**: Data visualization for goal tracking

### APIs & Services
- **OpenAI GPT-4o-mini**: Primary AI model for emotional support conversations
- **Anthropic Claude**: Alternative AI model for enhanced responses
- **Google Gemini**: Additional AI option for comprehensive support

### Development Tools
- **Local Storage**: Client-side data persistence
- **HTTP Server**: Python's built-in server for local development

## 📁 Project Structure

```
EmoWell/
├── index.html                 # Landing page & authentication gateway
├── frontend/                  # Main application directory
│   ├── assets/               # Static assets
│   │   └── wellness-bg.svg   # Background image for auth pages
│   ├── auth.js               # Authentication logic (login/signup)
│   ├── homepage.html         # Main application page with chatbot
│   ├── homepage.js           # Homepage functionality (chat, mood, API)
│   ├── Goalspage.html        # Goal setting interface
│   ├── Goalspage.js          # Goal management logic
│   ├── GoalsTracker.html     # Progress tracking page
│   ├── GoalsTracker.js       # Chart generation and progress logic
│   ├── games.html            # Games selection page
│   ├── Games1.js             # Game-specific logic
│   ├── Games2.js             # Additional game functionality
│   ├── login.html            # Login form
│   ├── signup.html           # User registration form
│   └── homepage.css          # Main stylesheet
└── README.md                 # Project documentation
```

## 🚀 Installation & Setup

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Python 3.x (for local development server)
- Optional: OpenAI API key for enhanced AI responses

### Quick Start

1. **Clone or Download** the project files

2. **Start the Development Server** (deployment to happen soon :) )
   ```bash
   cd path/to/EmoWell
   python -m http.server 8000
   ```

3. **Open in Browser**
   - Navigate to `http://localhost:8000`; live server if present changes to be made
   - The application will automatically handle authentication flow

## 🎯 How It Works

### Authentication Flow

1. **Landing Page (`index.html`)**: Entry point that checks authentication status
   - **New Users**: Displays login/signup options
   - **Returning Users**: Automatically redirects to main app

2. **User Registration (`signup.html` + `auth.js`)**:
   - Email/password registration with validation
   - Password strength indicator
   - Real-time form validation
   - Secure password storage (localStorage for demo)

3. **Login System (`login.html` + `auth.js`)**:
   - Email/password authentication
   - Form validation and error handling
   - Automatic redirect to main application

### Main Application Flow

#### Homepage (`homepage.html` + `homepage.js`)
- **Mood Selection**: 5 mood options (Happy, Sad, Angry, Anxious, Neutral)
- **AI Chatbot**: Context-aware conversations based on selected mood
- **API Integration**: Optional OpenAI API key for enhanced responses
- **Fallback System**: Pre-written responses when API unavailable

#### Goal Management (`Goalspage.html` + `Goalspage.js`)
- **Goal Creation**: Add personal wellness goals
- **Progress Tracking**: Mark goals as completed
- **Persistent Storage**: Goals saved in localStorage

#### Progress Visualization (`GoalsTracker.html` + `GoalsTracker.js`)
- **Chart Generation**: Visual progress charts using Chart.js
- **Goal Analytics**: Track completion rates and trends
- **Responsive Charts**: Adapts to different screen sizes

#### Therapeutic Games (`games.html` + `Games1.js` + `Games2.js`)
- **Tic-Tac-Toe**: AI opponent for cognitive engagement
- **Memory Game**: Pattern matching for mental stimulation
- **Sudoku**: Logic puzzles for stress relief
- **Game Selection**: Intuitive game picker interface
** some games are optimal for mobile touch screens desktop users have good tic tac toe for them **
### Technical Implementation

#### Authentication System
```javascript
// User data stored in localStorage
{
  "user@example.com": {
    "name": "John Doe",
    "email": "user@example.com",
    "password": "hashed_password"
  }
}

// Session management
localStorage.setItem('loggedInUser', email);
```

#### Mood-Based AI Responses
```javascript
const moodContexts = {
  happy: "User is feeling happy and joyful...",
  sad: "User is feeling sad and may need support...",
  // ... additional mood contexts
};
```

#### API Integration
```javascript
// OpenAI integration with mood context
const response = await fetch("https://api.openai.com/v1/chat/completions", {
  method: "POST",
  headers: {
    "Authorization": `Bearer ${API_KEY}`,
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    model: "gpt-4o-mini",
    messages: [
      { role: "system", content: systemPrompt },
      { role: "user", content: userMessage }
    ]
  })
});
```

## 🎮 Usage Guide

### For New Users
1. Visit the landing page
2. Click "Sign Up" to create an account
3. Set a strong password (6+ characters)
4. Complete registration and login automatically

### Daily Wellness Routine
1. **Set Your Mood**: Choose from 5 mood options on the homepage
2. **Chat with AI**: Share thoughts with the emotional support chatbot
3. **Set Goals**: Create wellness objectives in the Goals section
4. **Play Games**: Engage in therapeutic activities when needed
5. **Track Progress**: Monitor goal completion in the Tracker

### Advanced Features
1. **API Integration**: Add OpenAI API key for enhanced AI responses
2. **Goal Analytics**: View progress charts and completion trends
3. **Cross-Device Sync**: All data persists in browser storage

## 🔒 Privacy & Security

- **Local Storage**: All user data stored locally in browser
- **No Data Transmission**: No personal data sent to external servers
- **Optional API Keys**: AI features only work with user-provided API keys
- **Secure Authentication**: Password-based access control

## 🌱 Wellness Philosophy

EmoWell believes that emotional wellness should be:
- **Accessible**: Available to everyone, everywhere
- **Private**: Personal thoughts and feelings remain confidential
- **Supportive**: AI assistance without replacing human professionals
- **Engaging**: Interactive elements make wellness enjoyable

## 🤝 Contributing

This project was created for the GDG Mini-Hackathon 1. To contribute:
1. Fork the repository
2. Create a feature branch
3. Make your improvements
4. Submit a pull request

## 📄 License

This project is open-source and available under the MIT License.

---

**Remember**: While EmoWell provides emotional support tools, it is not a substitute for professional mental health care. If you're experiencing serious emotional distress, please consult qualified mental health professionals.
