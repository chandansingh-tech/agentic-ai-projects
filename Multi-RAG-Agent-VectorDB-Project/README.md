# PDF Assistant - Extracting Knowledge from PDFs

This Python script implements a powerful PDF assistant using the Phi framework. It allows users to interact with and retrieve knowledge from a collection of PDFs.

**Project Highlights**

*   **Phi Framework Integration:** Leverages the Phi framework for building intelligent agents.
*   **PDF Knowledge Base:** Constructs a knowledge base from user-specified PDFs for querying and exploration.
*   **Gemini Text Embedding:** Utilizes Google AI's Gemini model for accurate text embedding.
*   **Interactive Command-Line Interface:** Provides an interactive command-line interface for natural language queries.
*   **PostgreSQL Vector Database:** Stores vector embeddings in a PostgreSQL database with the pgvector extension for efficient similarity searches.

**Installation**

1.  **Prerequisites:**

    *   Python ([https://www.python.org/](https://www.python.org/))
    *   Docker (for PostgreSQL, optional but recommended) ([https://www.docker.com/](https://www.docker.com/))

2.  **Clone the Repository:**

    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

3.  **Create a Virtual Environment:**

    ```bash
    python -m venv .venv  # or python3 -m venv .venv
    source .venv/bin/activate  # Linux/macOS
    .venv\Scripts\activate  # Windows (Command Prompt)
    .venv\Scripts\Activate.ps1 # Windows PowerShell
    ```

4.  **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

    This installs the following packages:

    ```
    phidata
    python-dotenv
    yfinance
    packaging
    duckduckgo-search
    fastapi
    uvicorn
    groq
    openai # May not be directly used in this specific example
    sqlalchemy
    pgvector
    psycopg[binary]
    pypdf
    ```

5.  **Set Environment Variables:**

    *   Create a `.env` file in the project directory.

    *   Add the following lines, replacing placeholders with your actual keys:

        ```
        GROQ_API_KEY=YOUR_GROQ_API_KEY
        GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY
        ```

    *   Load environment variables:

        ```bash
        source .env  # Linux/macOS
        # OR
        setx GROQ_API_KEY "YOUR_GROQ_API_KEY" && setx GOOGLE_API_KEY "YOUR_GOOGLE_API_KEY" # Windows (requires restart or new terminal)
        ```

6.  **Set up PostgreSQL with Docker (Optional but Recommended):**

    ```bash
    docker run -d \
        -e POSTGRES_DB=ai \
        -e POSTGRES_USER=ai \
        -e POSTGRES_PASSWORD=ai \
        -e PGDATA=/var/lib/postgresql/data/pgdata \
        -v pgvolume:/var/lib/postgresql/data \
        -p 5532:5432 \
        --name pgvector \
        phidata/pgvector:16
    ```

    This command sets up a PostgreSQL 16 container with the pgvector extension, database `ai`, user `ai`, password `ai`, and maps port 5532. It also uses a named volume `pgvolume` for persistent data.

**Usage**

1.  **Run the Assistant:**

    ```bash
    python pdf_assistant.py
    ```

2.  **Interact with the Assistant:**

    Use natural language queries to ask questions about the information in the loaded PDF (e.g., "ThaiRecipes.pdf").

**Example Queries**

*   "What ingredients are needed for Pad Thai?"
*   "How do I make Tom Yum soup?"

**Technical Details**

*   `typer`: Used for the command-line interface.
*   `Groq`: Interacts with the Groq API.
*   `PgAgentStorage`: Stores conversation history in PostgreSQL.
*   `PDFUrlKnowledgeBase`: Manages the PDF knowledge base.
*   `PgVector2` and `GeminiEmbedder`: Handle vector storage and embedding.
*   `psycopg[binary]`: PostgreSQL adapter for Python.
*   `pypdf`: Library for PDF manipulation.
*   `sqlalchemy`: Python SQL toolkit and Object Relational Mapper.

**Database Connection String**

The code uses the following connection string (if you're using PostgreSQL):

postgresql+psycopg://ai:ai@localhost:5532/ai

**Future Enhancements**

*   Web interface integration.
*   Support for more document formats.
*   Expanded knowledge base integration.

**Contributing**

Contributions are welcome! Please submit pull requests with improvements or new features.

**License**

This project is licensed under the MIT License. See the LICENSE file for details.