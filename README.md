# AI News Hub

A full-stack web application that works like a simplified version of Google News, but exclusively for AI-related news.

## Overview

AI News Hub aggregates AI-related articles from trusted sources, processes them to extract key information, categorizes them, clusters similar articles together, and presents them in a clean, intuitive interface.

## Features

- Collects AI news from trusted sources
- Processes and summarizes articles using GPT
- Categorizes articles into predefined categories
- Clusters similar articles using semantic similarity
- Provides semantic search functionality
- Allows users to set preferences for personalized feeds
- Clean, responsive frontend interface

## Tech Stack

### Frontend
- React with TypeScript
- React Router for navigation
- TailwindCSS for styling
- Context API for state management

### Backend
- FastAPI (Python)
- JSON-based storage (can be extended to use a database)

## Project Structure

```
/
├── src/                  # Frontend source code
│   ├── components/       # React components
│   ├── context/          # React context providers
│   ├── pages/            # Page components
│   ├── mocks/            # Mock data
│   ├── types/            # TypeScript type definitions
│   ├── App.tsx           # Main application component
│   └── main.tsx          # Entry point
│
├── backend/              # Backend source code
│   ├── server.py         # FastAPI server
│   ├── requirements.txt  # Python dependencies
│   └── README.md         # Backend documentation
│
├── public/               # Static assets
├── README.md             # Project documentation
└── package.json          # Node.js dependencies
```

## Setup Instructions

### Frontend

1. Install dependencies:
   ```bash
   npm install
   ```

2. Start the development server:
   ```bash
   npm run dev
   ```

3. The frontend will be available at http://localhost:5173

### Backend

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Start the backend server:
   ```bash
   python server.py
   ```

4. The API will be available at http://localhost:8000
   
5. Seed the database with example data by making a POST request to:
   ```
   POST http://localhost:8000/admin/seed
   ```
   
   You can use curl or another API client:
   ```bash
   curl -X POST http://localhost:8000/admin/seed
   ```

## Development Roadmap

### Phase 1 (Current)
- Basic frontend with mock data
- Simple backend API endpoints

### Phase 2
- Integrate RSS feed collection
- Implement article processing and summarization with GPT
- Add semantic clustering for similar articles

### Phase 3
- Add user authentication
- Implement vector search for semantic queries
- Create automated article collection pipeline

## License

MIT