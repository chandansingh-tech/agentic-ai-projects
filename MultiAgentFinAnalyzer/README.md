# MultiAgentFinAnalyzer

This project implements a multi-agent system for financial analysis using the PHI library. It combines the capabilities of two agents:

*   **Finance AI Agent:** Analyzes financial data using YFinance.
*   **Web Search Agent:** Searches the web for relevant information using DuckDuckGo.

The user interacts with the application through either a console command or a web interface.

### Features

*   **Stock Analysis:** Retrieve stock price, analyst recommendations, fundamentals, and company news.
*   **Web Search Integration:** Search for additional information related to the analyzed stock.
*   **Multi-Agent Collaboration:** Agents work together to provide a comprehensive analysis.
*   **User-Friendly Output:** Data is presented in clear and concise tables (markdown format).

### Requirements

This project requires the following Python packages:
    phidata
    python-dotenv
    yfinance
    packaging
    duckduckgo-search
    fastapi
    uvicorn
    groq

You can install these using pip:
    pip install -r requirements.txt

Usage

1. Console Application (financial_analysis_agent.py):

This script demonstrates how to use the agents directly from the console.

    Steps:

    1. Clone the repository:
        https://github.com/chandansingh-tech/agentic-ai-projects.git

    2. Navigate to the project directory:
        cd agentic-ai-projects/MultiAgentFinAnalyzer

    3. Create a virtual environment (recommended: Python 3.x):

        python -m venv .venv  # or python3 -m venv .venv

    4. Activate the virtual environment:

        source .venv/bin/activate  # Linux/macOS
        .venv\Scripts\activate      # Windows (Command Prompt)
        .venv\Scripts\Activate.ps1   # Windows PowerShell

    5. Install dependencies:

        pip install -r requirements.txt

    6. Create a .env file in the MultiAgentFinAnalyzer directory with directory with your Groq and PHI API keys:

        GROQ_API_KEY=<your_groq_api_key>
        PHI_API_KEY=<your_phi_api_key>

    7. Run the script from the console:
        python financial_analysis_agent.py

2. Web Application (playground.py):

This script defines a web application using the PHI Playground framework. You can deploy this to a platform like Phidata for a user interface.

    Steps:

    1. Clone the repository:

        https://github.com/chandansingh-tech/agentic-ai-projects.git
    
    2. Navigate to the project directory:

        cd agentic-ai-projects/MultiAgentFinAnalyzer
        
    3. Create a virtual environment (recommended: Python 3.12):

        python -m venv .venv  # or python3 -m venv .venv
    
    4. Activate the virtual environment:

    source .venv/bin/activate  # Linux/macOS
    .venv\Scripts\activate      # Windows (Command Prompt)
    .venv\Scripts\Activate.ps1   # Windows PowerShell
    
    5. Install dependencies:

        pip install -r requirements.txt
    
    6. Create a .env file in the MultiAgentFinAnalyzer directory with your Groq and PHI API keys:

        GROQ_API_KEY=<your_groq_api_key>
        PHI_API_KEY=<your_phi_api_key>
        

    7. Run the script to from console:
        python playground.py

        This will start a local server running the web application. 
        Post execution, Phidata will likely assign a unique URL to your application. Note down this URL for the next step. (usually at http://localhost:7777).

3. Using the Web Application on Phidata:

    1. Login to your Phidata account.
    2. Navigate to the Playground section.
    3. Select your deployed endpoint (which should include the URL assigned by Phidata, likely in the format http://localhost:7777).
    4. In the text area, enter your query using the same syntax as the console application (e.g., "Summarize analyst recommendation and share the latest news for TESLA").
    5. Click "Run" to trigger the analysis and display the results on the page.
    
    Note: The specific deployment steps for Phidata might vary depending on their platform version. Refer to their documentation for detailed instructions

    Technologies Used:
    PHI Library
    YFinance (financial data)
    DuckDuckGo (web search)
    Groq
    uvicorn
    fastapi

    Contributing
    We welcome contributions to this project. Feel free to submit pull requests with improvements or new features.

    License
    This project is licensed under the MIT License. See the LICENSE file for details.





