# Multimodal AI Agent: Video Summarizer with Streamlit 🎥

This project showcases a powerful video summarization tool built using the Phi framework and Streamlit. It leverages the capabilities of a multimodal AI agent to extract insights from uploaded videos and answer your questions in a comprehensive and informative way.

**Key Features:**

*   **Video Summarization:** Analyzes video content using the state-of-the-art Gemini 2.0 Flash Exp model from Google AI.
*   **Natural Language Interface:** Ask questions about the video in plain English, and the agent will provide summaries tailored to your specific queries.
*   **Web-Based Interface:** Streamlit creates a user-friendly interface for uploading videos, entering questions, and viewing the analysis results.
*   **Contextual Enrichment:** The agent can go beyond the video itself, using DuckDuckGo to search for relevant web information and enrich the summaries.
*   **Actionable Insights:** The summaries are designed to be actionable, providing key takeaways and valuable information from the video content.

**Getting Started**

1.  **Prerequisites:**
    *   Python 3.6 or later
    *   A Google Cloud account with a project enabled for the Google Generative AI API ([invalid URL removed])
2.  **Installation:**
    *   Clone this repository.
    *   Create a virtual environment and activate it (recommended).
    *   Install project dependencies:

    **requirements.txt**
        phidata
        python-dotenv
        yfinance
        packaging
        duckduckgo-search
        fastapi
        uvicorn
        groq
        openai
        sqlalchemy
        pgvector
        psycopg[binary]
        pypdf
        streamlit
        google-generativeai
        duckduckgo-search

        ```bash
        pip install -r requirements.txt
        ```

3.  **Set Up Google Cloud Project:**
    *   Create a Google Cloud project and enable the Generative AI API.
    *   Obtain an API key and store it in a `.env` file using the variable name `GOOGLE_API_KEY`.
4.  **Run the Application:**
    *   Execute:

        ```bash
        streamlit run video_summerizer_multi-rag-gemini-agent.py
        ```

**Using the Video Summarizer**

1.  Open http://localhost:8501/ in your web browser.
2.  Click "Upload a video file" and select a video in MP4, MOV, or AVI format.
3.  Enter your question or desired insights in the text area below the video. Be specific about what you want to learn from the video.
4.  Click the "🔍 Analyze Video" button.
5.  The application will process the video and generate a summary based on your query. The summary may include insights from the video itself, supplemented by relevant web information retrieved through DuckDuckGo.

**Technical Stack**

*   **Phi Framework:** Provides the foundation for building the multimodal AI agent.
*   **Streamlit:** Creates the user-friendly web interface for interacting with the video summarizer.
*   **Gemini 2.0 Flash Exp (Google AI):** The core AI model for video content analysis and text generation.
*   **DuckDuckGo:** Web search engine used to gather additional context for the summaries.
*   **Google Generative AI:** Enables video processing and analysis using Google Cloud.
*   **python-dotenv:** Manages environment variables for the Google API key.

**Further Enhancements**

*   Integrate additional AI models for different video analysis tasks (e.g., object detection, sentiment analysis).
*   Implement advanced summarization techniques to provide concise and informative summaries.
*   Allow users to specify the desired length or format of the summaries.
*   Explore visualization techniques to present the video analysis results in a more engaging way.

**Disclaimer**

This project is for educational and demonstration purposes only. The accuracy and completeness of the video summaries may vary depending on the video content and the user's queries.

We welcome your contributions to this project! Feel free to submit pull requests with improvements or new features.

