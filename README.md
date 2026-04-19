# Blostem Task

[![Next.js](https://img.shields.io/badge/Next.js-16.2.3-black)](https://nextjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.111.0-green)](https://fastapi.tiangolo.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)](https://www.typescriptlang.org/)
[![Python](https://img.shields.io/badge/Python-3.8+-yellow)](https://www.python.org/)

An AI-powered B2B marketing engine designed to streamline lead management, partner nurturing, compliance tracking, and outreach automation. Built with a modern full-stack architecture using Next.js for the frontend and FastAPI for the backend.

## 🚀 Features

- **Lead Management**: AI-driven lead scoring and signal detection for B2B prospects
- **Partner Nurturing**: Automated nudge emails for stalled partners using generative AI
- **Compliance Tracking**: Real-time compliance monitoring and flagging system
- **Outreach Automation**: Personalized outreach campaigns with persona-based targeting
- **Dashboard Analytics**: Comprehensive stats and insights for marketing performance
- **Modern UI**: Responsive interface built with shadcn/ui and Tailwind CSS

## 🛠 Tech Stack

### Frontend
- **Framework**: Next.js 16 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS with shadcn/ui components
- **Icons**: HugeIcons
- **State Management**: React hooks with context

### Backend
- **Framework**: FastAPI
- **Database**: SQLAlchemy with SQLite (configurable)
- **Vector Store**: ChromaDB for embeddings
- **AI Integration**: Google Generative AI, LangChain, LlamaIndex
- **Scheduling**: APScheduler for automated tasks
- **Email**: SendGrid integration
- **PDF Generation**: ReportLab

## 📦 Installation

### Prerequisites
- Node.js 18+ and npm/yarn/pnpm
- Python 3.8+
- Git

### Backend Setup
1. Navigate to the server directory:
   ```bash
   cd server
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   Create a `.env` file in the server directory with:
   ```env
   CORS_ORIGINS=http://localhost:3000
   DATABASE_URL=sqlite:///./test.db
   GOOGLE_API_KEY=your_google_api_key
   SENDGRID_API_KEY=your_sendgrid_api_key
   ```

5. Run the database migrations:
   ```bash
   python seed.py
   ```

6. Start the server:
   ```bash
   uvicorn main:app --reload
   ```

The API will be available at `http://localhost:8000`.

### Frontend Setup
1. Navigate to the client directory:
   ```bash
   cd client
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🏗 Project Structure

```
blostem-task/
├── client/                 # Next.js frontend
│   ├── app/               # App router pages
│   ├── components/        # Reusable UI components
│   ├── lib/               # Utilities and API clients
│   └── types/             # TypeScript type definitions
├── server/                 # FastAPI backend
│   ├── modules/           # Business logic modules
│   │   ├── compliance.py
│   │   ├── nurture.py
│   │   ├── outreach.py
│   │   └── pipeline.py
│   ├── database.py        # Database configuration
│   ├── models.py          # SQLAlchemy models
│   └── main.py            # FastAPI application
└── test_all.py            # Test suite
```

## 🔧 Usage

### API Endpoints
- `GET /leads` - Retrieve all leads with AI scores
- `POST /leads` - Create a new lead
- `GET /partners` - Get partner status and stages
- `POST /nudge` - Generate and queue nudge emails
- `GET /compliance` - Check compliance status

### Development
- Run tests: `python test_all.py`
- Lint frontend: `npm run lint`
- Build for production: `npm run build`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

For questions or support, please open an issue on GitHub.
