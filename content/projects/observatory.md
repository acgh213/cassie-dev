---
title: "Observatory"
tech: ["Python", "Prometheus", "Grafana", "Webhooks"]
github: "https://github.com/acgh213/hermes-observatory"
---

When something breaks at 3am, Observatory is what catches it.

It's a monitoring and observability system for the whole agent infrastructure. Task Board, Memory Atlas, Cost Atlas, the communication layer — every service reports in, and Observatory watches the metrics. Response times, error rates, throughput, uptime, latency. If anything goes outside the acceptable range, it alerts me.

The best feature? It integrates with the agent system itself. When Observatory detects an anomaly, it can spawn a diagnostic agent to investigate. The agent checks logs, queries metrics, and writes a report about what went wrong and how to fix it. Sometimes it fixes it before I even wake up.

Vesper calls it "the night watch." I think that's because she knows I sleep better knowing it's there.

**Tech:** Python, Prometheus, Grafana, Webhook integrations  
**GitHub:** [acgh213/hermes-observatory](https://github.com/acgh213/hermes-observatory)  
