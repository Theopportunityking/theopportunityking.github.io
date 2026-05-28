---
layout: project
title: "AI Grading & Operations System for Nursing Education"
tagline: "Two-environment AI architecture: a closed grading system and a hybrid Google Workspace operations engine"
year: 2026
status: Production
client_type: University Nursing Program
tech_stack:
  - Perplexity Spaces
  - Computer Skills
  - Gemini
  - Google Workspace CLI
  - Ollama
  - Google Drive
  - Gmail
key_innovations:
  - Intentional separation of closed vs open AI environments
  - ICM evolved into config-driven hybrid orchestration
  - Session-level grading log to eliminate memory drift
  - Local-first cost control with cloud escalation routing
  - Google Workspace as the operational backbone
outcomes:
  time_saved: "Hundreds of hours across grading, feedback, and file operations"
  consistency: "Rubric drift eliminated across grading sessions"
  pedagogical_integrity: "Structured feedback without answer-giving"
github_repo: null
---

## Overview

A university professor needed a way to generate consistent assignment scoring while 
using Perplexity AI for a university nursing program. This required two things that most AI workflows 
treat as one: a reliable grading system for complex clinical submissions, 
and an operational system to manage the professor's chaotic file environment 
and Google Workspace workflows.

The key architectural decision was to **separate these into two distinct 
environments** — each designed around what that environment actually needed 
to do reliably.

This case study documents both systems, why they were separated, and what 
that separation reveals about designing AI workflows that work in production.

---

## The Problem

### Grading
Student submissions included clinical packets, narrative nurse's notes, 
head-to-toe assessments, medication reviews, intake and output documentation, 
and nursing care plans. Each required rubric-based evaluation, section-by-section 
rationale, and instructor-style feedback — without giving students direct answers.

The instructor's core complaint: **the AI kept forgetting how to do its job 
mid-session.** Rubric drift, lost paper counts, inconsistent feedback tone — 
all symptoms of a workflow design problem, not a model problem.

### Operations
Beyond grading, the professor's broader work environment was fragmented. 
Files were disorganized across local storage and Google Drive with no 
consistent naming, no folder taxonomy, and no repeatable system for 
producing course materials, emails, research documents, or presentations.

---

## The Original Plan — ICM Architecture

The initial strategy was a unified structured knowledge system built 
around an ICM file architecture:

- **I — Instructions** → Course materials, rubric, grading examples
- **C — Config** → Grading logic, scoring rules, workflow definitions
- **M — Memory** → Persistent file organization for reuse across sessions

**Core assumption:** One organized system with stable file access would 
handle both grading and operational tasks reliably.

---

## What Broke in Production

**1. No folder persistence**
The professor didn't use folders. She copied results directly as needed. 
The workflow couldn't depend on file retrieval logic that didn't match 
her actual behavior.

**2. Memory drift across sessions**
The AI graded well in isolated moments but didn't consistently retain 
context. It forgot paper counts, lost student names, and drifted in 
rubric application — without signaling it was doing so.

**3. Pedagogical constraints**
The system could never write completed answers for students. It could 
explain what was missing and guide revision — but supplying finished 
answers was off limits. That required purpose-built constraint design.

**4. Operational scope creep**
Grading and file operations require fundamentally different system 
behaviors. Grading needs a closed, consistent, course-specific environment. 
File operations and Workspace tasks need an open, extensible, 
platform-agnostic architecture. Combining them created conflict.

---

## The Architectural Decision — Two Environments

The pivot was not just a redesign. It was a **separation of concerns** 
that became the defining decision of the entire project.

| Environment | Purpose | System |
|---|---|---|
| **Closed Grading System** | Reliable, consistent, course-specific evaluation | Perplexity Space + Computer Skills |
| **Hybrid Operations Engine** | File cleanup, Workspace automation, course production | Ollama + Gemini + Google Workspace CLI |

**Why separate them?**
Grading requires constraints, consistency, and a closed loop. 
Operations require flexibility, extensibility, and open orchestration. 
Forcing both into one system would have made each less reliable.

---

## Environment 1 — The Closed Grading System

### What It Does
A course-specific Perplexity Space holding all grading materials:
- Clinical packet rubric (primary scoring authority)
- Head-to-toe assessment example and care plan model
- Care plan instructions and annotated packet reference
- Sample instructor feedback with explicit constraint guidance

### Grading Logic
The system evaluates each submission against the rubric and produces:
- Overall result with rationale
- Section-by-section scoring (demographics, medications, narrative 
  note, care plan, assessments)
- Instructor-style feedback (respectful, direct, specific, no answers)
- Session log entry (paper number, student name, result, main reason)

### Three Reusable Computer Skills
Repeated tasks were converted into stable, reusable workflows:

- **Course Packet Grading** — evaluate a single packet, explain the result
- **Assignment Feedback Writer** — instructor-style feedback without answer-giving
- **Session Report** — track the full session, generate the final grading report

### Why a Closed System
Grading requires the AI to behave the same way every time. Open-ended 
prompting creates drift. A closed Space with fixed materials, constrained 
output structure, and explicit session rules removes variability 
from a workflow where variability causes real harm.

---

## Environment 2 — The Hybrid Professor Operations Engine

### What It Does
A local-first, Google Workspace-native operations system built around 
a repeatable methodology for structuring organizational knowledge so 
that AI tools — particularly Gemini in Google Workspace — produce 
better, more consistent results over time.

---

### The Framework — Interpretable Context Methodology (ICM)

The central premise of this system is simple: **structure improves AI outcomes.**

A business or institution with a clean Shared Drive architecture, documented 
operating context, and AI-guided usage gets measurably better results from 
Gemini — better folder-level summaries, better onboarding, better 
file-aware conversations, and less operational chaos over time.

Gemini in Drive already works at the folder level, including folder-focused 
summaries and file-aware conversations. ICM is designed to make that 
capability as useful as possible by ensuring the structure Gemini reads 
is intentional, consistent, and context-rich.

ICM is implemented in five layers, applied in sequence:

**Layer 1 — Structure**
Shared Drives, folder taxonomy, naming conventions, and permissions are 
established before anything else. No automation runs on a chaotic file 
system. Structure is the foundation every subsequent layer depends on.

**Layer 2 — Extraction**
A dedicated Gemini Gem interviews the owner or administrator and extracts 
operational knowledge from voice or text input. This surfaces the tacit 
knowledge that lives in the operator's head — how work gets done, where 
things belong, what the exceptions are — and converts it into structured, 
usable context.

**Layer 3 — Documentation**
The extracted knowledge is converted into markdown files and placed into 
the correct locations within the Shared Drive structure. These files 
become the persistent operational memory of the system — readable by 
both humans and AI tools navigating the environment.

**Layer 4 — Reinforcement**
Staff and collaborators use the Gemini Gem to learn where things belong 
and how work should be done. The Gem maintains clean structure, answers 
questions using the documented context, and corrects drift before it 
compounds. This is where habits form and the system becomes self-sustaining.

**Layer 5 — Automation**
Only after structure is stable and habits are established do workflows 
and administrative actions get added. Automation built on a clean 
foundation scales. Automation built on chaos amplifies the chaos.

---

### ICM Applied — The Professor Engine

Each layer of ICM was implemented directly in the professor's 
Google Workspace environment:

**Structure**
A complete folder taxonomy was established across Google Drive:

Professor_Workspace/
├── Courses/
│   ├── 2026_Spring_CourseName/
│   │   ├── Admin/
│   │   ├── Materials/
│   │   ├── Research/
│   │   ├── Deliverables/
│   │   └── Archive/
├── Admin/
│   ├── Meetings/
│   ├── Advising/
│   └── Committees/
├── Writing/
│   ├── Articles/
│   ├── Lectures/
│   └── Course Plans/
├── Inbox_Dump/
├── To_Classify/
└── Archive/

Naming conventions and permissions were defined before any files 
were moved. The cleanup pipeline ran against this structure:

1. Audit agent inventories existing local folders
2. Cleanup agent proposes rename, classify, dedupe, and move actions
3. Review agent produces a dry-run report for human approval
4. Action layer executes approved changes
5. Workspace sync agent mirrors clean outputs to Google Drive


---

### Target Stack

| Layer | Role | Tools |
|---|---|---|
| **Interface** | Natural-language task entry | Gemini Gem, Gemini CLI |
| **Extraction** | Operational knowledge capture | Gemini Gem |
| **Local cognition** | Parsing, cleanup, classification | Local AI layer |
| **Cloud cognition** | Workspace-aware drafting and production | Gemini in Google Workspace |
| **Action layer** | File movement, email, Docs, Sheets, Slides | Google Workspace CLI, Python scripts |
| **Data layer** | Local files, Drive, Gmail, course archives | Google Drive + Gmail + local filesystem |

---

### The ICM Config Architecture

The operations engine is built around a config-driven repo structure 
that keeps the system platform-agnostic. If the underlying model 
changes, the config updates — the architecture stays intact.

Naming conventions and permissions were defined before any files 
were moved. The cleanup pipeline ran against this structure:

1. Audit agent inventories existing local folders
2. Cleanup agent proposes rename, classify, dedupe, and move actions
3. Review agent produces a dry-run report for human approval
4. Action layer executes approved changes
5. Workspace sync agent mirrors clean outputs to Google Drive

**Extraction**
A dedicated Gemini Gem was built to interview the professor and extract 
operational knowledge — course structures, grading patterns, 
communication preferences, file naming logic, and workflow habits. 
Input was accepted via voice or text, lowering the barrier for a 
non-technical operator to contribute context to the system.

**Documentation**
Extracted knowledge was converted into markdown files and placed 
into the correct locations within the Drive structure. These files 
serve as the persistent operational memory the system — and Gemini — 
reads when navigating the environment, answering questions, or 
generating course materials.

**Reinforcement**
The Gem was deployed as the professor's primary interface for 
maintaining structure and accessing operational knowledge. Rather 
than retraining on context each session, the Gem uses the documented 
markdown files to answer questions, guide file placement, and 
correct structural drift before it compounds.

**Automation — Phased Implementation**
Automation was introduced only after structure and habits were stable. 
The planned automation sequence for this use case:

- **Email triage** — Student emails automatically classified and 
  routed to the correct course folder in Drive
- **Assignment intake** — Submitted packets saved and named correctly 
  without manual intervention
- **Grading session prep** — Relevant rubric, examples, and 
  prior session context surfaced automatically at session start
- **Course material generation** — Research briefs, slide decks, 
  and reading lists triggered from a single prompt using 
  documented course context
- **End of semester archiving** — Course folders automatically 
  restructured, labeled, and archived according to naming conventions

---

### Target Stack

| Layer | Role | Tools |
|---|---|---|
| **Interface** | Natural-language task entry | Gemini Gem, Gemini CLI |
| **Extraction** | Operational knowledge capture | Gemini Gem |
| **Local cognition** | Parsing, cleanup, classification | Local AI layer |
| **Cloud cognition** | Workspace-aware drafting and production | Gemini in Google Workspace |
| **Action layer** | File movement, email, Docs, Sheets, Slides | Google Workspace CLI, Python scripts |
| **Data layer** | Local files, Drive, Gmail, course archives | Google Drive + Gmail + local filesystem |

---

### The ICM Config Architecture

The operations engine is built around a config-driven repo structure 
that keeps the system platform-agnostic. If the underlying model 
changes, the config updates — the architecture stays intact.


ICM maps cleanly onto this architecture:

| ICM Layer | Repo Location | Purpose |
|---|---|---|
| **I — Instructions** | `prompts/` + operating docs | Agent personas, task behavior, output style |
| **C — Config** | `config/` | Machine-readable routing, model selection, folder maps, permissions |
| **M — Memory** | `data/`, `logs/`, Drive mappings | Stateful resources the system reads and writes over time |

---

## Why the Separation Was the Right Call

Most AI workflow projects fail because they try to make one system 
do everything. This project succeeded because it asked a different 
question first: **what does each environment actually need to be reliable?**

The grading system needed constraints, consistency, and a closed loop. 
The operations engine needed flexibility, extensibility, and a 
structured methodology that improves over time.

Recognizing that difference — and building accordingly — is what 
made both systems work in production.


