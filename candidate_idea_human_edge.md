# Candidate Idea: Human Edge

**Status:** DOCUMENTED candidate — **long-horizon flagship** (not primary XPRIZE entry as of 2026-07-30)  
**Primary competition entry:** See `selected_idea_mom_test.md` (Mom Test AI)  
**Decision date:** 2026-07-30  
**Source review:** `D:\MAJOR-NODES\HUMAN-EDGE\Project-Human-Edge` (vision, product definition, business model, strategic analysis, project status) vs competition criteria  

---

## Decision (position in portfolio)

**Human Edge** is the flagship product under the Human Edge brand: turn **699 mental models** into a **daily insight engine** (“Inshorts for Intellectuals”). It is a strong multi-year company thesis with unusual execution maturity (Flutter MVP largely built, honesty-cleaned, release-ready).

For **Build with Gemini XPRIZE** (deadline **Aug 17, 2026**), it is **not** the default primary entry — unless reframed as an **AI-native media operations business** with new post–May 19 revenue (see “XPRIZE path if chosen”).

| Field | Choice |
|--------|--------|
| **Working name** | Human Edge |
| **Best XPRIZE category (if entered)** | **Education & Human Potential** |
| **One-liner** | Swipe the news. Decrypt it through a mental model. Build your intellectual edge. |
| **Product context repo** | `D:\MAJOR-NODES\HUMAN-EDGE\Project-Human-Edge` |
| **Implementation (app)** | Greenfield Flutter app (path per project docs / ADRs; historically `App-Human-Edge`) |
| **Content asset** | **699 mental models** (migrated / migrating into dedicated Supabase) |
| **Legacy reference** | Mental-Models-Directory (React/Vite — read-only migration source) |

---

## What the product is

### Thesis
People want to think better but will not do homework. Wrap mental models inside **daily news consumption** (Trojan horse):

1. **See News** — short Signal card (vertical swipe feed)  
2. **Decrypt via Lens** — reveal the mental model explaining *why*  
3. **Get Insight** — second-order / deeper truth  
4. **Save** — build personal **intellectual footprint**  
5. **Explore deeper** — Instagram-style case-study stories on models  

### Core surfaces (MVP)

| Surface | Role |
|---------|------|
| **Signal** | Daily hook — swipe feed + Decrypt |
| **Explore** | Directory of 699 models, search, categories |
| **Profile** | Saved insights/models, footprint / Signal Ratio |
| **Onboarding** | Role, industry, mandate → Signal Profile |

### User modes

| Mode | Can do | Cannot (MVP) |
|------|--------|----------------|
| **Public visitor** | Browse Signal, decrypt, explore models/stories | Save, private footprint |
| **Signed-in learner** | Save insights/models, build footprint | Full premium modules |
| **Premium practitioner** | Deeper case studies, lens packs *(deferred)* | — |

### Business model (from product docs)

| Layer | Model |
|-------|--------|
| **Free** | Swipe feed + instant Lens/Edge (never paywall the aha) |
| **Pro** | Deep case-study library — ~$9/mo or ~$99/yr |
| **Ads (optional)** | Native premium sponsorships in feed (not cheap banners) |
| **Later** | B2B / cohort licenses (consulting, education, firms) |

**Economic principle:** Monetize deep analytical thinking (premium); use high-velocity free feed as acquisition.

---

## Why this idea is strong (company lens)

| Strength | Detail |
|----------|--------|
| **Real problem** | News is noisy; mental models are collected but not applied in the moment |
| **Differentiation** | News × models join beats pure Inshorts *and* pure Farnam-Street-style libraries |
| **Content moat** | 699 curated models + stories — rare starting asset |
| **Product loop** | Habit (feed) → aha (decrypt) → identity (footprint) → depth (stories) |
| **Execution maturity** | Specs, ADRs, task contracts; MVP milestones M0–M6 complete; honesty cleanup; release path defined |
| **Brand fit** | Aligns with Human Edge / mental-models / Point Blanc intellectual brand |

---

## Competition scoring (~18 days left)

Scored for **Build with Gemini XPRIZE** judging (equal weight) + shippability.

| Criterion | Fit | Notes |
|-----------|-----|--------|
| **Business viability** | Medium | Freemium/habit apps convert slowly; Pro not fully the competition wedge yet. Revenue in 18 days is hard without a **new paid slice**. |
| **AI-native operations** | Medium (High *if reframed*) | Consumer “app with AI features” is weaker than **agents that run the media business** (ingest, match lens, publish, personalize, measure). |
| **Category impact** | High | Education & Human Potential — critical thinking at scale; path to 100k+ learners is credible. |
| **Ship speed** | High (app) / Low (new revenue) | App is far along; **new business + Stripe + AI ops evidence** still required under contest rules. |
| **Gemini / Google Cloud** | Natural *if* pipeline moves to Gemini | Content matching, personalization, and publish agents are ideal Gemini workloads. |

### Rules risk (must not ignore)

| Risk | Mitigation |
|------|------------|
| **“New after May 19, 2026”** | Full Human Edge pre-dates the window. Contest needs a **new business/project** after start date — or a clearly new commercial line with disclosed prior templates/code. |
| **Pre-existing product** | Do not submit “we shipped the whole app last month” as the *new* business without a clean narrative of **what was created during the hackathon**. |
| **Revenue** | Free feed alone does not score Business Viability. Need **earned revenue** + P&L. |

---

## Comparison to Mom Test AI (primary entry)

| | **Mom Test AI** (`selected_idea_mom_test.md`) | **Human Edge** (this doc) |
|--|-----------------------------------------------|---------------------------|
| **Role** | **Primary XPRIZE entry** | Long-game flagship / optional secondary path |
| **Category** | Entrepreneurship & Job Creation | Education & Human Potential |
| **Who pays now** | Founders / PMs (clear B2B) | Consumers → Pro (slower) |
| **AI decides** | Interview quality, evidence, assumptions | Content match, personalization, publish (if built) |
| **18-day revenue odds** | Higher | Lower without a new paid wedge |
| **Ambition** | Narrow wedge | Brand + media + product compounder |

**Portfolio stance:** Build **Mom Test AI** for the prize race; keep **Human Edge** as the multi-year intellectual brand — they can reinforce later (founders who validate → think better with Human Edge).

---

## Product definition (XPRIZE path *if* chosen)

Only pursue this as the competition vehicle if the following MVP business is real.

### Who pays (competition wedge — not freemium dream)

Pick **one** paid offer for the 90-day window:

| Option | Offer | Price sketch |
|--------|--------|----------------|
| **A (recommended)** | **Human Edge Pro — early founder/PM cohort** | $9–15/mo for case studies + weekly Lens Pack |
| **B** | **Signal Ops — “your industry Lens Pack”** | $19–29/mo curated vertical (e.g. Product, Finance) |
| **C** | **B2B pilot** | Small team license for analyst training |

### What the business must sell during the hackathon

1. Live Signal feed with **Decrypt** in production  
2. **Gemini-run (or Gemini-assisted) content pipeline** — news → model match → insight copy → publish  
3. At least one **paid** conversion path with Stripe (or equivalent) evidence  
4. Agent logs showing AI executing **key decisions** (which model, which angle, publish/hold)  

### What humans do vs what AI does

| Humans | AI (Gemini agents) |
|--------|---------------------|
| Taste, brand, final editorial gate | Ingest/source candidates; propose model–news pairs |
| ICP and positioning | Score Signal vs Noise for user profile |
| Sell Pro / collect testimonials | Generate draft Lens/Edge copy; flag weak matches |
| App product direction | Personalize feed ranking; log decisions for evidence |

### Pricing (competition-first)
- Charge **from day one** for Pro or a pack — free-only feed is not enough for judges  
- Keep free Decrypt aha (per business model rules); paywall **depth / packs / history**

---

## Gemini ecosystem mapping (Idea → Revenue)

| Stage | Google surface | How Human Edge would use it |
|-------|----------------|------------------------------|
| **01 Idea** | Gemini App | ICP wedges, pack themes, category narrative |
| **02 Prototype** | Google AI Studio | Lens-matching prompts, decrypt quality, ranking agents |
| **03 Design** | Stitch | Landing, paywall, shareable insight cards |
| **04 Build** | Google Antigravity | Agent-assisted pipeline + app integrations |
| **05 Ship** | Google Cloud | Host pipeline, APIs, logs, scale; **$300 credit** if eligible |
| **06 Launch** | Flow | 3-minute demo (Decrypt live + agent ops) |
| **07 Grow** | Pomelli | On-brand insight cards / social distribution |

**Technical mandate checklist (if this becomes the entry)**
- [ ] At least one **Google Cloud** product in production  
- [ ] At least one **Gemini API** LLM call in the live product/pipeline  
- [ ] Agent/API **logs + dashboards** as product evidence  
- [ ] Business activity **new after May 19, 2026** clearly scoped (disclose reused app/templates)  
- [ ] Earned **revenue** + P&L (not donations)  

---

## How this maps to prizes (if entered)

| Judging criterion | Proof we would collect |
|-------------------|------------------------|
| **Business viability** | Stripe revenue, Pro/pack conversions, P&L, monthly revenue split, users acquired |
| **AI-native operations** | Publish pipeline logs, Gemini usage/observability, “AI chose model X for story Y” demos, Cloud billing PDFs |
| **Category impact** | Narrative: critical thinking / media literacy at scale; 699 models; path to 100k learners; testimonials |

**Category prize note:** $50k for highest-grossing team **in each category** — freemium consumer is a weaker gross path than a high-ARPU B2B wedge unless Pro converts hard.

---

## Submission alignment (if entered)

Required package (see `submission_checklist.md`):

- GitHub repo (share with `testing@devpost.com` + `judging@hacker.fund` if private)  
- ≤3 min video — AI live in production (pipeline + Decrypt, not just UI tour)  
- 500–1000 word narrative — humans vs AI, jobs/opportunity story  
- Revenue + expense evidence (P&L template)  
- Product evidence folder (logs, API usage, dashboards)  
- Customer evidence (contacts + testimonials)  

**Deadline:** Aug 17, 2026 @ 1:00pm PDT  

---

## Immediate next steps (by path)

### Path A — Stay long-game flagship (default)
1. Cut first internal / TestFlight / Play internal build (per `PROJECT_STATUS` / release setup)  
2. Stand up **daily Signal publish SOP** (human + LLM assist)  
3. Ship shareable insight cards for distribution  
4. Define **one** Pro wedge and first 50–100 users  
5. Do **not** dilute XPRIZE sprint unless Path B is chosen  

### Path B — Elevate to XPRIZE entry (only if primary changes)
1. Explicitly **replace or dual-enter** vs Mom Test AI (document decision)  
2. Define **new business slice after May 19** + disclose prior code  
3. Wire **Gemini** into content ops as the star of the submission  
4. Charge Pro/pack immediately; instrument P&L and agent logs  
5. Film demo last from real production Decrypt + agent decisions  

---

## Risks and open product decisions

| Risk / open item | Why it matters |
|------------------|----------------|
| **Content engine** | LLM pipeline vs human curation still the load-bearing unknown |
| **ICP sharpness** | “Intellectuals” is vague — need a first wedge (e.g. PMs, founders, analysts) |
| **Habit competition** | Same thumb as X / LinkedIn / Inshorts |
| **Pro conversion** | Free must create identity; paid must feel career/skill ROI |
| **“100% Signal” promise** | Overclaiming destroys trust if feed quality is mixed |
| **Scope creep** | CMS / ads / multi-surface ecosystem can stall the daily loop |

---

## Decision log

| Date | Decision | Owner |
|------|----------|--------|
| 2026-07-30 | Document **Human Edge** as competition **candidate** + long-horizon flagship; **primary XPRIZE entry remains Mom Test AI** | Blue Akash + agent review of Project-Human-Edge |
| 2026-07-30 | Best category if entered: **Education & Human Potential** | Same |
| 2026-07-30 | XPRIZE-viable only if reframed as **AI-native media ops + paid wedge**, with post–May 19 business scope | Same |

---

## Related docs

### This folder (XPRIZE)
- `selected_idea_mom_test.md` — **primary selected entry**  
- `details.md` — competition overview  
- `rules_summary.md` / `faq.md` — constraints  
- `submission_checklist.md` — Devpost fields  
- `technical_capabilities.md` — Gemini stack  
- `marketing_strategy.md` — charge day one, first customers  
- `brainstorming.md` — earlier unselected hooks  

### Project-Human-Edge (source of truth)
- `_Core/Vision_v00.00.md`  
- `_Core/UX & Product/APP_PRODUCT_DEFINITION_v00.00.md`  
- `_Core/Business Strategy/BUSINESS_MODEL_v00.00.md`  
- `_Core/STRATEGIC_ANALYSIS_v00.00.md`  
- `_Core/CURRENT_STATE_v00.00.md`  
- `_Core/PROJECT_STATUS.md`  
