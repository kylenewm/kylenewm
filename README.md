# Projects

Note that these projects are just POC-level code to explore the capabalities and limitations of agentics system and modern AI tooling. 

The most recent was I recently built an autonomous coding orchestration system to circumvent key failures with LLMs and agentic systems (in a private repo soon to be published). At a high level, it is a three-layer system that takes a high-level plan and autonomously ships it, handling task execution, multi-model adversarial code review, among other items.

These personal projects towards the bottom were how I learned where models and agentic systems actually break: taking shortcuts, optimism bias, context drift, silent failures, and lack of continual learning, among others. Here is a very high-level diagram displaying the core loop of it. 

<img width="1583" height="803" alt="updated_image" src="https://github.com/user-attachments/assets/342e52f2-2749-4f50-9e72-3af37b0b91df" />

## Projects

### [Claude Code Build-Kit](https://github.com/kylenewm/council-v3)
**Status:** Heavily evolved into the Autonomous Coding Orchestration System above
**Goal:** Expand Claude Code's capabilities to enable building other productivity tools

---

### [Deep Research](https://github.com/kylenewm/personalized-deep-research)
**Status:** Completed
**Goal:** Develop a research product that is more trustworthy than most current deep research providers by optimizing for accuracy over coverage

Deep research with a layered anti-hallucination architecture that searches the web, gathers sources, and generates verified research reports.

This helps overcome trust issues with current deep research agents that often prioritize coverage. I sometimes use when doing research for new product features or higher-level planning.

See: [Example Report: Voice AI Observability](https://kylenewm.github.io/personalized-deep-research/reports/observability_voice_agents_report.html)

---

### [Code Visualizer](https://github.com/kylenewm/code-visualizer)
**Status:** Completed
**Goal:** Understand changes in real time when using AI-assisted coding

A developer observability tool built for the AI-assisted coding era. As product teams increasingly rely on tools like Cursor and Claude Code to accelerate development, a gap emerges: how do you maintain oversight of code you didn't write line-by-line?

CodeFlow helps by:
- Analyzing codebases in real time
- Visualizing function relationships
- Flagging when code drifts from its documentation

It integrates directly with Claude Code, enabling the AI to check its own work against project standards before committing.

---

### [AI Morning Briefing](https://github.com/kylenewm/ai-morning-briefing)
**Status:** Completed (with future iterations)
**Goal:** Streamline and personalize my ingestion of AI-related news

An automated daily briefing system that delivers personalized AI insights every weekday at 9:30 AM ET.

It curates AI articles, summarizes podcasts, and processes newsletters into a single digestible morning update. A future iteration will replace third-party search with my own research module and improve source quality and structure.

## Contact

If you're interested in collaborating or have questions, reach out:
- Email: **kylenewman1214@gmail.com**
- LinkedIn: https://www.linkedin.com/in/kylenewman2023/
- Substack: https://substack.com/@kylenewman1214
