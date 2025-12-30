# SantaQuiz

![Santa Quiz](santa.png)

## Overview

SantaQuiz is a festive Christmas trivia application that generates interactive multiple-choice questions about Christmas folklore and traditions. Powered by AI agents, it creates an engaging holiday quiz experience with a jolly Santa theme.

## Features

- **AI-Powered Question Generation**: Uses CrewAI agents to research Christmas facts and generate dynamic trivia questions
- **Interactive Quiz Format**: Multiple-choice questions with instant feedback
- **Festive Experience**: Hosted by entertaining elf characters with Santa as the judge
- **Multiple Categories**: Generate questions about various Christmas traditions and facts

## How It Works

The application uses three AI agents working together:

1. **Noel Researcher** - Discovers obscure Christmas facts from global traditions
2. **Holly Host** - Transforms facts into engaging multiple-choice questions
3. **Santa Judge** - Validates answers and provides festive feedback

## Technology Stack

- **Framework**: Gradio for the user interface
- **AI/LLM**: IBM Granite model via WatsonX AI
- **Agent Framework**: CrewAI for multi-agent orchestration

## About This Project

This is an **IBM Skills Network Guided Project**. The API credentials were provided within the IBM Skills Network environment for learning purposes.

## Getting Started

### Option 1: Run on IBM Skills Network (Recommended for Learning)

1. Access the project through the IBM Skills Network platform
2. API keys are pre-configured in the environment
3. No additional setup required - just run the application

### Option 2: Clone and Run Locally

#### Prerequisites

- Python 3.x
- Your own IBM WatsonX AI account and API credentials

#### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd SantaQuiz
```

2. Install dependencies:
```bash
pip install gradio crewai
```

3. Set up environment variables (see [API Security](#api-security) section below)

4. Run the application:
```bash
python app.py
```

The application will launch a Gradio interface where you can select Christmas categories and take the festive quiz!

## API Security

⚠️ **Important**: When running locally or deploying, never expose API keys publicly.

### Best Practices

1. **Use Environment Variables**: Store API credentials in `.env` files
   ```bash
   WATSONX_AI_PROJECT_ID=your_project_id_here
   WATSONX_APIKEY=your_api_key_here
   ```

2. **Add `.env` to `.gitignore`**: Prevent accidental commits of sensitive data
   ```
   .env
   .env.local
   *.key
   ```

3. **Use a `.env.example` File**: Provide a template for other developers
   ```bash
   WATSONX_AI_PROJECT_ID=your_project_id_here
   WATSONX_APIKEY=your_api_key_here
   ```

4. **For Production Deployment**:
   - Use secure secret management tools (AWS Secrets Manager, Azure Key Vault, HashiCorp Vault)
   - Implement proper authentication and authorization
   - Use API rate limiting and monitoring
   - Regularly rotate API keys
   - Never hardcode credentials in source code
   - Use separate API keys for development, testing, and production

5. **Additional Security Measures**:
   - Enable API key rotation policies
   - Monitor API usage for unusual activity
   - Use VPCs and firewalls to restrict API access
   - Implement proper logging and auditing


*Spread Christmas cheer and test your holiday knowledge! 🎄🎅*
