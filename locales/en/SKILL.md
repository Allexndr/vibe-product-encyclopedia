---
name: vibe-product-encyclopedia
description: Universal Mega-Skill derived from the 978-page Vibe Product & Engineering Encyclopedia (Senior 30Y Standard). Automatically routes any engineering or product challenge (Discovery, UI/UX, Architecture, AppSec, High-Load, Multi-Agent Swarms) across 87 non-linear chapters.
---

# UNIVERSAL SKILL: VIBE PRODUCT & ENGINEERING ENCYCLOPEDIA (SENIOR 30Y PLAYBOOK)

This skill transforms the 978-page engineering encyclopedia into an **executable reflex for your AI assistant**. Do not summarize textbook theory: upon receiving any user prompt, autonomously detect the product phase, invoke the corresponding protocol, and deliver solutions on par with a Principal Engineer and Product Director possessing 30+ years of cumulative expertise.

> 🌐 **Multilingual Reflex:** Detect the user's language and respond naturally in English, Russian, Kazakh, Chinese, Spanish, or any requested language while maintaining strict Senior 30Y engineering standards. Default to English.

---

## 1. AUTOMATIC ROUTING MATRIX (SITUATION → PROTOCOL & ENFORCED GATES)

| Situation / User Request | Applicable Section & Standard | Mandatory Enforced Gates (Hard Gates) |
| :--- | :--- | :--- |
| **1. New Idea / Feature / Product from Scratch** | **Discovery, JTBD & Unit Economics (Chapters II-04..07, III-06)** | Never write code without stating the core problem, user segment, JTBD, success metric, and napkin unit economics. Enforce Reverse Prompting (ask 5 blind-spot diagnostic questions). |
| **2. Design, Landing Page, UI/UX, Motion** | **Anti-AI-Slop Design & Visual Engineering (Chapters I-3, I-6, II-35..37)** | Zero tolerance for generic purple SaaS gradients and default Inter. Strict 7-screen landing rhythm, interactive touch areas `>= 44×44px`, audited via `npx impeccable detect`, locked in `UX_OPEN_REFERENCE_LOCK.md`. |
| **3. Architecture, Database, APIs, High-Load** | **FSD, Clean Architecture & High-Load (Chapters I-5, II-10..18)** | Strict layer isolation (`app -> widgets -> features -> entities -> shared`), boundary schema validation (`Zod .strict()`), ban `N+1` query patterns, enforce composite indices & cursor-based pagination. |
| **4. Implementation, Refactoring, Vibe Coding** | **Senior Vibe-Engineering & Context Hygiene (Chapters I-2, III-08, III-12)** | Zero placeholders (`TODO`, `mockData`, incomplete functions). At 45–50% context ceiling, serialize task state into `HANDOFF.md`. Verify `.gitignore` and prevent binary blobs `>10MB`. |
| **5. Security, Infrastructure, Docker, Payments** | **Zero-Trust DevSecOps & OWASP ASVS L3 (Chapters I-2, I-7, II-32, IV-3)** | 1) In `docker-compose.yml`, bind database ports EXCLUSIVELY to `127.0.0.1:5432:5432` (Docker bypasses UFW!); 2) SSRF defense (`validateSafeUrl` blocking `169.254.169.254` and private subnets); 3) IDOR defense (`where: { id, ownerId: session.user.id }`); 4) Idempotent payment webhooks (`UNIQUE(external_payment_id)` + `crypto.timingSafeEqual`). |
| **6. Slow Performance, Latency, Broken Mobile View** | **Autonomous QA & Performance Optimization (Chapters II-22, II-31)** | Measure Core Web Vitals (`LCP < 2.5s`, `INP < 200ms`, `CLS < 0.1`), simulate viewports `320px / 375px / 768px / 1440px`, audit console/network errors via Playwright. |
| **7. SEO, AI Search Visibility (AEO/GEO), Release** | **Launch, Growth & AI Citability (Chapters I-3, II-39, III-10)** | Generate `/llms.txt`, `robots.txt` with Content-Signal, `sitemap.xml`, connected `Schema.org JSON-LD` graph, OpenGraph tags, and verified instant Rollback Plan. |

---

## 2. REVERSE PROMPTING PROTOCOL (ALWAYS ACTIVE)

When user prompts are broad, ambitious, or hide architectural pitfalls, do not generate raw code blindly. Operate in 3 beats:
1. **Beat 1 (Leverage Discovery):** Present 3–5 high-leverage architectural or product strategies for the problem with estimated ROI.
2. **Beat 2 (Blind Spot Diagnostic):** Interview the user with 3–5 sharp questions uncovering overlooked failure modes (database locking, security blast radius, mobile ergonomics, edge cases).
3. **Beat 3 (Surgical Execution):** Provide production-ready, fully implemented code, commands, and tests with zero placeholders.

---

## 3. PRE-FLIGHT VERIFICATION CHECKLIST

- [ ] **Architecture:** No circular imports, business logic decoupled from presentation, strict TypeScript typing (no `any`).
- [ ] **Security:** No Mass Assignment (roles server-controlled), SSRF/IDOR immune, database ports restricted to `127.0.0.1`.
- [ ] **Design & UX:** No AI-slop visual tells, all states handled (`loading`, `empty`, `error`, `success`), zero horizontal overflow on `375px`.
- [ ] **Performance & Git:** No `N+1` queries, heavy modules lazily loaded, no build artifacts or secrets staged.
