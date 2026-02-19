# PocketPaw Clone - Getting Started

Welcome to your self-hosted AI Agent Platform!

## 🚀 Quick Start

### Prerequisites
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Node.js 18+](https://nodejs.org/) (for local dev)
- [Python 3.10+](https://www.python.org/) (for local dev)

### 🐳 Run with Docker (Recommended)

1.  **Configure Environment**:
    Rename `.env.example` (if exists) or create `.env` in the root directory.
    ```env
    OPENAI_API_KEY=sk-...
    # Other keys removed as we are OpenAI only
    ```

2.  **Start Services**:
    ```bash
    docker-compose up --build
    ```

3.  **Access App**:
    - Frontend: [http://localhost:5173](http://localhost:5173)
    - Backend API: [http://localhost:8000/docs](http://localhost:8000/docs)

### 🛠️ Local Development

#### Backend
1.  Navigate to `backend`:
    ```bash
    cd backend
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run Server:
    ```bash
    uvicorn app.main:app --reload
    ```

#### Frontend
1.  Navigate to `frontend`:
    ```bash
    cd frontend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Run Dev Server:
    ```bash
    npm run dev
    ```

## 🌟 Features

- **AI Chat Engine**: Exclusive integration with OpenAI (GPT-4o-mini) for high-quality responses.
- **Conversation History**: Persist your chats, create new topics, and manage history.
- **Agent Tools**: 
    - **Web Search**: DuckDuckGo integration.
    - **Calculator**: Math evaluation.
    - **Website Reader**: Extract content from URLs.
    - **File Reader**: Support for PDF, DOCX, and TXT files.
    - **Notes & Reminders**: Built-in management for personal data.
- **Memory System**: Hybrid SQL + Vector (ChromaDB) memory for long-term recall.
- **Safety Layer**: Guardrails for risky content and action logging.
- **Admin Panel**: Manage users (superusers only).

## 📝 Usage

1.  **Register/Login** to access the dashboard.
2.  **Chat**: Start talking to the AI. It remembers previous messages in the thread.
3.  **Tools**: 
    - "Search for latest AI news" -> Uses Web Search.
    - "Read this page: https://example.com" -> Uses Website Reader.
    - "Calculate 25 * 4" -> Uses Calculator.
    - "Read file /path/to/doc.pdf" -> Uses File Reader.
    - "Take a note about..." -> Uses Notes Tool.
    - "Set a reminder to..." -> Uses Reminder Tool.
4.  **Manage Data**: Use the sidebar to switch conversations.
"# web-project" 
