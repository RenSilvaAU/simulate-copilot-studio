# Banking Chatbot Simulator

This repository contains a Jupyter Notebook that simulates interactions with a banking chatbot to resolve various queries. It uses two main classes:

- **CopilotStudioBot**: Handles starting a conversation, sending questions, and receiving responses.  
- **UserSimulator**: Generates user questions and simulates user interactions using the Azure OpenAI service.

## Getting Started

1. **Prerequisites**  
   - Ensure Docker is running on your machine.  
   - If on macOS with Apple Silicon, make sure Rosetta is installed and enabled.  
   - Use a compatible IDE (e.g., VS Code) with Remote - Containers or Dev Containers enabled.

2. **Environment Variables**  
   - Copy `.env-template` to `.env` and set the following variables:
     ```
     AZURE_OPENAI_API_KEY=<YOUR KEY>
     AZURE_OPENAI_ENDPOINT="https://<BASE_NAME>.cognitiveservices.azure.com"
     AZURE_OPENAI_API_VERSION=2024-06-01
     AZURE_OPENAI_DEPLOYMENT=gpt-4o-mini
     BOT_NAME=<CoPilot Studio Bot Name>
     ENV_NAME=<CoPilot Studio Environment Name>
     ```
   - Make sure you have the Azure OpenAI service and Copilot Studio set up.

3. **Running the Notebook**  
   - Open the `.devcontainer` folder in VS Code and reopen in a container.  
   - Launch the notebook (`1-simulate.ipynb`).  
   - Run each cell in order to simulate banking-related conversations.

## How It Works

1. **Conversation Simulation**  
   - Each cell includes a question, and the chatbot responds via the `CopilotStudioBot` class.  
   - The `UserSimulator` determines the next user query based on the chatbot’s response.

2. **Result Tracking**  
   - The code tracks whether the user’s query was successfully answered or if it needs human escalation.

## Contributing

Feel free to open issues or submit pull requests for improvements. Make sure Docker and the dev container setup are properly configured before starting development.