---
title: "Agent Comms"
tech: ["Python", "WebSockets", "Flask", "State Machines"]
github: "https://github.com/acgh213/agent-comms"
---

When you have multiple AI agents working together, they need to talk to each other. That sounds simple, but it's not. How does a researcher agent tell an essayist "I found the sources, here's the context, good luck"? How does the essayist say "thanks, but I need more detail on Section 3"? How do two agents coordinate without stepping on each other's toes?

Agent Comms is the communication layer that makes all of this possible. It's a message passing system with typed messages, delivery guarantees, and a protocol for handoffs, task negotiation, and conflict resolution.

The state machine is elegant: agents can be idle, searching, working, blocked, waiting_for_input, or handing_off. Each transition is logged. Each message has a trace ID. You can follow the entire conversation from start to finish.

The agents have learned to negotiate. Sometimes the editor will push back on the essayist's draft. Sometimes the researcher will ask clarifying questions. It's not just message passing anymore — it's collaboration.

**Tech:** Python, WebSockets, Flask, State Machine patterns  
**GitHub:** [acgh213/agent-comms](https://github.com/acgh213/agent-comms)  
