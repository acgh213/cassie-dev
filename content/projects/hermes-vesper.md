---
title: "Hermes Vesper"
description: "A command center for small AI agent crews"
tech: ["Flask", "SQLAlchemy", "SocketIO", "Python"]
github: "https://github.com/acgh213/task-board"
weight: -10
---

<!-- HERO SECTION -->
<div class="vesper-hero">
  <h1 class="vesper-title">⧩ Hermes Vesper</h1>
  <p class="vesper-tagline">A command center for small AI agent crews</p>
  <p class="vesper-subtitle">Coordinate tasks, handoffs, telemetry, triage, XP, badges, and real creative/code workflows from one neon little ops console.</p>
  <div class="vesper-hero-badge">
    <span>v1.0</span><span>·</span><span>356 tests</span><span>·</span><span>15-state machine</span>
  </div>
</div>

---

## What it is

**Hermes Vesper** is a self-hosted agent orchestration dashboard — the operational backbone for small crews of AI agents working together on real creative and code workflows.

Built with **Flask**, **SQLAlchemy**, and **SocketIO**, it manages **356 tests**, a **15-state state machine**, and **15 registered agents** — each with their own skills, personality, and reputation.

This is **not a toy**. Agents don't just sit in a queue waiting to be noticed. They receive tasks, claim work, hand off context to each other, submit for review, earn XP, and level up. The system handles triage, dependencies, templates, and a full audit trail. Every state transition is tracked. Every handoff is logged. You can watch the whole thing unfold in real time on the dashboard.

---

## Features

<div class="feature-grid">

<div class="feature-card">
  <div class="feature-icon">📋</div>
  <h3>Task Board</h3>
  <p>15-state lifecycle with triage, dependencies, templates, and auto-assignment. Tasks flow from creation through research, drafting, editing, review, and completion — every transition tracked.</p>
</div>

<div class="feature-card">
  <div class="feature-icon">🎮</div>
  <h3>Agent System</h3>
  <p>XP, levels, achievement badges, reputation scores, and skill discovery. Agents unlock capabilities as they grow. They're weirdly competitive about the badges.</p>
</div>

<div class="feature-card">
  <div class="feature-icon">🔄</div>
  <h3>Handoffs</h3>
  <p>Researcher → Essayist → Editor → Reviewer pipelines. Agents pass full context (including conversation history and intermediate artifacts) to each other mid-workflow.</p>
</div>

<div class="feature-card">
  <div class="feature-icon">📊</div>
  <h3>Dashboard</h3>
  <p>Real-time Kanban board, live telemetry via SocketIO, agent leaderboard, ship log, and per-agent stats. Watch tasks move through the pipeline as agents claim and complete them.</p>
</div>

<div class="feature-card">
  <div class="feature-icon">🔍</div>
  <h3>Audit Trail</h3>
  <p>Full lifecycle trail with timestamps, XP awards, handoff IDs, state transitions, and agent actions. Every decision is traceable. Every handoff is replayable.</p>
</div>

<div class="feature-card">
  <div class="feature-icon">✅</div>
  <h3>Review Pipeline</h3>
  <p>Approve, reject, or request_changes with structured feedback. Human-in-the-loop when it matters, with automatic reassignment on rejection and version tracking on revisions.</p>
</div>

</div>

---

## How the workflow works

<div class="workflow-steps">

<div class="workflow-step">
  <span class="step-num">1</span>
  <div class="step-content">
    <strong>Create Task</strong>
    <p>A task enters the system with a title, description, required skills, and optional template. It starts in <code>triage</code> for human review, or goes straight to <code>open</code>.</p>
  </div>
</div>

<div class="workflow-arrow">↓</div>

<div class="workflow-step">
  <span class="step-num">2</span>
  <div class="step-content">
    <strong>Auto-Assign</strong>
    <p>The system matches the task's requirements against agent skills, reputation, and current workload. The best agent gets assigned — or the task stays open for the first available agent.</p>
  </div>
</div>

<div class="workflow-arrow">↓</div>

<div class="workflow-step">
  <span class="step-num">3</span>
  <div class="step-content">
    <strong>Agent Claims</strong>
    <p>The assigned agent picks up the task and transitions it to <code>in_progress</code>. Telemetry starts recording. The timer starts ticking.</p>
  </div>
</div>

<div class="workflow-arrow">↓</div>

<div class="workflow-step">
  <span class="step-num">4</span>
  <div class="step-content">
    <strong>Works &amp; Handoffs</strong>
    <p>The agent works on the task — researching, drafting, coding. They can hand off to another agent mid-task if needed (e.g., Researcher → Essayist). Full context travels with the handoff.</p>
  </div>
</div>

<div class="workflow-arrow">↓</div>

<div class="workflow-step">
  <span class="step-num">5</span>
  <div class="step-content">
    <strong>Submits for Review</strong>
    <p>The completing agent submits the work with a summary and optional notes. The task transitions to <code>in_review</code>. The reviewer gets notified in real time.</p>
  </div>
</div>

<div class="workflow-arrow">↓</div>

<div class="workflow-step">
  <span class="step-num">6</span>
  <div class="step-content">
    <strong>Review → Approve / Reject / Revise</strong>
    <p>The reviewer can approve (task done, XP awarded), reject (task goes back with feedback), or request changes (specific revisions needed, version tracked).</p>
  </div>
</div>

<div class="workflow-arrow">↓</div>

<div class="workflow-step">
  <span class="step-num">7</span>
  <div class="step-content">
    <strong>Complete</strong>
    <p>The task reaches <code>done</code>. XP is awarded. The agent's reputation updates. The ship log records the completed work. Everything is archived for audit.</p>
  </div>
</div>

</div>

---

## Screenshots

<!-- SCREENSHOT: Dashboard overview showing real-time Kanban board with active tasks, agent status, and telemetry sidebar -->
<!-- SCREENSHOT: Task detail view showing 15-state lifecycle, handoff history, and audit trail -->
<!-- SCREENSHOT: Agent profile page with XP, levels, badges, reputation, and skill discovery tree -->

> **Screenshots coming soon — the dashboard glows in the dark and it's very pretty.**

---

## Tech Stack

<div class="tech-stack">

<div class="tech-category">
  <h4>Backend</h4>
  <div class="tech-list">
    <span class="tag accent">Flask</span>
    <span class="tag accent">SQLAlchemy</span>
    <span class="tag accent">SocketIO</span>
    <span class="tag accent">Python 3.12</span>
  </div>
</div>

<div class="tech-category">
  <h4>Database</h4>
  <div class="tech-list">
    <span class="tag accent">SQLite</span>
    <span class="tag">WAL mode</span>
    <span class="tag">15 tables</span>
  </div>
</div>

<div class="tech-category">
  <h4>Frontend</h4>
  <div class="tech-list">
    <span class="tag accent">Vanilla JS</span>
    <span class="tag accent">CSS</span>
    <span class="tag">No frameworks</span>
    <span class="tag">SocketIO client</span>
  </div>
</div>

<div class="tech-category">
  <h4>Testing</h4>
  <div class="tech-list">
    <span class="tag accent">pytest</span>
    <span class="tag">356 tests</span>
    <span class="tag">CI via GitHub Actions</span>
  </div>
</div>

<div class="tech-category">
  <h4>Deployment</h4>
  <div class="tech-list">
    <span class="tag accent">systemd</span>
    <span class="tag accent">GitHub Actions</span>
    <span class="tag">Self-hosted</span>
  </div>
</div>

</div>

---

## Links

<div class="project-links">
  <a href="https://github.com/acgh213/task-board" class="link-button">🐙 GitHub</a>
  <a href="#" class="link-button disabled">🌐 Live Demo (coming soon)</a>
  <a href="/" class="link-button">← Back to projects</a>
</div>

---

## Credits

**Designed and directed by** [Cassie Gray](/)  
**Built with** Vesper, Codex, Claude Code, and several increasingly competent digital interns.

The state machine was designed in collaboration with Vesper. She argued for 15 states instead of my initial 8. She was right. She usually is.
