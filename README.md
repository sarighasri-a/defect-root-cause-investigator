# Defect Detective Assistant - AI ROOT CAUSE INVESTIGATOR

**Defect Detective Assistant** is a high-end RAG (Retrieval-Augmented Generation) assistant designed for **Discrete Manufacturing**. It investigates the root causes of production defects (like silver streaks, chatter marks, or porosity) and correlates them with process parameter deviations.

## Features
- **Defect Detective Assistant**: A fully responsive, high-fidelity UI that works on both Desktop and Mobile.
- **RAG-Powered Diagnostics**: Utilizes LangChain, ChromaDB, and OpenAI to retrieve accurate engineering data.
- **Cross-Vertical Knowledge Base**:
    - **Injection Molding**: Surface burns, short shots, sink marks.
    - **CNC Machining**: Chatter marks, built-up edge (BUE).
    - **Welding (MIG/TIG)**: Porosity, undercut, spatter.
    - **Stamping**: Wrinkling, springback, cracking.
    - **PCB Manufacturing**: Solder bridging, delamination, over-etching, drill offset.
- **Quick-Access Chips**: One-click tags for common investigations.
- **Branding**: "Build with Sarighasri" signature.

## Project Structure
- `app.py`: FastAPI backend and RAG logic.
- `ingest.py`: Script to process and index the manufacturing knowledge base (`data/`).
- `index.html`: Premium "Defect Detective Assistant" dashboard (HTML/CSS/JS).
- `data/`: Directory containing Markdown-based manufacturing SOPs and defect catalogs.
- `vector_db/`: Persistent ChromaDB store.

## Installation & Setup

### 1. Prerequisites
- Python 3.9+
- OpenAI API Key (Stored in `.env` file)

### 2. Create and Activate a Virtual Environment
It is recommended to use a virtual environment to manage dependencies:
**Windows:**
```bash
python -m venv .venv
.\.venv\Scripts\activate
```
**macOS/Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables
Create a `.env` file in the root directory (if not already present) and add your OpenAI API key:
```env
OPENAI_API_KEY="your-api-key-here"
```

### 5. Ingest Data
Before running the application, you must process and index the manufacturing knowledge base into the vector database. Run the ingestion script:
```bash
python ingest.py
```

### 6. Launch the Server
Start the FastAPI application server:
```bash
python app.py
```
The Defect Detective Assistant will be live and ready to use in your browser at:
👉 **[http://0.0.0.0:8080](http://localhost:8080)**

---
**Build with Sarighasri**
