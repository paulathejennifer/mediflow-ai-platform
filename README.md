# MediFlow AI: Intelligent Healthcare Referral Platform

MediFlow AI is a full-stack, AI-powered healthcare referral management platform designed to digitize and optimize patient referrals across healthcare facilities.

Built with **Next.js, FastAPI, PostgreSQL, and modern AI services**, MediFlow transforms fragmented, paper-based referral workflows into a centralized, real-time clinical collaboration platform. The system combines OCR, speech-to-text transcription, AI-assisted clinical summarization, intelligent duplicate detection, real-time notifications, and referral analytics to reduce administrative overhead while improving referral visibility and continuity of care.

Rather than replacing clinicians, MediFlow augments clinical workflows by automating repetitive administrative tasks while preserving clinician oversight and auditability throughout the referral lifecycle.

## 🎥 Demo Video

Watch the full project demonstration:

[![MediFlow AI Demo](https://img.shields.io/badge/Watch_Full_Demo-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1_wYbJPWEES41D3lyRa17OiexM3o0Wnu7/view?usp=sharing)

> *Click the button above or the image to watch the demo video on Google Drive.*

---

# 🏗️ System Architecture

Explore the high-level architecture behind MediFlow, including the AI pipeline, backend services, authentication, storage, and interoperability design.

📄 **Architecture Diagram:**
**[CLICK HERE](https://drive.google.com/file/d/1mwdPeysiQDE0mySE-HnOOjAblZJLlP1_/view?usp=drive_link)**

---

# 🔄 User Workflow

This diagram illustrates the complete patient referral lifecycle, from patient registration through AI-assisted referral creation, facility review, and referral tracking.

📄 **Workflow Diagram:**
**[CLICK_HERE](https://drive.google.com/file/d/1LtPnJHd21DneT0-DSfvqnip9J5MEPtKS/view?usp=drive_link)**

## ✨ Features

* **AI-Assisted Clinical Referrals** — Create, manage, and track referrals across multiple healthcare facilities.
* **Intelligent OCR Pipeline** — Extract structured clinical information from scanned referral letters, laboratory reports, and medical documents.
* **Speech-to-Text Clinical Notes** — Convert clinician voice recordings into structured referral documentation.
* **AI Clinical Summarization** — Automatically generate concise referral summaries, identify key findings, assess referral completeness, and classify medical specialties.
* **Duplicate Patient Detection** — Hybrid TF-IDF and fuzzy matching to reduce duplicate patient records.
* **Real-Time Referral Tracking** — Live referral status updates and WebSocket-powered notifications.
* **Role-Based Access Control (RBAC)** — Separate workflows for Super Admins, Facility Administrators, and Clinicians.
* **Referral Analytics Dashboard** — Monitor referral trends, specialty distribution, facility performance, and operational KPIs.
* **Audit Trail & Activity Timeline** — Complete referral lifecycle tracking for accountability and traceability.
* **DICOM Imaging Support** — Manage and view diagnostic medical images alongside referral records.
* **Cloud Document Storage** — Secure storage and retrieval of clinical documents and attachments.
* **FHIR-Ready Modular Architecture** — Designed to support healthcare interoperability and future integration with external health information systems.
* **Modern Full-Stack Architecture** — FastAPI, PostgreSQL, Next.js, Tailwind CSS, asynchronous AI pipelines, and modular backend services.


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
- **AWS** (S3-compatible) — Secure document storage
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
<img width="1365" height="676" alt="Screenshot 2026-06-26 011025" src="https://github.com/user-attachments/assets/36b8d189-a54b-4f39-8171-b5b58620401f" />
<img width="1365" height="681" alt="Screenshot 2026-06-26 010954" src="https://github.com/user-attachments/assets/9e89de09-39c7-48be-bddf-5af158b496a3" />
<img width="1365" height="678" alt="Screenshot 2026-06-26 010936" src="https://github.com/user-attachments/assets/126a2c5d-9e5c-4adb-878d-ca304f66a352" />
<img width="1365" height="680" alt="Screenshot 2026-06-26 010918" src="https://github.com/user-attachments/assets/b75aa840-9c96-4c42-8c3b-d92d4901e433" />
<img width="1365" height="682" alt="Screenshot 2026-06-26 011317" src="https://github.com/user-attachments/assets/20603913-4a08-4faf-a22f-01ad071244df" />
<img width="1365" height="680" alt="Screenshot 2026-06-26 011308" src="https://github.com/user-attachments/assets/3a980f97-090c-49cd-aefd-89205c368ea0" />
<img width="1365" height="680" alt="Screenshot 2026-06-26 011308 - Copy" src="https://github.com/user-attachments/assets/4ed9cb9e-cde4-4167-bf30-085c076ba3e2" />
<img width="1365" height="669" alt="Screenshot 2026-06-26 011241" src="https://github.com/user-attachments/assets/470930dd-28ea-4487-a156-2ebcc003ab3c" />
<img width="1365" height="680" alt="Screenshot 2026-06-26 011225" src="https://github.com/user-attachments/assets/8c8463a8-ed75-462f-bc1c-cfeebfb71506" />
<img width="1365" height="679" alt="Screenshot 2026-06-26 011214" src="https://github.com/user-attachments/assets/0b080aa2-8287-4110-92f0-5b665132d40d" />
<img width="1365" height="681" alt="Screenshot 2026-06-26 011155" src="https://github.com/user-attachments/assets/b66d5d7e-1f44-4d1c-a6f2-46062e5c25e4" />
<img width="1365" height="682" alt="Screenshot 2026-06-26 011144" src="https://github.com/user-attachments/assets/70f10efc-b59a-4543-aa42-f980f0ce405c" />
<img width="1365" height="681" alt="Screenshot 2026-06-26 011122" src="https://github.com/user-attachments/assets/681e5391-3d00-4558-a54f-412edf091b11" />
<img width="1355" height="678" alt="Screenshot 2026-06-26 011047" src="https://github.com/user-attachments/assets/8b0029f3-b5c0-454f-ab3e-cf4014b8d347" />
<img width="1365" height="678" alt="Screenshot 2026-06-25 105557" src="https://github.com/user-attachments/assets/ae1d0c6b-08f3-49c1-a243-f9f074ef50c8" />
<img width="1361" height="675" alt="Screenshot 2026-06-26 010900" src="https://github.com/user-attachments/assets/f48bbde2-3ed1-44ae-90b1-4175ceb7214f" />
<img width="1365" height="678" alt="Screenshot 2026-06-25 105557" src="https://github.com/user-attachments/assets/62ea3735-74d4-4e85-99ce-728829b2436f" />
```
