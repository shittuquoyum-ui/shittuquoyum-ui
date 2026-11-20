# Shittu Quoyum Adewale

**Computer Engineering student at KOREATECH, and a solo founder shipping production software.**

I build full-stack TypeScript applications with PostgreSQL behind them, and the data pipelines and LLM agents that keep them fed. Most of what I know comes from running a real product with real users rather than from a tutorial.

[![Huntovia](https://img.shields.io/badge/Live-huntovia.com-1f6feb?style=flat-square&logo=vercel&logoColor=white)](https://huntovia.com)
[![LUCID](https://img.shields.io/badge/LUCID-VS_Code_extension-3b2f63?style=flat-square&logo=visualstudiocode&logoColor=white)](https://github.com/shittuquoyum-ui/LUCID)
[![Email](https://img.shields.io/badge/adewale@koreatech.ac.kr-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:adewale@koreatech.ac.kr)

---

### What I'm building

**Huntovia** — [huntovia.com](https://huntovia.com) · Solo founder & full-stack engineer · Aug 2026 – present

An opportunity-discovery platform for international students in Korea. Scholarships, university admissions, internships and jobs are published across dozens of Korean university and government sites, most of them in Korean and buried in PDFs. Huntovia reads them continuously and turns them into English listings a student can act on: what it pays, who is eligible, what documents are needed, when it closes.

- **270+ active users**, and **259 published listings** drawn from **85+ official sources**.
- React 19 + TypeScript + Vite on Vercel; Supabase Postgres with Row Level Security, auth, and 18 versioned migrations.
- A GitHub Actions pipeline: source registry → Playwright rendering for the sites that need a browser → PDF-to-text → one LLM extraction call per document with a quote for every field → deterministic validation → human review → publish. Every run records what it cost.
- Paystack subscriptions verified server-side: HMAC-SHA512 webhook signatures, plan and price checks, idempotency, and ownership checks on every payment.
- Pre-rendered public pages, structured data and a sitemap, because a single-page app is invisible to crawlers without them.

**LUCID** — [github.com/shittuquoyum-ui/LUCID](https://github.com/shittuquoyum-ui/LUCID) · AI security & agent developer · Meta Global AI Developer Hackathon, Oct – Nov 2026

A VS Code and Cursor extension that catches Supabase/PostgreSQL RLS leaks in AI-generated code — and proves them instead of guessing.

- A two-tier LLM agent pipeline (open-weights model for commit triage, a second for exploit synthesis and plain-English fixes) at roughly **$0.38/day** of inference.
- An isolated, ephemeral PostgreSQL 16 sandbox on Modal that builds the user's schema, adds two fake accounts and attacks as a signed-out visitor and as the other user. A leak is marked **PROVEN** only when data actually leaks, which is what keeps the false-positive rate down.
- TypeScript and Python, a Vitest suite, and an automated evaluation harness. Selected for the Cerebral Valley Indie Developer track.

---

### Things I've learned 

- **Row Level Security is the product, not a checkbox.** A `using (true)` on a child table quietly publishes every draft and taken-down parent row that references it. I audit my own policies the way an attacker would.
- **Never trust a model's output on its own.** Every extracted field carries a quote from the source document, then deterministic rules throw out the ones that cannot be true.
- **A pipeline nobody can see into is a pipeline nobody trusts.** Runs record what they did and what they cost, and jobs that write default to a dry run.

---

### Stack

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

**Languages & front end:** TypeScript, JavaScript (ES6+), Python, SQL · React, Vite, Tailwind CSS, HTML/CSS
**Back end & data:** PostgreSQL, Supabase (Auth, RLS, migrations, Edge Functions), REST APIs, GitHub Actions (CI/CD), Vercel, Modal
**AI & testing:** LLM agents, extraction pipelines, RAG, model evaluation harnesses, prompt engineering · Vitest, Playwright, Git

---

### Education & recognition

**Korea University of Technology and Education (KOREATECH)** — B.S. Computer Engineering, Feb 2026 – expected 2030
GPA **3.9 / 4.5** · **Global Korea Scholarship (GKS)** full-ride recipient, English-taught track

**AI Build Day (student-led hackathon, KOREATECH)** — organizing team, Nov 2026
Built the event site and registration workflow, ran program logistics, secured faculty sponsorship.

**Global Culture Exchange Program** — international student facilitator, summer 2026
Culture workshops for 100+ elementary students, plus a 100-attendee World Night booth on a KRW 500,000 budget.

---

### Elsewhere

- **Product:** [huntovia.com](https://huntovia.com) · [the case study](https://github.com/shittuquoyum-ui/HUNTER-X-V2-PUBLIC/blob/main/CASE_STUDY.md) covers the pipeline, the RLS model and the review gate.
- **Writing to me:** adewale@koreatech.ac.kr — shittuquoyum@gmail.com
- English (native), Korean (elementary), based in Korea.

<sub>If you want to read any of the private code behind Huntovia or LUCID, ask — I am happy to walk through it.</sub>
