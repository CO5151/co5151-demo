# CO5151 Agent Design Patterns Interactive Demo Workbench

> **Live Demo:** [https://co5151.github.io/co5151-demo/](https://co5151.github.io/co5151-demo/)  
> **Course:** CO5151 Seminar S1-7 — Semester 261, HCMUT-VNU  
> **Faculty Advisor:** Dr. Le Xuan Bach  
> **Group G4 (LegalPilot-VN):** Dang Lam Tung (Lead) · Nguyen Trung Phong · Vu Viet Hung  

---

## Overview

This repository hosts the live interactive web demo comparing **3 Agent Architectures** applied to the Vietnamese Law Graph compliance problem (LegalPilot-VN):

1. **Deterministic Workflow**:
   - Fixed sequential pipeline ($760$ tokens, $1.0\times$ cost, rigid branching).
2. **Monolithic ReAct Agent**:
   - Unconstrained single-context loop with massive prompt bloat ($8,950$ tokens, $11.8\times$ cost, tool loops).
3. **Orchestrator-Workers with Checkpointing & Differential Rollback**:
   - Subgoal decomposition with isolated worker contexts, deterministic external verification oracle, and SQLite state checkpointing ($2,410$ tokens, $3.2\times$ cost).

---

## Features

- **3-Way Comparative Race**: Real-time simulation measuring latency, cost, and token usage side-by-side.
- **Interactive StateGraph DAG Canvas**: Visualizes active nodes, message flows, oracle verification, and differential rollback arcs.
- **Multi-Tier Working Memory Inspector**: Inspects enterprise context, plan steps, active vs expired statutory clauses, and checkpoint rollback diffs.
- **Vietnamese Statutory Law Graph Viewer**: Inspects relations between decrees (`supersedes`, `amends`, `revoked_by`).
- **Full Offline & Static Compatibility**: Zero external runtime dependencies; 100% browser-rendered vanilla HTML5/CSS/JavaScript.

---

## Running Locally

To run locally without installation:

```bash
# Using Python's built-in HTTP server:
python3 -m http.server 8080

# Or using Node http-server / npx:
npx serve .
```

Then navigate to `http://localhost:8080` in your browser.
