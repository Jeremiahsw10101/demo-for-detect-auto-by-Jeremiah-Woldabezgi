# Demo Project by Jeremiah Woldabezgi

Hi, I’m Jeremiah Woldabezgi. I built this demo for Detect Auto as a way to **show** what I can do instead of just telling you.

Here’s a quick video of the project running live on my laptop:  
▶️ [Watch my demo](https://drive.google.com/file/d/1bVEgzYXkBWF5HWJYjQdMMnfAEWwwUQ3J/view?usp=sharing)

You can visit a live link to the demo online at:

https://repait-ai-powered-chat-fastapi-nextjs-production.up.railway.app

You just need to create a dummy account and login using those credentials to be able to use it.

----------------------------------

# Detect Auto - AI Diagnostic Tool

This is an AI-powered automotive diagnostic tool that helps mechanics and car owners diagnose issues, predict the necessary parts for a repair, and generate repair summaries.

## Key Features

- AI Diagnostic Chatbot
- Smart Parts Predictor
- Repair Order Summarizer
- JWT Authentication (for Accounts/Login)


## Getting Started

## Project Structure

The project is divided into two main parts:

- `/client` - Frontend Next.js application
- `/server` - Backend FastAPI application

### Prerequisites

- Node.js 16+
- Python 3.9+
- PostgreSQL (or use Docker)
- OpenAI API key

### Backend Setup

1. Navigate to the server directory:
   \`\`\`
   cd server
   \`\`\`

2. Create a virtual environment:
   \`\`\`
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   \`\`\`

3. Install dependencies:
   \`\`\`
   pip install -r requirements.txt
   \`\`\`

4. Set environment variables:
   \`\`\`
   export DATABASE_URL=postgresql://postgres:postgres@localhost:5432/detect_auto
   export OPENAI_API_KEY=your_openai_api_key
   \`\`\`

5. Run the server:
   \`\`\`
   uvicorn main:app --reload
   \`\`\`

Alternatively, you can use Docker Compose:
\`\`\`
docker-compose up
\`\`\`

### Frontend Setup

1. Navigate to the client directory:
   \`\`\`
   cd client
   \`\`\`

2. Install dependencies:
   \`\`\`
   npm install
   \`\`\`

3. Set environment variables:
   Create a `.env.local` file with:
   \`\`\`
   NEXT_PUBLIC_API_URL=http://localhost:8000
   \`\`\`

4. Run the development server:
   \`\`\`
   npm run dev
   \`\`\`

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## API Documentation

Once the backend is running, you can access the API documentation at:
- Swagger UI: [http://localhost:8000/docs](http://localhost:8000/docs)
- ReDoc: [http://localhost:8000/redoc](http://localhost:8000/redoc)

## Database Schema

The application uses the following database schema:

- `users` - User accounts
- `sessions` - Diagnostic sessions
- `diagnostic_results` - Results from AI diagnostics
- `part_predictions` - Predicted parts for repairs
- `repair_notes` - Additional notes for repairs
- `repair_summaries` - Generated repair summaries

## License

This project is licensed under the MIT License.
