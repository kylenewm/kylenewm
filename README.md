# Projects

Note that most of these enable for me to learn about the failure points of models and agentic systems. These include the model taking shortcuts, optimism bias, context drift, bias from self-assessment, silent/cascading failures, lack of continual learning, and much more. 

I have just built an an autonomous coding orchestration system to circumvent this. At a high level, it is a three-layer system that takes a high-level plan and autonomously ships it, handling task execution, multi-model adversarial code review, crash recovery, and session management across 4-5+ hour runs without human intervention.

I am now using the system itself to build the folowing: 

**Continual Learning Multi-Agent System:** Expand on the single-agent system to a multitude of coordinated agents that get learn over time. This system captures what works and what fails across runs and feeds those patterns back into future sessions automatically.

**Real-Time Agent Observability Platform:** Monitoring infrastructure for concurrent autonomous agent runs. Building the tooling to monitor, trace, and intervene across all runs from a single view.

**Agentic Deep Research and Evaluation:** Connecting research agents that find emerging patterns and failure modes directly into the evaluation pipeline, so what the system learns about quality automatically improves how it measures quality going forward.

The end goal of this work is to amplify my producitvity while integrating cutting edge reserach into rapidly improving system, where they system will eventually be most improving itself besides the upfront planning and the code review needed to make sure it scales properly. I'll be posting more on my substack over the coming days as this continues to scale. 

## Projects

### [Claude Code Build-Kit](https://github.com/kylenewm/council-v3)
**Status:** Completed (improved version incorporating pieces of the above soon)  
**Goal:** Expand Claude Code's capabilities to enable building other productivity tools

A set of features on top of Claude Code that addresses its rough edges. Claude Code is powerful but inconsistent. It rushes through tasks, over-engineers simple requests, loses context mid-session, and sometimes claims completion on broken code.

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

A developer observability tool built for the AI-assisted coding era. As product teams increasingly rely on tools like Cursor and Claude Code to accelerate development, a gap emerges: how do you maintain oversight of code you didn’t write line-by-line?

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
