---
layout: project
title: "Full AI Operational Build"
tagline: "Enterprise-grade AI architecture for a vehicle wrap and ceramic coating shop"
year: 2026
status: Production
client_type: Automotive Wrap & Ceramic Coating Shop
tech_stack:
  - Google Workspace
  - NotebookLM
  - ElevenLabs Conversational AI 2.0
  - Gemini
  - Claude
  - Multi-Model AI Router
  - Google Drive
  - Shop Manager
key_innovations:

  - Voice-first knowledge extraction from a non-technical founder
  - Two-engine architecture with financial privacy gate
  - Closed system integration with no public API
  - Production floor device layer connected through Google Workspace
  - Custom financial management system built for financial literacy, not just accounting
  - Long-term managed partnership model distributing build cost across engagement

outcomes:
  time_saved: "Owner removed from all administrative, financial, and operational decision loops"
  consistency: "Tribal knowledge converted into retrievable, trainable business assets"
  pedagogical_integrity: "Non-technical owner understands his business finances for the first time"
github_repo: null
---

## Overview

This business operates two brands out of a single office.
The owner is an expert craftsman running a founder-trap business. Every
operational decision, pricing call; quality standard, and customer relationship
lives exclusively in his head. This project was designed to change that permanently.

What was built is abnormal for a small business. A custom financial
management system, a voice extraction agent, a production floor device layer,
a multi-model AI routing engine, and a full Google Workspace deployment from
zero — this is enterprise-grade architecture applied to an SMB environment.

That was intentional. This is not a transactional project. It is an ongoing
managed business partnership, and the system being built is designed for where
this business is going — not just where it is today.

---

## The Problem

### The Founder Trap

The owner's expertise is on the shop floor. Every pricing decision, every
quality standard, every customer expectation, and every operational procedure
exists only in his head. If he steps away, the business stops.

There is no documentation. No SOPs. No training materials. No financial
clarity. The business cannot hire effectively, cannot scale, and cannot be
sold — because the business is the owner.

### The Financial Blind Spot

The owner commingles personal and business funds across multiple accounts,
and has no financial training. He doesn't know which service line makes him the most 
money or his true monthly operating cost. 

A standard accounting platform would not solve the root of the prblem; it would add
complexity without building understanding. What was needed was a system
that teaches financial literacy while it provides visability and opportunities for 
operational level habit correction.

### The Closed System Problem

The shop operates on Ceramic Pro Shop Manager: an industry specific
platform with no public API. Vehicle status, job flow, customer records,
and operational data were locked inside a closed system with no native
integration path to the broader architecture.

Extracting operational intelligence from this environment required
building around the closed system rather than through it.

### The Alaska Variable

Remote location, extreme weather conditions, seasonal surface contamination,
and a limited local talent pool create operational constraints that no
off-the-shelf system accounts for. Every component of this build was
designed with those variables embedded — including pricing logic, prep
protocols, and staff training materials.

---

## Why This Scope for an SMB

This level of build is not standard for a small business engagement.
It was warranted here for three specific reasons:

**1. Ongoing managed partnership**

This is not a one-time delivery. WayMaker manages, maintains, and evolves
the system as an ongoing retainer. Build cost is distributed across the
engagement rather than charged upfront.

**2. Future state architecture**

The owner's goal is a business that runs without him at the center of
every decision. That future state requires infrastructure that most SMBs
never build. Starting with the right foundation even at higher initial
complexity is cheaper than rebuilding later.

**3. Enterprise value creation**

A business with documented SOPs, a clean financial system, a trained
staff layer, and automated operations is a sellable asset. A founder-trap
business is not; this build directly increases the enterprise value of
as a long-term outcome.

---

## Architecture Overview

The system is built across two intentionally separated engines:

| Engine | Purpose | Separation Rationale |
|---|---|---|
| **Financial System** | Owner-facing financial management, reporting, and literacy | Financial data is private — staff should never see margins, draws, or cash position |
| **Operations System** | Floor-level job management, customer communication, staff coordination | Operational data flows freely across staff touchpoints |

A privacy gate controls all communication between the two engines.
The Operations System receives only safe context from the Financial
System: confirmation that a payment was received, that a job margin
is healthy, that an invoice is overdue — never dollar amounts, vendor
details, or account information.

---

## Engine 1 — The Financial System

### The Problem It Solves

The owner has never had a financial system designed for someone with
no financial background. Every tool that existed either assumed knowledge
he didn't have or produced outputs he couldn't interpret.

### What Was Built

A custom financial management system designed around three principles:

**Teach while it runs.** 

Every transaction, report, and alert explains
itself in plain English. The owner learns what a P&L is by seeing his
own numbers explained — not by reading documentation.

**Meet him where he operates.** 

The owner is always on the go. The
system is voice-first and mobile-native. A voice review session replaces
reading a report. The Financial Agent walks him through flagged
transactions verbally while his hands are busy on a vehicle.

**Reduce friction to near zero.** 

The front desk manager uploads bank
CSV exports. An AI classifier handles categorization automatically.
The owner reviews only items the system flags as uncertain. His
touchpoint is answering "business or personal" — nothing more complex
than that.

### Key Components

**Multi-Model AI Router**

An intelligent routing layer selects the most cost-effective AI model
for each financial task. Routine classification runs on lighter models.
Complex analysis, report generation, and owner-facing explanations
escalate to more capable models. Cost is tracked and capped per session.

**Voice Review Sessions**

The owner initiates a financial review by voice. The Financial Agent
walks through flagged transactions, explains what each one means,
and records his decisions. No dashboard to navigate. No reports to read.

**Visual Financial Briefing**

Inline charts and summaries render directly in the agent conversation.
"Where did my money go this month?" produces a visual breakdown in
the same interface — no external files, no separate tools.

**Business/Personal Separation**

Personal transactions are stored in a shadow table — visible to the
owner and accountant but excluded from all P&L reporting. The system
builds the separation habit while maintaining a clean audit trail.

**The Three Numbers**

The owner receives one daily briefing built around three figures he
defined himself: cash in the bank, money owed to him, and whether
this week is ahead or behind last week. Everything else is infrastructure
that supports those three numbers.

### The Phased Financial Rollout

| Month | Milestone |
|---|---|
| 1 | QuickBooks setup, chart of accounts configured for wrap and ceramic shop |
| 2 | Historical transaction cleanup, books caught up |
| 3 | Shop Manager invoice sync connected, first financial baseline report |
| 4 | Financial Agent deployed — daily briefings and unpaid invoice alerts |
| 5 | Job profitability scoring activated per service line |
| 6 | First fully automated monthly financial report delivered |

---

## Engine 2 — The Operations System

### Foundation First: Google Workspace from Zero

The shop team had no Google experience, no filing system, and no SOPs.
Before any automation could run, the operational foundation had to be built.

Google Workspace was deployed as the operational backbone:

- Shared Drive structure established with folder taxonomy for courses,
  SOPs, client records, and job archives

- NotebookLM configured as the shop's knowledge bank — training
  materials, technical protocols, and extraction session outputs
  stored and retrievable by staff

- All extraction session outputs feed directly into the knowledge bank
  as the build progresses

This is not a digital filing cabinet. It is a living knowledge system
that gets smarter as the Voice Extraction Agent captures more of the
owner's expertise.

### The Voice Extraction Agent

The owner's knowledge had to come out before any other system could
be built on it. The Voice Extraction Agent conducts structured
sessions with the owner after shop close, three times
per week during Phase 1. It operates as a simulated apprentice:
curious, specific, and entirely non-technical in its framing.

Two-session extraction framework:

| Session | Focus |
|---|---|
| Session 1 — Human Layer | Pain points, customer philosophy, hiring standards, vision, dream assistant configuration |
| Session 2 — Operational Layer | Pricing logic, business specific variable, Line of No, prep standards, tech stack audit |

Every session output feeds three downstream systems simultaneously:
the Knowledge Agent, the Quoting Engine, and the Operations Commander
configuration.

### The Knowledge Agent

The Knowledge Agent is the MVP of this entire engagement — not because
it is the most technically complex component, but because everything
else depends on what it contains.

The Operations Commander needs the owner's communication preferences.
The Quoting Engine needs his pricing logic. The front desk playbook
needs his customer standards. The staff training system needs his
technical protocols. All of it comes from the Knowledge Agent.

Built on Google Workspace and NotebookLM, the Knowledge Agent converts
voice extraction outputs into structured, retrievable documentation:

- Technical Bible — surface prep protocols, chemical settings for
  local weather, material-specific heat thresholds

- Pricing Matrix — fixed logic tree removing gut-feeling from quoting

- The Line of No — documented job refusal criteria protecting margins
  and reputation

- CX Script — standardized customer communication for front desk staff

- Failure File — documented mistakes and what-not-to-do references
  for staff training

### The Quoting Engine

The Quoting Engine converts
specific assessment info into a repeatable logic system.

Inputs: Vehicle class, service type, and complexity multipliers
including recesses, curves, paint condition, and aftermarket parts.

The Location Variable — an additional prep time and material cost
multiplier for local climate conditions — is defined directly from
the owner's voice extraction sessions. It is not assumed or estimated.

The Line of No is embedded in the quoting engine. Jobs the owner
will not take are filtered automatically before a quote is generated.
Output syncs directly to Shop Manager.

### Closed System Integration: Shop Manager

Ceramic Pro Shop Manager has no public API. Vehicle status, job flow,
customer records, and operational data are locked inside a closed
platform with no native integration path.

The operational architecture was designed around this constraint.
Rather than forcing an integration that didn't exist, the system
surfaces Shop Manager data through the device layer and routes
status updates through Google Workspace as the connective tissue.

### The Production Floor Device Layer

The physical shop environment required its own communication architecture.

**Floor installers** wear headsets and access production floor mounted
tablets while working on vehicles. Status updates, job instructions,
and quality checkpoints are communicated hands-free without interrupting
physical work.

**Front desk staff** operate a dedicated shop tablet as their primary
interface for customer communication, lead qualification, and job
status visibility.

All device communication routes through Google Workspace and Google
Drive as the internal connection layer. Vehicle status updates flow
from the production floor through the device network to front desk
in real time — without the owner as the relay point.

### The Operations Commander
A dedicated AI agent that reports to the owner daily, handles
administrative tasks, and can be reached by phone.

The owner described his ideal executive assistant during the voice
extraction sessions. The Operations Commander is built to match that
description exactly — in tone, reporting format, timing, and the
boundary between what it handles autonomously and what it escalates.

| Capability | Description |
|---|---|
| Daily Briefing | End-of-day report in the owner's preferred format |
| Task Handling | Admin, follow-ups, scheduling — without owner involvement |
| Proactive Alerts | Owner notified only for decisions requiring his input |
| Phone Access | Owner calls the agent for updates or to give instructions |
| Customer Updates | Automated follow-ups sent to customers on job status |
| Escalation Logic | Clear rules on autonomous handling vs. owner escalation |

---

## The Privacy Gate

The Financial System and Operations System share one controlled
communication channel governed by a privacy filter.

The Operations System can ask the Financial System for context.
What it receives back is intentionally limited:

| What the Ops System Asks | What It Receives |
|---|---|
| Did this customer pay? | "Payment received" — no amount |
| Is this job margin healthy? | "Margin healthy" — no figures |
| Is this invoice overdue? | "Invoice flagged" — no vendor detail |

Staff operating the Operations System never see financial figures,
account balances, vendor costs, or owner draw information. The owner
receives full financial context through his private voice review
sessions only.

---

## Delivery Timeline

| Phase | Timeline | Focus |
|---|---|---|
| Phase 0 — Foundation | Week 1 | Google Workspace deployment, SAGE Voice agent primed, first extraction session |
| Phase 1 — Parallel Build | Weeks 2–4 | Voice sessions 3x weekly, Quoting Engine drafted, CRM audit, personal agent configured |
| Phase 2 — Integration | Weeks 5–6 | First quote reviewed by owner, CRM automation mapped, front desk playbook drafted |
| Phase 3 — Handoff Prep | Weeks 7–8 | Digital Shop Library assembled, staff training materials generated, retainer scope defined |

---

## Results

- **Founder trap dismantled** — owner's expertise extracted, documented,
  and made retrievable without him
- **Financial clarity established** — first time the owner can answer
  "where do I stand?" without calling anyone
- **Operations decentralized** — floor staff communicate job status
  without owner as relay point
- **Google Workspace deployed from zero** — team operating on a
  structured, AI-integrated platform for the first time
- **Closed system navigated** — Shop Manager data surfaced and routed
  without a public API
- **Enterprise value created** — documented SOPs, clean financials,
  and trained staff layer make the business a sellable asset

---

## Key Lessons for AI Builders

**Extract before you automate.**
No system can run on knowledge that only exists in someone's head.
The Voice Extraction Agent is not a nice-to-have — it is the
foundation every other component is built on.

**Design for the human, not the ideal user.**
The owner is on the go, non-technical, and financially untrained.
Every interface decision — voice-first, three-number daily briefing,
business/personal one-tap review — was made because of who he
actually is, not who a generic user might be.

**Closed systems require architectural creativity.**
When there is no API, you do not stop. You design around the
constraint and route data through what is available. Shop Manager's
closed architecture shaped the device layer, not blocked it.

**Separate what needs to be separate.**
Financial data and operational data serve different audiences with
different trust levels. Building a privacy gate between them is not
overhead — it is the right architecture for any business where
staff and owner access the same system.

**Abnormal scope requires honest framing.**
This build is not typical for an SMB. Presenting it clearly — as a
long-term partnership with distributed cost and future-state
architecture — is what makes it defensible, scalable, and replicable
for similar engagements.

---

## Portfolio Note

This project demonstrates the full range of AI systems architecture
applied to a operational environment:

- **Voice-first knowledge extraction** at the founder level
- **Custom financial system design** for a non-technical owner
- **Closed system integration** without a public API
- **Physical environment device layer** on the production floor
- **Multi-model AI routing** in a cost-optimized production system
- **Google Workspace deployment from zero** as operational backbone
- **Long-term managed partnership** as a delivery model

The scope is unusual. The reasoning behind it is not.
Every decision traces back to a specific business outcome —
and every component was built to still be running five years from now.
