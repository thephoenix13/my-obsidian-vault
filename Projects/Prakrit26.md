---
tags: [project, healthtech, ai, fullstack, react, supabase, openai, claude]
status: Active Development
codebase: C:/Users/Admin/svasthai
docs: D:/Projects/PrakritAI
---

# Prakrit26 — Prakrit AI (Complete Reference)

> Family health management and AI-powered health companion platform targeting Indian families. Two folders make up this product: the active codebase (`svasthai`) and the strategy/documentation archive (`PrakritAI`).

---

## Product Overview

**What it is:** A central platform for families to manage health records, analyze medical documents with AI, track medications, and get 24/7 health assistance — all in one place.

**Problem it solves:** Scattered health records, inability to understand medical reports, medication non-compliance, and lack of continuous health engagement between doctor visits.

**Target users:** Families, caregivers, individuals managing chronic conditions, anyone confused by medical reports.

**Market:** India-first (English + Hindi), with LATAM expansion planned.

**Stage:** Pre-launch / Beta with waitlist (as of April 2026).

---

## Core Features

1. **Family Health Profiles** — Separate health records for each family member (spouse, parents, children)
2. **AI Document Analysis** — Upload lab reports, prescriptions, X-rays, ultrasounds; get plain-language AI explanations
3. **Medication Tracking** — Track medications for all family members, reminders, adherence monitoring
4. **24/7 AI Health Assistant** — Context-aware conversational AI with voice mode
5. **PrakritGPT** — Advanced document-aware AI chat for deeper health questions
6. **Health Timeline** — Chronological record of all documents, consultations, and medications
7. **Health Insights** — Cross-report analysis, trend detection, pattern recognition
8. **Emergency Health Card** — Store blood type, allergies, emergency contacts, critical medications
9. **WhatsApp Integration** — AI health assistant via WhatsApp (Twilio, short-form 8-line responses)
10. **Admin Dashboard** — Waitlist management and admin features

---

## Tech Stack

### Frontend
- React 18.3.1 + TypeScript
- Vite 5.4.19
- shadcn/ui + Radix UI
- Tailwind CSS 3.4.17
- React Router DOM v6
- TanStack React Query v5
- React Hook Form + Zod
- Recharts (charts)
- Framer Motion (animations)
- i18next (English/Hindi)
- Sonner (notifications)
- Lucide React (icons)

### Backend (Supabase)
- PostgreSQL with Row-Level Security (RLS)
- Supabase Auth
- 17 Deno Edge Functions

### AI & Integrations
- OpenAI API (document analysis, assistant)
- Anthropic Claude API (PrakritGPT, health insights)
- Twilio (WhatsApp webhook, voice)
- Web Speech API (voice input/output)
- pdfjs-serverless (medical PDF processing)

---

## Supabase Edge Functions (17 total)

| Function | Purpose |
|---|---|
| ai-health-assistant | Conversational AI with family health context |
| analyze-medical-document | OCR + AI analysis of medical documents |
| prakrit-gpt-chat | Advanced document-aware chat |
| voice-assistant | Voice input processing |
| voice-session-token | Temporary voice session tokens |
| whatsapp-webhook | Twilio WhatsApp integration |
| generate-health-insights | Trend analysis across multiple documents |
| intelligent-search | Search across family health records |
| compare-health-reports | Comparative analysis of test results |
| detect-warnings | Flag abnormal values and health risks |
| personalized-recommendations | Generate health recommendations |
| explain-medical-term | Explain medical terminology in plain language |
| get-admin-users | Admin user management |
| send-waitlist-email | Waitlist email notifications |
| seed-test-data | Development test data generation |

---

## App Routes

| Route | Page |
|---|---|
| `/` | Landing page (marketing, features, team) |
| `/auth` | Login / Signup |
| `/dashboard` | Main health overview |
| `/family` | Family member profiles |
| `/documents` | Upload & analyze medical documents |
| `/medications` | Medication tracking |
| `/ai-assistant` | Conversational health assistant |
| `/health-insights` | Trend analysis & recommendations |
| `/emergency` | Emergency health card |
| `/timeline` | Chronological health history |
| `/prakrit-gpt` | Advanced AI chat |
| `/admin` | Admin / waitlist management |
| `/join-waitlist` | Pre-launch signup |

---

## Project Structure

```
svasthai/
├── src/
│   ├── pages/           # 20+ page components
│   ├── components/      # UI, BottomNav, VoiceMode, ProtectedRoute
│   ├── components/ui/   # shadcn-ui library
│   ├── components/admin/
│   ├── integrations/supabase/
│   ├── hooks/           # useVoiceMode, useScrollAnimation
│   ├── utils/           # VoiceAudio.ts
│   ├── i18n/            # English/Hindi configs
│   └── assets/
├── supabase/
│   ├── functions/       # 17 Edge Functions
│   └── migrations/      # DB schema migrations
├── public/
└── package.json
```

---

## Environment Variables

```
VITE_SUPABASE_URL=https://rppnbesqzrunyjgpeojn.supabase.co
VITE_SUPABASE_PROJECT_ID=rppnbesqzrunyjgpeojn
VITE_SUPABASE_PUBLISHABLE_KEY=[JWT]

# Supabase Edge Function secrets
ANTHROPIC_API_KEY
OPENAI_API_KEY
TWILIO_ACCOUNT_SID
TWILIO_AUTH_TOKEN
SUPABASE_SERVICE_ROLE_KEY
```

---

## Strategy & Documentation (D:/Projects/PrakritAI)

### Version History (Product Iterations)
| Version | Focus |
|---|---|
| v1 | Early planning, pitch decks, MVP user journey map, competitive research (Hey Doc App) |
| v2 | Social media plan, 4-week content calendar, refined user guide |
| v3 | Landing page design, LinkedIn content for brand & founder |
| v4 | Latest design iterations, personal branding |

### Key Documents
- **Prakrit AI Information Manual** — Full user guide (PDF + DOCX)
- **Prakrit AI Write Up** — Product overview and positioning
- **Apollo-Integration Master Plan** — Detailed Apollo 247 integration plan
- **Apollo-Feature Integration Summary** — Feature overview for Apollo partnership
- **Social Media Plan v2** — Marketing strategy
- **4-Week Content Calendar** — Launch content plan

---

## Apollo 247 Integration Plan

9 features planned for integration into the Apollo 247 healthcare ecosystem:

1. AI Document Analysis — explain Apollo lab reports in plain language
2. Medication Tracking — with Apollo pharmacy refill integration
3. Family Health Profiles — replacing discount-only Circle dashboard
4. AI Health Assistant — post-consultation patient engagement
5. Health Timeline — populated from Apollo test history
6. Health Insights — for Apollo chronic disease program patients
7. Maternal Health Tracking — for Apollo MomVerse hub
8. Emergency Health Card — at Apollo physical touchpoints
9. PrakritGPT — upgrade/replace Apollo's "Ask Apollo" feature

**Positioning:** Fills the patient engagement gap between Apollo healthcare events.
**Revenue model:** Drives consultations, pharmacy orders, diagnostics, and Circle member retention.

---

## Team

| Name | Role |
|---|---|
| Shailesh N A | Partner & Co-Founder |
| Narayanan Ramachandran | Product Lead & Co-Founder |
| Digital5 | Tech Partner / Digital Agency |

---

## Current Status (April 2026)

- 244 git commits — active, mature codebase
- Pre-launch / waitlist phase
- Recent work: WhatsApp demo, session management, memory leak fixes, auth token fixes
- 21 bug fixes documented (null checks, error handling, UI polish)
- Apollo 247 integration in planning stage
