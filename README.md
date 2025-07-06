
# Google Gemini Based Personal AI Assistant **Who Can See You** - "Friday"

A real-time AI assistant with Camera Access built with LiveKit and Google's Realtime API, inspired by the AI assistant from Iron Man. This project creates a voice-enabled personal assistant that can assist in search with weather information, perform web searches, and send email.

# Features

- Voice-enabled interaction with real-time audio processing
- AI assistant with Access to Camera Visual meaning an AI assistant that can see you or environment through Camera 
- Weather information for any city
- Web search capabilities using DuckDuckGo
- Email sending through Gmail
- Noise cancellation for better audio quality
- Butler-like personality with professional yet slightly sarcastic responses

# Architecture
The assistant is built using:

- LiveKit for real-time audio/video communication
- Google's Realtime API for natural language processing
- Python as the main programming language
- WebRTC for seamless audio streaming

# Prerequisites

- Python 3.8 or higher
- LiveKit Cloud account
- Google AI Studio API key
- Gmail account with App Password enabled

# Installation

Create a virtual environment:

```bash
python -m venv .venv

# On Windows:
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Configuration

Environment Variables

Create a .env file in the project root with the following variables:

LiveKit Configuration  
LIVEKIT_URL=wss://personal-ai-assistant-q2i9se0p.livekit.cloud  
LIVEKIT_API_KEY=your_livekit_api_key  
LIVEKIT_API_SECRET=your_livekit_api_secret

Google AI Studio  
GOOGLE_API_KEY=your_google_ai_studio_api_key

Gmail Configuration (for email functionality)  
GMAIL_USER=your_gmail_address@gmail.com  
GMAIL_APP_PASSWORD=your_gmail_app_password

## Gmail Setup To enable email functionality:

Enable 2-factor authentication on your Gmail account
Generate an App Password:

Go to Google Account settings
Security → 2-Step Verification → App passwords
Generate a password for "Mail"
Use this password as GMAIL_APP_PASSWORD



Usage
Starting the Assistant

Run the assistant with:

``` bash
python agent.py start
```

Console Mode

```bash
python agent.py console
```


# Core Components
Agent (agent.py)

- Main entry point for the LiveKit agent
- Configures the Google Realtime Model with "Aoede" voice
- Sets up noise cancellation and video capabilities
- Manages the agent session lifecycle

Prompts (prompts.py)

- Defines the AI personality as "Friday"
- Sets behavioral guidelines for butler-like responses
- Provides conversation flow instructions

Tools (tools.py)

- Weather Tool: Fetches current weather using wttr.in API
- Search Tool: Performs web searches using DuckDuckGo
- Email Tool: Sends emails through Gmail SMTP

## Personality

Friday is designed to be:

- Professional yet approachable
- Slightly sarcastic but always polite
- Concise in responses (one sentence when possible)
- Acknowledges tasks with phrases like "Will do, Salman" or "Understood Boss"

# Dependencies

Key libraries used:

livekit-agents: Core LiveKit agent functionality  
livekit-plugins-google: Google AI integration  
livekit-plugins-noise-cancellation: Audio enhancement  
langchain_community: Web search capabilities  
requests: HTTP requests for weather API  
python-dotenv: Environment variable management

# Troubleshooting

Common Issues

SSL Certificate Issues:

```bash
Remove-Item Env:SSL_CERT_FILE
```

Authentication Errors:

Verify your LiveKit credentials  
Check Google AI Studio API key  
Ensure Gmail App Password is correct


Audio Issues:

Check microphone permissions  
Verify noise cancellation settings  
Test with console mode first



# Contribution and Acknowledgement  

This open source project is produced by https://github.com/ruxakK/friday_jarvis from https://www.youtube.com/watch?v=An4NwL8QSQ4&ab_channel=Thanh-yDavidNguyen.   
  
However, assistant personality is customized for myself.

