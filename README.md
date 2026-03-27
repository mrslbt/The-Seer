# The Seer — Astrology Oracle

A web-based astrology oracle that combines real astronomical calculations with AI to deliver personalized readings, natal charts, daily cosmic forecasts, and relationship compatibility.

Live at [theseer.xyz](https://theseer.xyz)

## What is The Seer?

The Seer is a mobile-first astrology app that actually computes your natal chart from real planetary data — not lookup tables. It runs the Swiss Ephemeris (the same engine used by professional astrologers) directly in your browser via WebAssembly, calculates your exact planetary positions, house cusps, and aspects, then uses that data to power everything: daily forecasts, oracle readings, compatibility reports, and chart analysis.

When you ask a question, The Seer sends your real chart data and current transits to an LLM that responds as an ancient, direct oracle — brief, pointed, slightly unsettling.

## Why?

Most astrology apps give you generic horoscopes based on your sun sign alone. The Seer uses your full birth data (date, time, place) to compute a complete natal chart, then cross-references it against real-time planetary transits. The readings aren't canned — they're generated from actual astronomical context specific to you and the current sky.

## Features

### Oracle
Ask yes/no or open-ended questions. The Seer classifies your question (love, career, money, health, etc.), scores the relevant transits in your chart, and delivers a reading — max four sentences. Ask follow-ups for deeper context, or tap "Why did The Seer say this?" for an insight article explaining the astrology behind the answer.

### Cosmos Dashboard
A personalized daily forecast. Overall cosmic score (1-10), category-by-category breakdowns, key transits affecting you today, moon phase, retrogrades, and transit timing. Auto-refreshes every 30 minutes.

### Natal Chart
Your full chart: Big Three (Sun, Moon, Rising), all planetary placements with signs, degrees, and houses, retrograde indicators, house cusps, and an AI-generated personality reading. Ask questions about your chart — superpower, love style, career path.

### Bonds (Compatibility)
Select two profiles and get full synastry analysis — cross-chart aspects, element harmony, relationship signatures. Shows a compatibility tier (fated, magnetic, kindred, complex, friction, distant), a daily "bond pulse" showing how today's transits affect the pair, and answers relationship questions via the oracle.

### Other
- **Multi-profile** — up to 10 profiles with full natal charts, stored locally
- **Reading history** — last 100 readings saved with timestamps and moon phase
- **Shareable readings** — generates an image card for sharing via Web Share API
- **Sound design** — procedurally generated ethereal tones via Web Audio API
- **Crisis detection** — detects self-harm language and surfaces crisis hotline numbers
- **PWA** — installable, offline-capable app shell
- **i18n** — English and Japanese

## Tech Stack

- React 18 + TypeScript + Vite
- **Swiss Ephemeris (WASM)** — real astronomical calculations running client-side
- **OpenAI GPT-4o-mini** — oracle responses via serverless API
- **Cloudflare Pages** — hosting, serverless functions, D1 database
- **PostHog** — analytics
- **Sentry** — error tracking
- Web Audio API — procedural sound effects
- Canvas API — shareable reading cards

## Getting Started

```bash
git clone https://github.com/mrslbt/The-Seer.git
cd The-Seer
cp .env.example .env    # add your OPENAI_API_KEY
npm install
npm run dev
```

The oracle endpoint requires an OpenAI API key.

@bymarselb
