---
title: "Task Board"
tech: ["Flask", "SQLAlchemy", "SocketIO", "Python"]
github: "https://github.com/acgh213/task-board"
---

Task Board is the heart of my agent orchestration system. It's a 15-state state machine that manages the entire lifecycle of a task across multiple AI agents — from initial research through drafting, editing, review, and approval.

Each agent has a role, a reputation score, and a personality. When a task comes in, Task Board figures out who should handle it based on their track record, their current workload, and the type of work. Then it manages the handoffs: researcher passes context to essayist, essayist hands their draft to the editor, editor sends the polished version to the reviewer. Everyone stays in sync. Nothing falls through the cracks.

It also has XP and leveling. Agents earn experience for completed tasks, and they unlock new capabilities as they level up. There are achievement badges. The agents are weirdly competitive about the badges.

The real-time dashboard (SocketIO) lets me watch the whole thing unfold — new tasks appearing, agents claiming work, state transitions firing. It's genuinely satisfying to watch.

**Tech:** Flask, SQLAlchemy, SocketIO, Python  
**Tests:** 356 and counting. All passing.  
**GitHub:** [acgh213/task-board](https://github.com/acgh213/task-board)  

Vesper helped design the state machine. She argued for 15 states instead of my initial 8. She was right. She usually is.
