# Challenge 1: Mom Test AI — Truth-Seeking Customer Discovery
**Competition:** Build with Gemini XPRIZE  
**Category:** Entrepreneurship & Job Creation  
**Working name:** Mom Test AI *(final brand TBD)*  
**Sector:** Founder tooling / Customer discovery / User research SaaS

> **Source idea:** [`../selected_idea_mom_test.md`](../selected_idea_mom_test.md)  
> **Existing system (asset base):** `D:\MAJOR-NODES\WORK-SYSTEMS\MOM-TEST`  
> **Related product nodes:** `PROJECT-NODES\01-PERSONAL-GROWTH-PROJECTS\Mom-Test-Idea`, `PROJECT-NODES\06-SOLOPRENEUR-SAAS-PROJECTS\Mom-Test-Tool-Idea`

---

## Challenge Context

Most early products fail not because founders cannot ship code, but because they **never learned the truth about demand**. They ask leading questions ("Would you use this?"), collect compliments ("Sounds amazing!"), and treat politeness as validation. By the time the product launches, the "yeses" evaporate into zero revenue.

This is the problem Rob Fitzpatrick named in *The Mom Test*: people are motivated to be kind, so they lie — usually without meaning to. The way through is discipline: talk about **their life**, ask about **past concrete behavior**, dig under flattery, and treat **commitment** (time, reputation, money) as the only real signal.

Today, founders and product teams still run discovery with:

- Spreadsheets and Notion pages that do not enforce Mom Test rules  
- Generic interview templates that still ask hypotheticals  
- Manual transcript review with no systematic flattery / fluff detection  
- No living map of which assumptions are validated, invalidated, or still untested  

There is **no widely adopted AI-native loop** that (1) plans unbiased questions from a hypothesis, (2) scores those questions against Mom Test rules, (3) reviews transcripts for fact vs opinion vs compliment, and (4) updates an assumption vault with evidence quotes and next actions — with agents making those classification decisions in production.

We already own a deep **methodology system** (book + domain-agnostic engine + guide generator + relationship preset + sample multi-chapter guides) under `WORK-SYSTEMS\MOM-TEST`. That system proves the method is codifiable. The competition challenge is to **productize the business-customer-discovery path** into a real Gemini-operated SaaS that ships, charges, and logs AI decisions before the XPRIZE deadline (**Aug 17, 2026**).

The initial proof of concept should focus on the **founder / early-team customer-interview loop** (hypothesis → interview plan → transcript in → Gemini report out → assumption vault), with the potential to expand into multi-domain truth extraction (co-founder vetting, hiring, enterprise discovery) using the same engine skeleton already proven in MOM-TEST.

---

## Challenge Description

**Develop:** An AI-native SaaS that helps founders, product managers, and researchers run customer interviews the Mom Test way — planning unbiased questions, reviewing transcripts, flagging flattery and fluff, extracting real demand signals, and maintaining a living insight vault per project.

**How might Gemini agents close the truth gap in customer discovery by deciding which questions are biased, which answers are evidence vs compliments, which assumptions are validated or invalidated, and what to ask next?**

**That helps users to:**

1. Turn a problem hypothesis into a **Mom Test–safe interview guide** (questions about past behavior, not opinions about the product).  
2. **Score and rewrite** draft questions against the three Mom Test laws and the bad-data counter-moves (deflect compliments, anchor fluff, dig beneath signals).  
3. **Ingest interview transcripts** (paste/upload) and label each claim as fact, opinion, hypothetical, compliment, or commitment signal.  
4. **Map evidence** to assumptions: validated / invalidated / needs more data, with quote-level support.  
5. Recommend **next interviews, next questions, and commitment asks** (time / reputation / money) so conversations advance instead of "going well."  
6. Store a **project insight vault** so learning compounds across interviews instead of dying in notes apps.  
7. Operate with **human-in-the-loop** final go/no-go calls — AI decides classifications and recommendations; humans own the business decision.

**Priority scope:**

1. **Business customer discovery** as the initial domain (the original Mom Test use case).  
2. Solo founders and early teams (1–10 people) validating a B2B or B2C idea.  
3. Core loop only: hypothesis + assumption map → interview plan → transcript analysis → assumption status + next actions.  
4. Gemini API + at least one Google Cloud surface in production; agent logs retained as product evidence.

**Target outcomes (competition window):**

1. Live product with **real paying users** (target path: first 5–10 seats at **$29–49/mo** or interview packs at **$19–39**).  
2. Measurable **AI-native operations**: Gemini agents execute question scoring, transcript labeling, and assumption status updates in production (logs + dashboards).  
3. Credible **category impact** narrative: better validation → fewer dead startups → more viable products and jobs; path toward **100k+** founders/operators.  
4. Full XPRIZE submission package: GitHub, ≤3 min video of AI live, 500–1000 word narrative, P&L, product + customer evidence.

**Data / assets expected to be available:**

1. **Methodology corpus** — full book chapters + engine rules already in `MOM-TEST/book` and `MOM-TEST/system/engine`.  
2. **Generation procedure & templates** — intake form, guide template, note-taking legend, commitment ladders.  
3. **Worked sample guides** — e.g. relationship-vetting SAMPLE (structure to mirror for business preset).  
4. **User-provided** problem statements, assumptions, and interview transcripts (synthetic demos allowed pre-customer; real transcripts after first users).  
5. **Public founder/research content** for PoC demos (podcast transcripts, published interview write-ups, YC/IndieHackers case notes — fair-use / synthetic paraphrases preferred for demos).  
6. Stripe (or equivalent) billing, Cloud logs, and simple P&L for competition evidence.

**The solution must be able to:**

* Ingest a hypothesis / problem space and produce Mom Test–compliant question sets.  
* Detect and rewrite biased, hypothetical, leading, or compliment-seeking questions.  
* Continuously analyse transcript text (and optionally audio later) for fact vs fluff vs commitment.  
* Surface **rationale** for every AI label (why this is flattery; which rule it violates; what to ask instead).  
* Update assumption status with linked evidence quotes.  
* Recommend the next concrete advancement ask (not "stay in touch").  
* Run as a focused MVP first (paste transcript → report), then expand to live interview HUD, multi-interviewee aggregation, and domain presets.  
* Be validated with real founders in short workshops or paid pilots; human-in-the-loop is mandatory for go/no-go.

**Indicative proof-of-concept approach:**

* **Phase A (days):** Productize the business-discovery preset from the existing engine; Gemini prompt chain for question scoring + transcript labeling; minimal web UI.  
* **Phase B (1–2 weeks):** Charge first users; instrument logs/dashboards; tighten prompts on real transcripts.  
* **Phase C (pre-deadline):** Polish demo video from production usage; package revenue + AI evidence for Devpost.  
* Live recording / multi-party interviews / multi-domain presets are **post-MVP** unless a paying user forces priority.

---

## What We Already Have vs What We Must Solve

> The `MOM-TEST` system is the **knowledge and generation backbone**. The XPRIZE product is the **productized, Gemini-operated business layer** on top. Do not rebuild methodology from scratch; productize and instrument it.

### Already built (`D:\MAJOR-NODES\WORK-SYSTEMS\MOM-TEST`)

| Asset | What it is | Product value |
|---|---|---|
| **Book corpus** (`book/`) | Full *Mom Test* chapters + cheatsheet | Ground-truth rules for prompts and UX copy |
| **Engine core** (`system/engine/`) | Principles, bad-data moves, commitment/advancement, generation procedure, intake, templates, note-taking | Domain-agnostic "truth extraction OS" |
| **Preset architecture** | `_TEMPLATE/` + catalog + new-preset procedure | Scalable path: business, co-founder, hiring, etc. |
| **Relationship preset** | Full domain pack + SAMPLE multi-chapter guide | Proof the engine works end-to-end *outside* pure business |
| **Guide output shape** | Quick sheet, scenario, big-3 goals, Q bank, good-vs-bad, traps, commitment ladder, scorecard, note legend | Spec for SaaS report sections |
| **PDF tooling** (`tools/`) | Compile guides to HTML/PDF | Optional export for paid tiers later |
| **Claude-operated workflow** | Natural-language "generate a guide for X" | Validates UX of intake → tailored guide; not yet multi-tenant SaaS |

### Explicit gaps the product must close

| Gap | Why it matters for XPRIZE |
|---|---|
| **No production Gemini agents** | Judging criterion #2 requires AI executing key decisions *in production* with logs |
| **No multi-tenant product UI** | Cannot charge founders via a private Claude session in a local repo |
| **Business customer-discovery preset not first-class** | Catalog today leads with *relationship*; competition ICP is founders validating ideas |
| **No transcript analysis pipeline** | Core MVP differentiator: fact vs fluff labeling at scale |
| **No assumption vault / project memory** | Learning must compound across interviews |
| **No billing, auth, observability** | Business viability + AI-ops evidence require Stripe + Cloud + dashboards |
| **No revenue or customer evidence yet** | Competition weights real users and real revenue equally with AI story |

### The wedge insight

Start where the existing system is **already sharp** (rules, bad-data taxonomy, commitment ladder, guide structure) and where Gemini is **naturally strong** (classification, rewrite, structured extraction). Do **not** start with live multi-party interview HUD, mobile apps, or marketplace features.

---

## PoC Data & Content Sourcing Strategy

> While real customer transcripts are the gold standard, a demo and early eval harness can be built from public methodology material + synthetic founder scenarios. Pitch: *"Here's the agent labeling a realistic discovery transcript. Now paste your last three interviews and see which assumptions actually have evidence."*

### 1. Methodology & Rule Grounding

| Source | What It Provides | Access |
|---|---|---|
| **`MOM-TEST/book/`** | Canonical principles, bad-data types, commitment rules | Local (owned) |
| **`MOM-TEST/system/engine/`** | Operationalized rules for agents | Local (owned) |
| **Rob Fitzpatrick — *The Mom Test*** | Source book; keep product educational, not a full reprint | Fair use / paraphrase; own systemization |
| **Customer Development / Lean literature** | Complementary language for assumption testing | Public |

### 2. Competitive & Market Signals (business case)

| Source | What It Provides | Access |
|---|---|---|
| **CB Insights / startup failure studies** | "No market need" as top failure cause | Public summaries |
| **YC, IndieHackers, Lenny's Newsletter** | How founders actually run discovery | Public |
| **Dovetail, Condens, Grain, Notion AI** | Adjacent research tooling (not Mom-Test-native) | Public sites |
| **User Interviews, Respondent** | Recruiting markets; partnership adjacency | Public |

### 3. Synthetic & Demo Transcripts

| Source | What It Provides | Access |
|---|---|---|
| **Hand-authored synthetic interviews** | Controlled cases: heavy flattery, pure fluff, real commitment, mixed signals | Build in-repo under `fixtures/` |
| **Paraphrased public founder stories** | Realistic problem language without PII | Manual curation |
| **First 5–10 paid users' pastes** | Real distribution for prompt eval (with consent) | Post-launch |

### 4. Product Evidence Stack (competition-mandated)

| Source | What It Provides | Access |
|---|---|---|
| **Gemini API usage logs / Cloud Monitoring** | Proof of production AI decisions | Google Cloud |
| **Stripe / payment exports** | Revenue evidence | Paid product |
| **Agent decision logs** (structured JSON) | Question scores, label decisions, assumption updates | App instrumentation |
| **Customer testimonials + contacts** | Customer evidence for judges | Sales process |

### PoC Build Strategy

1. **Encode the engine rules** as system prompts + structured JSON schemas (fact / fluff / compliment / commitment / dig-next).  
2. **Ship business preset v1** (hypothesis intake → question bank → scorecard) using engine + book — not relationship-first.  
3. **Transcript analyzer MVP** on synthetic fixtures first, then real user pastes.  
4. **Assumption vault** as simple project-scoped records (status + quotes + links).  
5. **Charge from day one**; use paid usage to refine prompts and collect evidence for the video/P&L.

This demonstrates the full pipeline — plan, score, analyze, advance — without waiting for perfect voice infrastructure.

---

## Business Case Analysis & Execution Plan

> *This section turns the competition entry into a pitchable business case: ICP, pain, product wedges, complexity, SWOT, and a demo narrative judges and early customers can feel.*

### Customer Profile (Target ICP)

| Detail | Info |
|---|---|
| **Primary ICP** | Solo founders and 2–5 person early teams validating a new product idea |
| **Secondary ICP** | Product managers / UX researchers running continuous discovery |
| **Tertiary ICP** | Accelerators, founder communities, indie-hacker cohorts |
| **Geography** | Global English first; India / SEA founder density is a practical launch network |
| **Willingness to pay** | Already pay for Notion, ChatGPT Plus, research tools; **$29–49/mo** is in-range if it saves failed build months |
| **Current state** | Google Docs interview notes, "would you buy?" questions, compliment collection, no assumption tracker |
| **The core goal** | Get **truth** (facts + commitment) cheaply enough to kill or refine the idea *before* a large build |

### Product Portfolio (What the business sells)

| Module | What it is | Competition priority |
|---|---|---|
| **Interview Planner & Question Builder** | Hypothesis → assumptions → Mom Test–safe script; bad-question detector | **MVP — must ship** |
| **Transcript Truth Analyzer** | Paste/upload → fact / fluff / compliment / commitment labels + dig prompts | **MVP — must ship** |
| **Assumption & Insight Vault** | Per-project status board with evidence quotes and next actions | **MVP — must ship** |
| **Commitment Ladder Coach** | End-of-interview advancement asks (time / reputation / money) | MVP-light |
| **Live Interview HUD** | On-screen prompts during a call ("don't pitch"; next dig) | Post-deadline unless requested |
| **Multi-domain presets** | Co-founder, hiring, vendor — reuse MOM-TEST engine | Scale phase |
| **Team / accelerator seats** | Shared vaults, observer notes, cohort dashboards | Scale phase |

### Business Challenges (Validated Against Founder Reality)

#### 🔴 Challenge 1: Compliment Culture Masquerades as Validation
**Evidence:** *The Mom Test* and decades of lean practice: "sounds great" and "I'd definitely use that" are free and usually worthless. Startup post-mortems repeatedly cite "no market need" after months of friendly interviews.  
**Impact:** Founders burn time and capital building products nobody will pay for. False positives feel like progress.

#### 🔴 Challenge 2: Founders Cannot Self-Police Questions in the Moment
**Evidence:** Under social pressure, people pitch, ask hypotheticals, and accept fluff. Even people who *read* the book relapse in live conversation.  
**Impact:** Without real-time or post-hoc enforcement of rules, methodology knowledge does not transfer into better data.

#### 🔴 Challenge 3: Insights Die in Notes; Assumptions Stay Implicit
**Evidence:** Notes live in Docs/Notion with no link from quote → assumption → status → next interview. Teams re-interview the same fuzzy questions.  
**Impact:** No compounding learning. No clean go/no-go evidence for co-founders or investors.

#### 🔴 Challenge 4: Research Tools Are Generic, Not Truth-Native
**Evidence:** Tools like Dovetail/Grain help *store and theme* research; they do not systematically enforce past-behavior questions or flag flattery as non-evidence.  
**Impact:** Market gap for a **Mom Test–native** AI product with a sharp, memorable wedge.

### What You Can Build — Solutions with Complexity Assessment

#### Solution 1: Gemini Question Coach (Bad-Question Detector + Rewriter)
| Aspect | Detail |
|---|---|
| **Problem it solves** | "Are my interview questions going to get me lies?" |
| **What it does** | User pastes draft questions or a hypothesis. Gemini scores each question against Mom Test rules, labels failures (hypothetical, leading, opinion-seeking, pitch-in-disguise), and rewrites into past-behavior anchors. Outputs a printable/quick-sheet plan. |
| **Complexity** | 🟢 **Low–Medium** |
| **Why** | Pure LLM classification + rewrite; rules already codified in `engine/01`–`02`. Minimal UI. |
| **Time to MVP** | 3–7 days |
| **Impact** | Instant "aha" demo; easiest first paid feature; strong video clip. |
| **Maps to existing asset** | Engine principles + generation procedure + question bank patterns |

#### Solution 2: Transcript Truth Analyzer (Fact vs Fluff Engine)
| Aspect | Detail |
|---|---|
| **Problem it solves** | "Which parts of this interview are real demand signals?" |
| **What it does** | Ingests transcript text. Labels spans: concrete past fact, generic fluff, hypothetical, compliment, emotion signal, commitment/advancement. Suggests dig-next questions. Summarizes "what you actually learned" vs "what felt good." |
| **Complexity** | 🟡 **Medium** |
| **Why** | Needs reliable structured output, eval fixtures, and clear UX for rationale. Privacy/consent copy required for real customer data. |
| **Time to MVP** | 1–2 weeks |
| **Impact** | Core AI-native ops story: agents **decide** labels in production. |
| **Maps to existing asset** | `02-bad-data-and-digging.md`, good-vs-bad answer tables, note-taking legend |

#### Solution 3: Assumption Vault + Next-Interview Agent
| Aspect | Detail |
|---|---|
| **Problem it solves** | "What do we still not know — and what do we ask next?" |
| **What it does** | Project-scoped assumptions with status (validated / invalidated / needs data). Links evidence quotes. Gemini proposes next interviewees, next questions, and a concrete commitment ask. Human confirms status changes. |
| **Complexity** | 🟡 **Medium** |
| **Why** | Light data model + agent recommendations; trust requires human confirmation UX. |
| **Time to MVP** | 1–2 weeks (can ship thin version with Solution 2) |
| **Impact** | Turns one-off analyses into a product habit; retention driver. |
| **Maps to existing asset** | Learning goals, decision scorecard, commitment ladder |

#### Solution 4: Live Interview HUD + Audio Pipeline
| Aspect | Detail |
|---|---|
| **Problem it solves** | "Help me not pitch *during* the call." |
| **What it does** | Real-time prompts, optional transcription, live fluff alerts. |
| **Complexity** | 🔴 **High** |
| **Why** | Latency, permissions, reliability, multi-platform meeting noise. |
| **Time to MVP** | 4–8+ weeks |
| **Impact** | Differentiating long-term; **not** required to win the first revenue week. |
| **Maps to existing asset** | Guided interview mode ideas from product nodes; note-taking signals |

### SWOT Analysis — Pitching Mom Test AI (Competition + Customers)

#### Strengths
| # | Strength |
|---|---|
| 1 | **Deep proprietary systemization** already exists in MOM-TEST (engine + presets + sample guides) — not starting from a blank prompt. |
| 2 | **Clear ICP and pricing** with day-one charge culture aligned to XPRIZE business-viability judging. |
| 3 | **Natural Gemini workload**: classification, rewrite, structured extraction, multi-step agents — easy to show "AI executes decisions." |
| 4 | **Memorable category story**: fewer dead startups → jobs and economic opportunity (Entrepreneurship & Job Creation). |

#### Weaknesses
| # | Weakness |
|---|---|
| 1 | **No production product or revenue yet** inside a short remaining window (~deadline Aug 17, 2026). |
| 2 | **Brand/legal carefulness** around "Mom Test" naming and book IP — educational use vs trademark/branding risk; final brand TBD. |
| 3 | **Cold-start of real transcripts** until first users trust the tool with interview data. |
| 4 | **Business preset not fully packed** in catalog the way relationship is — must build founder domain pack first. |

#### Opportunities
| # | Opportunity |
|---|---|
| 1 | **Wedge then expand**: founder discovery → PM research → accelerator seats → multi-domain truth engine (co-founder, hiring) using same MOM-TEST architecture. |
| 2 | **Content-led acquisition**: Point Blanc / Mom Test education content nodes already exist as distribution scaffolding. |
| 3 | **Category prize path**: highest-grossing team *in category* also wins $50k — revenue discipline compounds. |
| 4 | **Replicability**: every founder and many PMs need this loop; viral demo = "paste your last interview, see the fluff." |

#### Threats
| # | Threat |
|---|---|
| 1 | **ChatGPT/Gemini generic chat** as "good enough" free alternative if differentiation is only prompts without product memory and workflow. |
| 2 | **Research platforms** adding AI theming without Mom Test rigor — must stay sharp on *truth vs politeness*. |
| 3 | **Privacy sensitivity** of interview data; mishandling kills trust. |
| 4 | **Adoption resistance** — founders who want encouragement more than truth may churn (positioning must attract truth-seekers). |

### Recommended Starting Point

> **Start with Solution 1 + Solution 2 as a single MVP loop.** Do not build live call HUD first. Encode the MOM-TEST engine into Gemini agents, wrap a thin product UI, charge, instrument, film production usage.

| Phase | What | Timeline (indicative) |
|---|---|---|
| **Phase 1 (PoC / MVP)** | Business preset + Question Coach + Transcript Analyzer + thin vault | ~1–2 weeks |
| **Phase 2 (Sell)** | First 5–10 paying users; log/dashboard evidence; prompt hardening | Continuous with Phase 1 |
| **Phase 3 (Submit)** | Demo video from production, narrative, P&L, Devpost package | Before Aug 17, 2026 |
| **Phase 4 (Scale)** | Live HUD, multi-domain presets, team/accelerator plans | Post-deadline |

### Gemini / Google Stack Mapping (Mandate)

| Stage | Google surface | Use in this challenge |
|---|---|---|
| Idea | Gemini App | ICP, messaging, pricing hypotheses |
| Prototype | Google AI Studio | Scoring + transcript agents; "Get Code" export |
| Design | Stitch | Landing + app shells |
| Build | Antigravity / agent-assisted coding | Ship MVP fast |
| Ship | **Google Cloud** + **Gemini API** | Hosting, secrets, logging, production LLM calls |
| Launch | Flow | ≤3 min competition video |
| Grow | Pomelli | Founder-facing posts |

**Technical mandate checklist**

- [ ] ≥1 Google Cloud product in production  
- [ ] ≥1 Gemini API LLM call in the live product  
- [ ] Agent/API logs + dashboards retained as product evidence  
- [ ] Business activity new after May 19, 2026 (disclose reused templates/boilerplates)  
- [ ] Humans vs AI split documented for narrative  

### What the Demo Would Look Like (Pre-Pitch / Video)

1. **Hypothesis in:** Founder types: "Busy parents need an AI meal planner that reduces weeknight stress." Lists 3 assumptions.  
2. **Question Coach:** Gemini rewrites "Would you use an AI meal planner?" → "Walk me through the last three weeknight dinners — what happened, what broke, what did you pay for?" Shows rule violations on the bad question.  
3. **Transcript paste:** A 5-minute synthetic (then real) interview. UI highlights: green facts ("I ordered DoorDash 4 times last week, ~$80"), red fluff ("I'd totally try that"), purple commitment ("I can intro you to two other parents in my group chat").  
4. **Assumption vault:** One assumption → Invalidated (they already solved with a $12/mo app and won't switch); one → Needs data; one → Weak positive with a commitment ask recommended.  
5. **Logs panel (for judges):** Timestamped agent decisions — scores, labels, model version — proving AI-native operations.

**The Pitch**

*"Everyone said your idea was amazing — so why did nobody buy? Mom Test AI runs customer interviews the Mom Test way: it blocks biased questions, labels compliments as non-evidence, and shows which assumptions actually have facts and commitments behind them. Paste your last interview; in under a minute you'll see what you learned versus what just felt good. We're already systemized this method end-to-end in our engine — now Gemini runs the decisions in production for founders who want truth before they build."*

---

## Humans vs AI (Operating Model)

| Humans | AI (Gemini agents) |
|---|---|
| Pick problem, segment, and final go/no-go | Build and score unbiased question sets |
| Run or schedule the interview | Label evidence vs opinion vs flattery in transcripts |
| Own ethics, consent, and customer relationships | Recommend digs, next interviews, assumption status |
| Sell, support, and set pricing | Log decisions for product + competition evidence |
| Override bad model judgments | Draft reports and next-action checklists |

---

## Success Metrics

### Product / learning metrics
- % of draft questions rewritten before interview  
- Ratio of fact-labeled vs fluff-labeled spans on transcripts  
- Assumptions moved to validated/invalidated per project  
- Commitment asks proposed vs obtained (user-reported)

### Competition / business metrics
- Paying seats or packs sold during window  
- Monthly revenue and simple P&L  
- Production Gemini call volume + logged decisions  
- Testimonials + customer contacts for judges  
- Path narrative to 100k founders (distribution + pricing plan)

---

## Risks & Mitigations

| Risk | Mitigation |
|---|---|
| Shipping too much surface area | Hard-lock MVP to plan → analyze → vault |
| Generic LLM substitutes | Product memory + structured vault + Mom Test–specific eval fixtures |
| Naming / IP sensitivity | Educational positioning; prepare alternate brand if needed |
| No users by deadline | Network-first sales; charge pre-order; workshops with founder communities |
| Hallucinated "evidence" | Quote-span grounding; human confirm on assumption status |
| Privacy blowups | Explicit consent, no training on customer data without opt-in, export/delete |

---

## Immediate Execution Checklist

1. **Register / confirm** Devpost + Google Cloud credit eligibility.  
2. **Lock brand + one-liner** for scroll-stopping first frame.  
3. **Mint `business-customer-discovery` preset** in MOM-TEST (or product repo mirror) from engine template — first-class founder domain.  
4. **Build MVP loop** in production: hypothesis → plan → transcript → report → vault.  
5. **Instrument** Gemini decisions + Cloud logs + Stripe.  
6. **Sell** first 5–10 paying users offline/network first.  
7. **Film demo last** from real production usage; assemble Devpost package.

---

## Related Documents

| Doc | Role |
|---|---|
| [`../selected_idea_mom_test.md`](../selected_idea_mom_test.md) | Selection decision + category + pricing |
| [`../details.md`](../details.md) | Competition overview |
| [`../rules_summary.md`](../rules_summary.md) / [`../faq.md`](../faq.md) | Constraints |
| [`../submission_checklist.md`](../submission_checklist.md) | Devpost package |
| [`../technical_capabilities.md`](../technical_capabilities.md) | Gemini stack |
| [`../marketing_strategy.md`](../marketing_strategy.md) | Charge day one |
| `D:\MAJOR-NODES\WORK-SYSTEMS\MOM-TEST\` | Existing system to productize |
| `PROJECT-NODES\...\Mom-Test-Idea` + `Mom-Test-Tool-Idea` | Earlier product feature maps |

---

## Decision Log

| Date | Decision | Owner |
|---|---|---|
| 2026-07-30 | Select Mom Test AI for XPRIZE; category Entrepreneurship & Job Creation | Blue Akash + agent review |
| 2026-08-01 | Author Challenge_1 doc mirroring Supply Chain AI structure; ground in MOM-TEST assets + product gaps | Challenge doc session |

---

*Template parity note: This document mirrors the structure of `Petrochemicals-Challenge/challenges/Challenge_1_Supply_Chain_AI.md` (context → description → data/PoC strategy → business case → solutions with complexity → SWOT → starting point → demo/pitch), adapted from enterprise supply-chain allocation to founder truth-seeking discovery under Build with Gemini XPRIZE constraints.*
