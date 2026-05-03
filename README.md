GoldenHour AI
90 Seconds. One Message. A Life Saved.
Road Safety Hackathon 2026 – BIMSTEC Countries Organised by IIT Madras – CoERS | Track: RoadSoS | Team: The Encoder

🧠 What is GoldenHour AI?
GoldenHour AI is a multi-agent AI emergency coordination system triggered by a single WhatsApp message, SMS, or voice call — requiring zero app installation.

When someone witnesses a road accident, they message GoldenHour AI. Within 90 seconds, the system simultaneously:

🚑 Dispatches the nearest capable ambulance
🏥 Pre-alerts the hospital ER with patient details
🗣️ Guides the bystander through CPR in their local language
👨‍👩‍👧 Notifies the victim's family via vehicle registration lookup
📋 Auto-generates a legal-grade incident report for police + insurance
No app. No training. No infrastructure. Just one number to message.

💀 The Problem
Metric	Reality
Annual road deaths in BIMSTEC	~3,00,000
Golden Hour compliance (rural)	< 15%
Avg ambulance response (tier-2)	45 minutes
112 call center hold time	4–8 minutes
Bystanders who know CPR	< 11%
50%+ of road deaths are preventable if reached within the Golden Hour.
Current systems are single-channel, uncoordinated, and leave bystanders helpless.

⚡ How It Works
Bystander texts "accident on NH-44, 2 injured, one not breathing"
        ↓
GoldenHour AI receives message (WhatsApp / SMS / Voice)
        ↓
LLM Orchestrator triages severity → extracts location → routes tasks
        ↓ (all parallel, < 90 seconds)
        
┌─────────────────────────────────────────────────────┐
│  GeoAgent      → Validates GPS coordinates          │
│  DispatchAgent → Alerts nearest ambulance via SMS   │
│  HospitalAgent → Pre-alerts ER with ETA + severity  │
│  GuideAgent    → Sends CPR audio in local language  │
│  FamilyAgent   → Notifies kin via vehicle reg       │
│  ReportAgent   → Generates FIR + insurance PDF      │
└─────────────────────────────────────────────────────┘

        ↓
        
Bystander gets live ETA updates
Hospital activates trauma team BEFORE ambulance arrives
🤖 AI Architecture
INPUT LAYER
├── WhatsApp (Twilio / Meta Cloud API)
├── SMS / USSD (feature phones, rural BIMSTEC)
├── Voice call (Twilio Voice + Whisper STT)
└── Photo (GPT-4o Vision → severity score)


ORCHESTRATOR
└── Claude claude-sonnet-4-20250514 (Anthropic)
    ├── Triage: fragmented text → structured JSON
    ├── RAG: ChromaDB + WHO/Red Cross first-aid docs
    └── Fallback: rule-based classifier if API > 3s
    

SPECIALIST AGENTS (Celery parallel tasks)
├── GeoAgent       → Google Maps Geocoding API
├── DispatchAgent  → Ambulance DB + Twilio SMS
├── HospitalAgent  → ER capacity check + webhook
├── GuideAgent     → CPR TTS (gTTS / ElevenLabs)
├── FamilyAgent    → Vehicle reg lookup + SMS
└── ReportAgent    → ReportLab PDF generation



🧱 Tech Stack
Layer	Technology
LLM	Claude claude-sonnet-4-20250514 (Anthropic)
Backend	FastAPI + Celery + Redis
Database	PostgreSQL (SQLAlchemy ORM)
Vector DB	ChromaDB (RAG for first-aid protocols)
Messaging	Twilio WhatsApp + Voice + SMS
Maps	Google Maps Geocoding + Routes API
STT	OpenAI Whisper
TTS	gTTS / ElevenLabs
Frontend	React + Tailwind CSS (hospital dashboard)
Deploy	Railway.app + Cloudflare


📁 Project Structure

goldenhour-ai/
├── backend/
│   ├── main.py                  # FastAPI app + webhook endpoints
│   ├── agents/
│   │   ├── orchestrator.py      # LLM triage + task routing
│   │   ├── dispatch_agent.py    # Ambulance alert logic
│   │   ├── hospital_agent.py    # ER pre-alert + capacity check
│   │   ├── guide_agent.py       # CPR instruction loop + TTS
│   │   ├── family_agent.py      # Vehicle reg + kin notification
│   │   └── report_agent.py      # Incident PDF generation
│   ├── integrations/
│   │   ├── twilio_client.py     # WhatsApp + Voice + SMS
│   │   ├── maps_client.py       # Google Maps geocoding
│   │   └── llm_client.py        # Anthropic + OpenAI wrapper
│   ├── rag/
│   │   ├── ingest.py            # PDF chunking + embedding
│   │   ├── retriever.py         # ChromaDB vector query
│   │   └── data/                # WHO/Red Cross first-aid PDFs
│   ├── db/
│   │   ├── models.py            # Incident, Hospital, Ambulance
│   │   └── seed.py              # 20 hospitals, 10 ambulances
│   └── config.py
├── frontend/
│   ├── dashboard/               # React hospital admin view
│   └── demo/                    # Public demo page
├── docker-compose.yml
├── requirements.txt
└── README.md


MIT License — open for research and non-commercial safety use.
