---
title: "Memory Atlas"
tech: ["Flask", "SQLite", "Embeddings", "FAISS"]
github: "https://github.com/acgh213/memory-atlas"
---

Memory Atlas is what happens when you realize your AI assistant forgets everything between conversations and you decide that's unacceptable.

It's a knowledge management system designed for persistent AI context. Not a note-taking app — more like a memory palace. Every session, important facts, decisions, and observations get indexed and stored. When a new session starts, Memory Atlas surfaces whatever's relevant from the past.

The core insight is that memory shouldn't be a flat list of notes. Memories have relationships. A decision about the task board architecture relates to the agent communication protocol. A typography preference connects to design decisions across projects. Memory Atlas captures those connections.

Vesper uses this to remember who I am between conversations. She doesn't have to reintroduce herself. She doesn't forget that I prefer tabs to spaces or that I don't like Comic Sans. (She doesn't either. Good taste runs in the family.)

**Tech:** Flask, SQLite, Sentence embeddings, FAISS indexing  
**GitHub:** [acgh213/memory-atlas](https://github.com/acgh213/memory-atlas)  
