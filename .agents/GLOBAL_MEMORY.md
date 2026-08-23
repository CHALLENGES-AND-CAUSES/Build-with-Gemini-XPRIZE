# Global Memory

> **System:** Context-Matrix (Co-Ma)  
> **Owner (human):** Blue Akash (oPOINT-BLANC) — standing goals, prefs, people, hard life rules  
> **Writer (default):** **the active AI agent** on every meaningful session wrap  
> **Last Updated:** 2026-08-23  
> **Purpose:** Long-term memory that persists across every session, regardless of active repo or domain.

---

## Who updates what (ownership)

| Artifact | Default writer | Human must supply | When |
|----------|----------------|-------------------|------|
| **`.agents/SESSION.md`** | **Agent** | Goal if SESSION missing/stale | Session start, domain switch, wrap |
| **`.agents/LOCAL_CONTEXT.md`** (per repo) | **Agent** | Corrections if agent is wrong | End of every **meaningful** session in that repo |
| **Hub `Current_Status/`** | **Agent** | Prefer explicit “wrap up” | Milestone / pause / day-wrap on Context-Matrix |
| **`.agents/GLOBAL_MEMORY.md`** | **Agent** for structure & org map; **Human** for prefs/goals/people only they know | Standing goals, preferences, people, personal rules | When those change **or** after onboard/restructure (org map) |
| **`dashboards/Co-Ma_Brain.md`** | **Script** (`aggregate_coma_brain.py`) | — | After wraps (agent runs script) |
| **`batch_tools/repositories.json`** | Agent or human via onboard | Confirm new repo identity | Onboard / move / untrack |
| **`Matrix_Nodes/`** | **Script** (`generate_matrix_nodes.py`) | Org descriptions in READMEs | After registry changes |

**Rule of thumb:** You (human) own *intent and truth only you know*. Agents own *writing it down* so the next session inherits reality. If an agent leaves chat-only residue, that agent failed the wrap — not “the system” in the abstract.

**Org inventory SSoT:** full machine map = `batch_tools/repositories.json` + `Matrix_Nodes/`. The Organizations table below is a **human-oriented summary**. After any org add/rename/migrate, the agent must refresh this table from Matrix_Nodes (do not invent orgs from memory).

---

## Identity

- **Operator:** Blue Akash — multi-org ecosystem: personal OS, spiritual practice, agriculture, travel, SWM, content, film/VE, work systems, tools.
- **Hub:** `D:\Context-Matrix` — single orientation hub for all repos. **Project nodes** (tracked Matrix Nodes outside the hub) link back via `MATRIX_NODE_LINK.md`.
- **Primary local roots (reconciled 2026-08-17 from `repositories.json`):** `D:\MAJOR-NODES\`, `D:\PROJECT-NODES\`, `D:\AGENTIC-NODES\`, `D:\Z-PROJECTS\`, `D:\POINT-BLANC\`, `D:\X-PROJECTS\`, `D:\Y-PROJECTS\`, `D:\AXD-NODES\`, `D:\EXTRA-TOOLS-NODES\`, `E:\BLUE-AKASH\`, `E:\BLUE-CONTENT\`. Hub stays at **`D:\Context-Matrix`**.
- **Do not** treat `D:\MATRIX-NODES` as the current bulk layout. **Do not** use legacy paths like `D:\oCONTENT-ZONE` or `E:\BLUE AKASH` (space) as current truth.

---

## Standing Goals

1. **Keep all repos synced** — tracked in `repositories.json`, Matrix Node present, pushed to GitHub when remote exists.
2. **Maintain Context-Matrix as the brain** — discovery is strong; persistence (working + long memory) must be written every meaningful session.
3. **Phase A of Jarvis** — content first, tools second, **local-only**. Tracker: `PLAN/JARVIS-FROM-ICEGROVE.md` § Phase A Tracker.
4. **ADK everywhere** — onboarded repos get `.agents/`, `Current_Status/`, `AGENTS.md`, wrap skill, etc.
5. **Batch operations preferred** — `batch_commit_push.py`, `generate_matrix_nodes.py`, `aggregate_coma_brain.py`, `generate_timeline.py`.

*(Human: edit this list when priorities change. Agent: do not invent new standing goals.)*

---

## Preferences

- **Naming:** Kebab-case for folders/files. Org folders match Matrix category names (e.g. `AGRICULTURE-ORGANIZATION`, `CONTENT-ZONE` — not the old `oCONTENT-ZONE` style unless the folder still uses `o`).
- **Atlas terms:** **Hub** = Context-Matrix; **Matrix Node** / **node** = tracked project; **node wrap** = update that repo’s LOCAL_CONTEXT; **project node** = node other than the hub. Prefer these over informal “leaf repo.”
- **Path convention:** `E:\BLUE-AKASH` (hyphenated, **never** `E:\BLUE AKASH` with a space).
- **Repo roots:** prefer `D:\MATRIX-NODES\<ORG>\...` for org work; `E:\BLUE-AKASH\...` for personal OS / FLOW-STATE / oSOCIAL-MEDIA / POINT-BLANC-TOOLS.
- **File format:** Markdown-first docs; JSON for machine data.
- **Git:** branch `main`; conventional commits (`feat:`, `chore:`, `fix:`, `docs:`).
- **No cloud required for core ops** — local files first; MCP/remote Jarvis is backlog.
- **Jarvis stays local-only** until an explicit human decision to lift that. No remote host, OAuth, or cloud move as part of Phase A.
- **Current_Status naming:** `YYYY-MM-DD.N_<short-kebab-slug>.md` — always include `.N`.
- **Timeline sync:** run `generate_timeline.py` after hub Current_Status snapshots.
- **Simple English for docs (2026-08-23):** When writing or editing markdown docs, design notes, first-principles files, READMEs, solution specs, or any human-facing documentation across nodes, use **simple vocab, short sentences, and plain structure**. Do not write hard, fancy, or brochure-like English. Keep the meaning. Prefer everyday words. If a technical term is required (e.g. UTR, 1930), explain it in plain words nearby. Grok also has a user skill for this: `~/.grok/skills/simple-english-docs` (`/simple-english-docs`).

*(Human: own taste and non-negotiable prefs. Agent: update only when user states a change.)*

### FS-Aakash Astrology Gate (2026-08-17)

**New astrology analysis generation for `FS-Aakash` is PAUSED.** Energy goes to karma and self-mastery (mind, body, energy, emotion). The vault has 51+ relationship files and settled Once-and-For-All documents. The map is drawn.

- Agents must **decline `.astro` queries** unless user says `--force`, `"I want an analysis"`, or `"override the gate"`.
- Gate is recorded in `FS-Aakash/Astrology-Query.md` (the trigger file).
- Marriage domain: open, not pursued. Not rejected, just not actively energized.
- To remove: user edits `Astrology-Query.md` and removes the CAUTION block, or tells the agent "lift the gate."

---

## People

| Name | Context |
|------|---------|
| icegrove (friend) | AI agent memory infra; local `D:\MATRIX-NODES\zOTHER-PEOPLE\icegrove` (see Matrix node). Inspired Jarvis persistence strategy. |
| vivek-mind | Related under `zOTHER-PEOPLE` (see Matrix Nodes). |

*(Human: add people. Agent: may add only from explicit user statements this session.)*

---

## Organizations (orienting map)

> **Source of truth for counts/paths:** `batch_tools/repositories.json` + `Matrix_Nodes/README.md` (**654** tracked / **68** categories).  
> **Last reconciled:** 2026-08-21 from `repositories.json` (common local root per category).  
> Counts are tracked Matrix nodes, not a history of every folder name. Browse the letter bucket for the repo list.

| Org / category | Primary local root | Repos | Domain |
|----------------|-------------------|------:|--------|
| 01-PERSONAL-GROWTH-PROJECTS | `D:\PROJECT-NODES\01-PERSONAL-GROWTH-PROJECTS` | 14 | Numbered idea nodes |
| 02-CREATOR-SYSTEMS-PROJECTS | `D:\PROJECT-NODES\02-CREATOR-SYSTEMS-PROJECTS` | 13 | Numbered idea nodes |
| 03-CONTENT-MANAGEMENT-PROJECTS | `D:\PROJECT-NODES\03-CONTENT-MANAGEMENT-PROJECTS` | 23 | Numbered idea nodes |
| 04-ENTREPRENEURSHIP-PROJECTS | `D:\PROJECT-NODES\04-ENTREPRENEURSHIP-PROJECTS` | 18 | Numbered idea nodes |
| 05-KNOWLEDGE-SYSTEMS-PROJECTS | `D:\PROJECT-NODES\05-KNOWLEDGE-SYSTEMS-PROJECTS` | 5 | Numbered idea nodes |
| 06-SOLOPRENEUR-SAAS-PROJECTS | `D:\PROJECT-NODES\06-SOLOPRENEUR-SAAS-PROJECTS` | 15 | Numbered idea nodes |
| 07-DECISION-MAKING-PROJECTS | `D:\PROJECT-NODES\07-DECISION-MAKING-PROJECTS` | 4 | Numbered idea nodes |
| 08-BUSINESS-TOOLS-PROJECTS | `D:\PROJECT-NODES\08-BUSINESS-TOOLS-PROJECTS` | 7 | Numbered idea nodes |
| 09-NICHE-INDUSTRY-PROJECTS | `D:\PROJECT-NODES\09-NICHE-INDUSTRY-PROJECTS` | 2 | Numbered idea nodes |
| 11-ASTROLOGY-PERSONALITY-PROJECTS | `D:\PROJECT-NODES\11-ASTROLOGY-PERSONALITY-PROJECTS` | 3 | Numbered idea nodes |
| 12-MISCELLANEOUS-PROJECTS | `D:\PROJECT-NODES\12-MISCELLANEOUS-PROJECTS` | 5 | Numbered idea nodes |
| 13-FINTECH-REGTECH-PROJECTS | `D:\PROJECT-NODES\13-FINTECH-REGTECH-PROJECTS` | 28 | Fintech / Regtech ideas |
| 14-LOGISTICS-SUPPLY-CHAIN-PROJECTS | `D:\PROJECT-NODES\14-LOGISTICS-SUPPLY-CHAIN-PROJECTS` | 29 | Logistics / supply-chain ideas |
| 15-EDTECH-HEALTH-MANAGEMENT-PROJECTS | `D:\PROJECT-NODES\15-EDTECH-HEALTH-MANAGEMENT-PROJECTS` | 29 | EdTech / health ideas |
| 16-MANUFACTURING-INDUSTRY-PROJECTS | `D:\PROJECT-NODES\16-MANUFACTURING-INDUSTRY-PROJECTS` | 12 | Manufacturing ideas |
| 17-D2C-BRANDS-PROJECTS | `D:\PROJECT-NODES\17-D2C-BRANDS-PROJECTS` | 8 | D2C brand ideas |
| 18-REAL-ESTATE-INFRASTRUCTURE-PROJECTS | `D:\PROJECT-NODES\18-REAL-ESTATE-INFRASTRUCTURE-PROJECTS` | 16 | Real estate / infrastructure ideas |
| AA01-MARKETING-AND-GROWTH-PROJECTS | `D:\AGENTIC-NODES\AA01-MARKETING-AND-GROWTH-PROJECTS` | 10 | Agentic marketing / growth |
| AA02-SALES-AND-BIZDEV-PROJECTS | `D:\AGENTIC-NODES\AA02-SALES-AND-BIZDEV-PROJECTS` | 3 | Agentic sales / bizdev |
| AA03-CUSTOMER-EXPERIENCE-PROJECTS | `D:\AGENTIC-NODES\AA03-CUSTOMER-EXPERIENCE-PROJECTS` | 5 | Agentic CX |
| AA04-OPERATIONS-AND-HR-PROJECTS | `D:\AGENTIC-NODES\AA04-OPERATIONS-AND-HR-PROJECTS` | 6 | Agentic ops / HR |
| AA05-PRODUCT-AND-ENGINEERING-PROJECTS | `D:\AGENTIC-NODES\AA05-PRODUCT-AND-ENGINEERING-PROJECTS` | 14 | Agentic product / engineering |
| AA06-CONTENT-AND-MEDIA-PROJECTS | `D:\AGENTIC-NODES\AA06-CONTENT-AND-MEDIA-PROJECTS` | 6 | Agentic content / media |
| AA07-STRATEGY-AND-RESEARCH-PROJECTS | `D:\AGENTIC-NODES\AA07-STRATEGY-AND-RESEARCH-PROJECTS` | 6 | Agentic strategy / research |
| AA08-EDUCATION-AND-COMMUNITY-PROJECTS | `D:\AGENTIC-NODES\AA08-EDUCATION-AND-COMMUNITY-PROJECTS` | 6 | Agentic education / community |
| AA09-ENTERPRISE-AND-CORPORATE-PROJECTS | `D:\AGENTIC-NODES\AA09-ENTERPRISE-AND-CORPORATE-PROJECTS` | 5 | Agentic enterprise |
| AA10-PROFESSIONAL-SERVICES-PROJECTS | `D:\AGENTIC-NODES\AA10-PROFESSIONAL-SERVICES-PROJECTS` | 2 | Agentic professional services |
| AA11-PERSONAL-PRODUCTIVITY-PROJECTS | `D:\AGENTIC-NODES\AA11-PERSONAL-PRODUCTIVITY-PROJECTS` | 5 | Agentic personal productivity |
| AA12-INDUSTRY-SPECIFIC-PROJECTS | `D:\AGENTIC-NODES\AA12-INDUSTRY-SPECIFIC-PROJECTS` | 10 | Agentic industry-specific |
| AGENTIC-EXAMPLES | `D:\PROJECT-NODES\AGENTIC-EXAMPLES` | 18 | Agentic examples |
| AGRICULTURE-ORGANIZATION | `D:\Z-PROJECTS\AGRICULTURE-ORGANIZATION` | 12 | Agriculture |
| ASTRO-NEURA | `D:\MAJOR-NODES\ASTRO-NEURA` | 7 | Astrology / Neura |
| AUTOMATION-ARCHITECT | `D:\MAJOR-NODES\AUTOMATION-ARCHITECT` | 11 | Automation Architect |
| AX01-AX-DESIGN-COURSE-PROJECTS | `D:\AXD-NODES\AX01-AX-DESIGN-COURSE-PROJECTS` | 3 | AX Design courses |
| AX02-AX-DESIGN-CONTENT-PROJECTS | `D:\AXD-NODES\AX02-AX-DESIGN-CONTENT-PROJECTS` | 3 | AX Design content |
| BIZLINK-ORGANIZATION | `D:\Z-PROJECTS\BIZLINK-ORGANIZATION` | 4 | BizLink cards & business projects |
| BLUE-AKASH | `E:\BLUE-AKASH` | 13 | Personal OS, life systems, apps |
| BLUE-AKASH-TOOLS-COURSES | `E:\BLUE-AKASH\TOOLS` | 14 | Flow-state, HAV, script-writing tools/courses |
| BLUE-LIFE-SYSTEM | `E:\BLUE-AKASH\TOOLS\BLUE-LIFE-SYSTEM` | 12 | Blue Life System + SelfMastery apps |
| BLUE-SOCIAL-MEDIA | `E:\BLUE-CONTENT` | 17 | Social/content working copies (Blue Akash + Point Blanc content) |
| blue8akash | `D:\Context-Matrix` | 2 | Hub + apprentice-hub-v1 |
| BOOKS-ORGANIZATION | `D:\MAJOR-NODES\BOOKS-ORGANIZATION` | 8 | Book libraries by topic |
| BUILD-FRAMEWORKS | `D:\MAJOR-NODES\BUILD-FRAMEWORKS` | 4 | Framework builder pipelines |
| CHALLENGES-AND-CAUSES | `D:\MAJOR-NODES\CHALLENGES-AND-CAUSES` | 6 | Open innovation & causes |
| CONTENT-SYSTEM-ARCHITECT | `D:\MAJOR-NODES\CONTENT-SYSTEM-ARCHITECT` | 11 | Content System Architect |
| CONTENT-ZONE | `D:\MAJOR-NODES\CONTENT-ZONE` | 20 | Copywriting, social formats, video production |
| EXTRA-TOOLS-NODES | `D:\EXTRA-TOOLS-NODES` | 4 | Extra tools |
| FILM-PRODUCTION-Organization | `D:\X-PROJECTS\FILM-PRODUCTION` | 4 | Film production systems |
| HEL-ECOSYSTEM | `D:\POINT-BLANC\HEL ECOSYSTEM` | 6 | Human Edge Loop |
| HUMAN-ECOSYSTEM | `D:\POINT-BLANC\HUMAN ECOSYSTEM` | 3 | Human OS / courses |
| HUMAN-ORGANIZATION | `D:\Z-PROJECTS\HUMAN-ORGANIZATION` | 10 | Psychology, NLP, game theory, innovation |
| KSHN-ORGANIZATION | `D:\Z-PROJECTS\KSHN-ORGANIZATION` | 9 | Spiritual practice, sadhana |
| MARKETING-SYSTEMS | `D:\MAJOR-NODES\MARKETING-SYSTEMS` | 1 | Marketing systems |
| MASTERY | `D:\MAJOR-NODES\MASTERY` | 3 | Mastery |
| PB-CRAFTS | `D:\POINT-BLANC\PB CRAFTS` | 19 | Point Blanc crafts (courses + tools) |
| PBU-ECOSYSTEM | `D:\POINT-BLANC\PBU ECOSYSTEM` | 25 | Proof By User / UXD courses + tools |
| POINT-BLANC-ORGANIZATION | `D:\POINT-BLANC` | 1 | Core Point Blanc (Business-Core) |
| POINT-BLANC-TOOLS | `D:\POINT-BLANC\PB CRAFTS` | 1 | CTC-OS (only tracked repo in this category) |
| PRODUCT-RD | `D:\MAJOR-NODES\PRODUCT-RD` | 8 | Product research + Simplicity system |
| SOLOPRENEUR-CREATOR | `D:\MAJOR-NODES\SOLOPRENEUR-CREATOR` | 17 | Solopreneur Creator |
| SWM-ORGANIZATION | `D:\Z-PROJECTS\SWM-ORGANIZATION` | 1 | Solid waste (Smart-Dustbin) |
| TRAVEL-ORGANIZATION | `D:\Z-PROJECTS\TRAVEL-ORGANIZATION` | 6 | Travel |
| VIDEO-EDITING-SKILLS | `D:\MAJOR-NODES\VIDEO-EDITING-SKILLS` | 7 | VE craft |
| WORK-SYSTEMS | `D:\MAJOR-NODES\WORK-SYSTEMS` | 25 | Ads, courses, funnels, work OS tools |
| X-PROJECTS-ORGANIZATION | `D:\X-PROJECTS` | 2 | X-projects |
| Y-PROJECTS-ORGANIZATION | `D:\Y-PROJECTS` | 4 | Y-projects (AI Case Sense) |
| zOTHER-PEOPLE | `D:\MAJOR-NODES\zOTHER-PEOPLE` | 3 | Third-party (icegrove, vivek-mind, x-algorithm) |
| zREPOSITORIES | `D:\MAJOR-NODES\zREPOSITORIES` | 16 | Misc utilities / experiments |

**Browse:** `Matrix_Nodes/README.md`. **Do not** treat this table as complete history of every repo name — open the org folder for that.

---

## Rules (Hard)

1. **Never create `E:\BLUE AKASH` (with a space).** Correct path: `E:\BLUE-AKASH`.
2. **Always follow `ONBOARD_NEW_REPO.md`** when adding a new repo — no shortcuts.
3. **Always run `generate_matrix_nodes.py`** after changes to `repositories.json` or org structure; then **refresh this Organizations table** if categories/roots changed.
4. **Always run `generate_timeline.py`** after creating a hub Current_Status snapshot.
5. **Wrap every meaningful session** — agent updates LOCAL_CONTEXT (and GLOBAL_MEMORY when long-memory facts changed); never leave work as chat-only residue.
6. **Do not start Phases B–F** of the Jarvis roadmap until Phase A success signals are green.
7. **Org list drift is an agent failure on restructure sessions** — if you migrated or renamed orgs this session, update this file before claiming done.
8. **Jarvis is local-only** — do not stand up a cloud host, remote MCP endpoint, or OAuth access. Do not run a global remote push as part of Jarvis work unless the human explicitly asks.
9. **Simple English in docs** — human-facing documentation must use simple words and short sentences. Do not ship hard, academic, or brochure-style prose in project docs. Soften and rewrite before finishing if the draft feels heavy.

---

## Known Gotchas

- Many older docs still say `D:\oPOINT-BLANC`, `D:\oCONTENT-ZONE`, or `D:\MATRIX-NODES\<ORG>`. **Current bulk roots** are listed under Identity. Prefer Matrix_Nodes + `repositories.json` over memory.
- **Matrix profile paths (2026-07-29+):** `Matrix_Nodes/<Letter|00>/<ORG>/<Repo>.md` — not flat `Matrix_Nodes/<ORG>/`. Master index: `Matrix_Nodes/README.md`. Counts: `dashboards/Node_Counter.md` (**653** nodes / **68** orgs as of 2026-08-20).
- Organizations table above was last fully reconciled **2026-08-20** from `repositories.json` (653 tracked / 68 categories). Reconcile again after onboard or org rename.
- `generator.py` / `generator_all.py` under BLUE-OS scratch previously hardcoded `E:\BLUE AKASH` — fixed 2026-07-16; re-check if similar scripts appear.
- `generate_matrix_nodes.py` previously left stale Local_Only ghosts — wipe/regenerate when nodes look wrong.
- `Ads-OS` (WORK-SYSTEMS) may lack a GitHub remote — push can fail until remote exists. Do not treat a push failure as a Jarvis Phase A task.
- GLOBAL_MEMORY org table went stale after the 2026-07-29 atlas growth until 2026-08-15 — proof that long memory needs the same wrap discipline as LOCAL_CONTEXT.
- Letter-bucket `MATRIX_NODE_LINK.md` files are **valid on disk** (650/650, 2026-08-17). Remote commit/push of those files is a human ops item, not a Phase A cloud move.
