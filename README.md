<div align="center">

# 🚑 GoldenHour AI

## **Every second after a road crash, someone is dying for lack of coordination.**
### GoldenHour AI fixes that — with one WhatsApp message, in under 90 seconds.

<br/>

[![Built For](https://img.shields.io/badge/Built%20For-Road%20Safety%20Hackathon%202026-orange?style=for-the-badge)](https://github.com/pandeylakshya207-max/goldenhour-ai)
[![Powered By](https://img.shields.io/badge/Powered%20By-Claude%20Sonnet%204-blueviolet?style=for-the-badge&logo=anthropic)](https://anthropic.com)
[![Response Time](https://img.shields.io/badge/Response%20Time-%3C%2090%20Seconds-brightgreen?style=for-the-badge)](#)
[![Zero Install](https://img.shields.io/badge/App%20Install-Zero%20Required-blue?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/pandeylakshya207-max/goldenhour-ai?style=for-the-badge&color=yellow)](https://github.com/pandeylakshya207-max/goldenhour-ai/stargazers)

<br/>

🏆 **Road Safety Hackathon 2026 — BIMSTEC Countries**  
Organised by **IIT Madras – CoERS** &nbsp;|&nbsp; Track: **RoadSoS** &nbsp;|&nbsp; Team: **The Encoder**

<br/>

> *"The ambulance isn't too slow. The coordination is."*

</div>

---

## 🩸 The Problem

**300,000 people die on BIMSTEC roads every year.**  
Not because we lack ambulances. Not because hospitals aren't equipped.  
Because **the first 90 seconds are chaos** — and no system coordinates what happens in them.

| Reality Check | Number |
|---|---|
| Annual road deaths, BIMSTEC | **~3,00,000** |
| Golden Hour compliance in rural areas | **< 15%** |
| Avg ambulance response, Tier-2 cities | **45 min** |
| 112 call center hold time | **4–8 min** |
| Bystanders trained in CPR | **< 11%** |

**50%+ of these deaths are preventable** — if the right help is triggered in the right order within the first hour.  
Every existing system does one thing. No system does all five. Until now.

---

## 💡 The Solution

**GoldenHour AI** is a multi-agent AI emergency coordination system that activates the entire response chain — ambulance, hospital ER, CPR guidance, family notification, and legal documentation — from a **single WhatsApp message, SMS, or voice call**.

No app. No training. No smartphone required. Just one number to message.

**Real incident simulation:**
> A truck driver on NH-44 at 2 AM texts: *"accident near milestone 114, 2 injured, one unconscious"*  
> Within 90 seconds: ambulance dispatched → ER pre-alerted with severity data → family notified via vehicle registration → CPR audio delivered in Hindi → FIR PDF generated.  
> The hospital trauma team is ready **before the ambulance arrives**.

---

## 🌍 The Impact

| Without GoldenHour AI | With GoldenHour AI |
|---|---|
| Bystander calls 112, waits on hold | One WhatsApp message triggers everything |
| Ambulance dispatched, hospital unaware | Hospital ER pre-alerted with ETA + severity |
| Bystander watches helplessly | CPR audio guide in their language, immediately |
| Family learns hours later | Family notified via vehicle reg in < 90s |
| Paperwork filed days later | FIR + insurance PDF auto-generated at scene |

> **This system doesn't replace emergency services. It makes them 10x faster to coordinate.**

---

## ✨ Features

| | Feature | What it does |
|---|---|---|
| 🚀 | **Zero-Install Access** | Works on WhatsApp, SMS, USSD, voice — any phone, anywhere |
| 🧠 | **AI Triage Engine** | Claude Sonnet 4 parses panicked, fragmented text into structured emergency JSON |
| ⚡ | **6 Parallel Agents** | Dispatch, hospital, CPR, family, geo, and report agents fire simultaneously — not sequentially |
| 🗣️ | **Multilingual CPR Audio** | Real-time voice instructions in 10+ languages: Hindi, Bengali, Tamil, Sinhala, Thai... |
| 🏥 | **Hospital Pre-Alert** | ER trauma team activates *before* the ambulance arrives |
| 👨‍👩‍👧 | **Family Notification** | Auto-identifies next of kin via vehicle registration — no contact needed |
| 📋 | **Legal Incident Report** | FIR + insurance PDF auto-generated at time of incident |
| 📸 | **Photo Severity Scoring** | GPT-4o Vision estimates injury severity from a crash photo |
| 🔁 | **Fallback Resilience** | Rule-based classifier activates if LLM latency exceeds 3s |
| 📡 | **Feature Phone Support** | USSD + SMS path for rural areas with no smartphones |

---

## 🧠 How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│  STEP 1 — Bystander sends one message                           │
│  "accident on NH-44, 2 injured, one not breathing"              │
│  via WhatsApp / SMS / Voice / Photo                             │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  STEP 2 — LLM Orchestrator (Claude Sonnet 4)                    │
│  • Parses broken text → structured severity JSON                │
│  • Scores severity 1–5                                          │
│  • RAG lookup against WHO / Red Cross first-aid docs            │
│  • Routes tasks to all 6 agents in parallel                     │
└──────────────────────────┬──────────────────────────────────────┘
                           │
         ┌─────────────────┼─────────────────┐
         │                 │                 │
         ▼                 ▼                 ▼
┌──────────────┐  ┌────────────────┐  ┌──────────────────┐
│  STEP 3      │  │  STEP 4        │  │  STEP 5          │
│  GeoAgent    │  │  DispatchAgent │  │  HospitalAgent   │
│  Validate    │  │  Nearest ambu- │  │  ER pre-alert    │
│  GPS coords  │  │  lance via SMS │  │  ETA + severity  │
└──────────────┘  └────────────────┘  └──────────────────┘
         │                 │                 │
         ▼                 ▼                 ▼
┌──────────────┐  ┌────────────────┐  ┌──────────────────┐
│  GuideAgent  │  │  FamilyAgent   │  │  ReportAgent     │
│  CPR audio   │  │  Vehicle reg → │  │  FIR + insurance │
│  local lang  │  │  notify kin    │  │  PDF generation  │
└──────────────┘  └────────────────┘  └──────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  STEP 6 — Bystander receives confirmation                       │
│  ✅ Ambulance ETA  ✅ CPR audio  ✅ "Hospital team is ready"    │
└─────────────────────────────────────────────────────────────────┘
```

**AI/ML Pipeline:**

```
Panicked raw text
    │
    ▼  Claude Sonnet 4 ──→ intent extraction ──→ severity JSON
    │
    ▼  ChromaDB RAG ──→ WHO/Red Cross protocols ──→ CPR script
    │
    ▼  gTTS / ElevenLabs ──→ multilingual audio ──→ Twilio delivery
    │
    ▼  Celery task queue ──→ all 6 agents fire simultaneously
```

---

## 🚀 Key Innovations

> **This is not a chatbot. It's a coordination engine.**

| Existing System | Limitation | GoldenHour AI's Approach |
|---|---|---|
| **112 / Emergency Hotlines** | Single channel, human bottleneck, 4–8 min hold | AI parses instantly, no hold time |
| **Ambulance apps (FastHelp, etc.)** | Requires app + smartphone | Works on WhatsApp, SMS, USSD — any ₹800 phone |
| **Hospital alert systems** | Triggered on arrival, not before | ER pre-alerted with ETA before ambulance departs |
| **AI chatbots** | Sequential responses, no real-world actions | 6 agents execute in parallel with live integrations |
| **Existing CPR tools** | Requires app, English-only | Real-time audio in 10+ languages, zero install |

**The core insight:** Emergency response fails not from lack of resources — but from **sequential, siloed communication**. GoldenHour AI parallelizes what was always done in series.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **LLM / Orchestrator** | Claude Sonnet 4 (Anthropic) |
| **Backend** | FastAPI + Celery + Redis |
| **Database** | PostgreSQL (SQLAlchemy ORM) |
| **Vector DB / RAG** | ChromaDB |
| **Messaging** | Twilio (WhatsApp + Voice + SMS) |
| **Maps** | Google Maps Geocoding + Routes API |
| **Speech-to-Text** | OpenAI Whisper |
| **Text-to-Speech** | gTTS / ElevenLabs |
| **Vision** | GPT-4o (crash photo severity scoring) |
| **Frontend Dashboard** | React + Tailwind CSS |
| **Deployment** | Railway.app + Cloudflare |

---

## 📦 Installation

**Prerequisites:** Python 3.10+, Node.js 18+, Redis, PostgreSQL, Twilio account, Anthropic API key, Google Maps API key

```bash
# Clone
git clone https://github.com/pandeylakshya207-max/goldenhour-ai.git
cd goldenhour-ai

# Install dependencies
pip install -r requirements.txt

# Configure secrets
cp .env.example .env
# → Fill in: ANTHROPIC_API_KEY, TWILIO_*, GOOGLE_MAPS_KEY, DATABASE_URL

# Initialize database + RAG
python backend/db/seed.py
python backend/rag/ingest.py

# Start services
redis-server &
celery -A backend.main worker --loglevel=info &
uvicorn backend.main:app --reload --port 8000

# Frontend dashboard
cd frontend/dashboard && npm install && npm run dev
```

---

## ▶️ Usage

**Send this to your configured Twilio number:**

```
"Road accident near Silk Board flyover, Bengaluru. 3 injured. One not responding."
```

**System response in < 90 seconds:**

```json
{
  "incident_id": "GH-2026-0503-001",
  "severity": 4,
  "location": { "lat": 12.9176, "lng": 77.6234, "landmark": "Silk Board, Bengaluru" },
  "ambulance_dispatched": "KA-01-EMS-042",
  "hospital_alerted": "Manipal Hospital, HSR Layout",
  "eta_minutes": 8,
  "cpr_guidance_sent": true,
  "family_notified": true,
  "report_generated": "GH-2026-0503-001.pdf"
}
```

**Bystander receives:**
- ✅ Ambulance confirmation + live ETA
- ✅ CPR audio in their local language
- ✅ "Hospital trauma team is ready and waiting"

> 🌐 **[View Interactive Demo →](https://github.com/pandeylakshya207-max/goldenhour-ai/blob/main/goldenhour_ai_full_app.html)**

---

## 📂 Project Structure

```
goldenhour-ai/
├── backend/
│   ├── main.py                  # FastAPI app + Twilio webhook endpoints
│   ├── agents/
│   │   ├── orchestrator.py      # Claude LLM triage + parallel task routing
│   │   ├── dispatch_agent.py    # Nearest ambulance selection + SMS alert
│   │   ├── hospital_agent.py    # ER pre-alert + capacity check
│   │   ├── guide_agent.py       # CPR loop + multilingual TTS
│   │   ├── family_agent.py      # Vehicle reg lookup + kin notification
│   │   └── report_agent.py      # Legal-grade PDF generation
│   ├── integrations/
│   │   ├── twilio_client.py     # WhatsApp / Voice / SMS
│   │   ├── maps_client.py       # Google Maps geocoding + routing
│   │   └── llm_client.py        # Anthropic + OpenAI unified wrapper
│   ├── rag/
│   │   ├── ingest.py            # PDF chunking + embedding pipeline
│   │   ├── retriever.py         # ChromaDB semantic query
│   │   └── data/                # WHO / Red Cross source PDFs
│   ├── db/
│   │   ├── models.py            # Incident, Hospital, Ambulance schemas
│   │   └── seed.py              # 20 hospitals + 10 ambulances
│   └── config.py
├── frontend/
│   ├── dashboard/               # React hospital admin panel
│   └── demo/                    # Public demo page
├── goldenhour_ai_full_app.html  # Standalone interactive demo
├── docker-compose.yml
├── requirements.txt
└── README.md
```

---

## 💼 For Recruiters & Judges

This project demonstrates production-level thinking across multiple domains:

| Dimension | What this project shows |
|---|---|
| **System Design** | Multi-agent orchestration, parallel Celery workers, Redis queuing, <90s SLA |
| **AI Engineering** | LLM prompt design, RAG pipeline (ChromaDB + WHO docs), vision + STT + TTS integration |
| **Real-World Constraints** | Feature phone support, multilingual NLP, API fallback under latency, zero-install UX |
| **Product Thinking** | Solves a 300,000-deaths/year problem with zero behavior change required from users |
| **Scalability** | Stateless FastAPI agents, horizontal Celery scaling, cloud-agnostic deployment |

> *Built not to win a hackathon — built to actually work in rural Bihar at 2 AM.*

---

## 🌍 Real-World Impact Potential

GoldenHour AI is designed to scale across infrastructure realities:

- 🇮🇳 **India** — 1.5L+ annual road deaths. Works over WhatsApp (500M+ users) and SMS. Direct 112 API integration path ready.
- 🌏 **BIMSTEC** — Bangladesh, Myanmar, Sri Lanka, Thailand, Nepal, Bhutan. USSD path covers feature phone majority.
- 🌍 **Global South** — Any region with WhatsApp penetration, weak 911 infrastructure, and high road mortality.
- 🏛️ **Government + NGO** — Open API layer (v3.0 roadmap) enables municipal integration without rebuilding from scratch.

> **The infrastructure already exists — 500 million WhatsApp users, millions of ambulances, thousands of ERs. GoldenHour AI is the coordination layer they were all missing.**

---

## 🎤 Pitch

> *What if saving a life required nothing more than sending a WhatsApp message?*
>
> GoldenHour AI is a multi-agent AI system that turns one panicked text into a fully coordinated emergency response: ambulance dispatched, hospital pre-alerted, CPR audio delivered, family notified, legal report filed — all in parallel, all in under 90 seconds. No app. No training. No infrastructure barrier.
>
> Built for the 300 million people who live far from a trauma center and close to a national highway. Presented at IIT Madras Road Safety Hackathon 2026. Powered by Claude Sonnet 4, FastAPI, Twilio, and ChromaDB.

---

## ⚡ Roadmap

- [ ] **v1.1** — Live ambulance GPS tracking (WebSocket push)
- [ ] **v1.2** — USSD menu for zero-data feature phone trigger
- [ ] **v1.3** — Government 112 API integration (India, Bangladesh, Sri Lanka)
- [ ] **v2.0** — Predictive hotspot mapping (ML on historical incident data)
- [ ] **v2.1** — Offline PWA for paramedics
- [ ] **v2.2** — Full IVR voice call flow (Whisper STT + multilingual)
- [ ] **v3.0** — Open API for NGOs and municipal corporations

---

## 🤝 Contributing

High-value contribution areas:

- 🗣️ Regional language TTS (especially Sinhala, Burmese, Nepali)
- 🏥 Hospital / ambulance database integrations for new cities
- 📡 USSD flow testing on real feature phones
- ⚡ Load testing the Celery parallel pipeline

```bash
git checkout -b feature/your-feature
git commit -m "feat: describe change"
git push origin feature/your-feature
# → Open a PR
```

Follow [Conventional Commits](https://www.conventionalcommits.org/) · Open an issue before large PRs.

---

## 📜 License

MIT — free for research and non-commercial safety use. See [LICENSE](./LICENSE).

---

## 🙌 Acknowledgements

- **IIT Madras CoERS** — Road Safety Hackathon 2026
- **Anthropic** — Claude Sonnet 4, the orchestration brain
- **WHO & Red Cross** — First-aid protocols powering the RAG layer
- **Twilio** — Multi-channel messaging infrastructure
- Every bystander who ever stood helpless at an accident — *this is for you*

---

<div align="center">

<br/>

**300,000 people a year. One coordination layer that could change that.**

If this project matters to you — star it, share it, build on it.

[![Star this repo](https://img.shields.io/github/stars/pandeylakshya207-max/goldenhour-ai?style=social)](https://github.com/pandeylakshya207-max/goldenhour-ai/stargazers)

<br/>

*Share on [LinkedIn](https://linkedin.com) · [Twitter / X](https://twitter.com) · Tag someone building for social impact*

<br/>

> *"The best emergency system is the one that requires nothing from the person in shock."*

</div>
