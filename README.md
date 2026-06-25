# MediFlow AI: Healthcare Referral Management Platform

**Full-stack AI-powered healthcare referral management system** with OCR, speech-to-text transcription, DICOM imaging, and real-time clinical workflows.

## 🎥 Demo Video

Watch the full project demonstration:

[![MediFlow AI Demo](https://img.shields.io/badge/Watch_Full_Demo-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://www.youtube.com/watch?v=RgBazufVYEQ)

> *Click the button above or the image to watch the demo video on Google Drive.*

## ✨ Features

- **AI-Powered Referral Management** — Intelligent handling of patient referrals
- **OCR (Optical Character Recognition)** — Extract text from medical documents and faxes
- **Speech-to-Text Transcription** — Convert doctor notes and consultations into structured data
- **DICOM Imaging Support** — View and manage medical images
- **Real-time Clinical Workflows** — Live updates and collaboration between healthcare providers
- **Full-stack Architecture** — Modern backend + responsive frontend

## 📁 Repositories

- **Backend**: [mediflow_backend](https://github.com/paulathejennifer/mediflow_backend)
- **Frontend**: [mediflow_frontend](https://github.com/paulathejennifer/mediflow_frontend)

**Here is the complete, ready-to-paste Markdown** for your README:

```markdown
## 🛠 Tech Stack

### Frontend
- **Next.js 15** (App Router)
- **Tailwind CSS**
- **Zustand** (State Management)
- **Recharts** (Analytics & Charts)
- **Lucide React** (Icons)
- **Sonner & React Hot Toast** (Notifications)

### Backend
- **FastAPI** (High-performance Python framework)
- **SQLAlchemy** (ORM)
- **PostgreSQL** (Database)
- **Pydantic** (Data validation)
- **Alembic** (Database migrations)

### AI & Infrastructure
- **Groq Cloud** (Llama 3.1 8B) — Clinical summaries and quality scoring
- **Google Speech Recognition** — Speech-to-text
- **Backblaze B2** (S3-compatible) — Secure document storage
- **WebSockets** — Real-time notifications

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- Python 3.11 or higher
- PostgreSQL (local or hosted)
- Git

### Backend Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/paulathejennifer/mediflow_backend.git
   cd mediflow_backend
   ```

2. **Create and activate virtual environment**
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate

   # macOS / Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**  
   Create a `.env` file in the root of the `mediflow_backend` directory and paste the following:

   ```env
   ENVIRONMENT=development
   SECRET_KEY=your_super_secret_key_here

   # Database
   DATABASE_URL=postgresql://mediflow_user:mediflow_password@localhost:5432/mediflow_db

   # AI
   GROQ_API_KEY=your_groq_api_key_here

   # Backblaze B2 (S3-compatible)
   AWS_ACCESS_KEY_ID=your_backblaze_key_id_here
   AWS_SECRET_ACCESS_KEY=your_backblaze_application_key_here
   S3_BUCKET_NAME=your_bucket_name_here
   S3_ENDPOINT_URL=https://s3.us-west-004.backblazeb2.com   # Update with your actual region

   # Frontend URL (for CORS)
   FRONTEND_URL=http://localhost:3000
   ```

5. **Run database migrations**
   ```bash
   alembic upgrade head
   ```

6. **Start the development server**
   ```bash
   uvicorn app.main:app --reload
   ```

   The backend API will be available at `http://localhost:8000`  
   Swagger UI: `http://localhost:8000/docs`

### Frontend Setup

```bash
cd ../mediflow_frontend
npm install
npm run dev
```

```
