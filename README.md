The following is part of a collection of personal projects I use and iterate on in my day-to-day as a Product Manager, with the goal of improving execution and decision making. 

> **Scope note:** Some of these are less polished because they’re built to pressure-test agentic AI in practice and understand the limits of autonomous coding agents. The goal is MVP-quality output for architectural decisions, Eng/DS collaboration, and parallelizing certain workflows.


## In progress

### Adversarial testing suite
Automated code review using agents across different tools (in simple terms: one model finds bugs in Claude Code output, a third model judges validity to avoid looping critiques, then Claude Code proposes fixes).

Includes a planning option for net-new features. Earlier multi-model planning attempts lacked codebase context and web search, so this version is designed to run end-to-end with less manual intervention.

### Simulation gym
Validates new system features by having multiple Claude Code agents execute tasks, with tests generated outside Claude Code to reduce biased self-evaluation.

The point is to measure whether changes actually improve outcomes, rather than blindly adding features and assuming they help.

### Autonomous workflows with HITL

Parallelizes work across agents where they can attempt a task a series of times before requiring intervention.

This tooling is useful for iterative and subjective tasks (for example: slide decks) where models need several passes.

<details>
<summary><b>Aside from technical complexity, the reason the above are somewhat unique is they're hard to make as an enterprise product. </b></summary>

- **Adversarial testing** requires multiple top IDE tools in the loop. A vendor cannot realistically ship a feature that assumes you are not using their own product.
- **Simulation gym** exists because I’ve seen models construct tests in ways that bias toward the newer feature winning, even when the feature is worse. Using an external runner helps validate assumptions instead of trusting a single tool’s self-evaluation.
- **Autonomous workflows with HITL** are often not worth it for typical users from a compute and UX standpoint. Most people do not want a slide deck to take 20 minutes to generate, and most slide deck users are not technical enough for tooling that requires this level of setup. For me, it’s still worth it because it lets me parallelize work further.

</details>

## Projects

### [Claude Code Build-Kit](https://github.com/kylenewm/council-v3)
**Status:** Completed (improved version incorporating pieces of the above soon)  
**Goal:** Expand Claude Code's capabilities to enable building other productivity tools

A set of features on top of Claude Code that addresses its rough edges. Claude Code is powerful but inconsistent. It rushes through tasks, over-engineers simple requests, loses context mid-session, and sometimes claims completion on broken code.

Council adds:
- Mode injection (switching sgent conext between rapid prototyping,research, and production modes)
- Build frameworks with quality gates
- Path protection for sensitive files
- Multi-agent orchestration with circuit breakers to catch stuck loops
- Multi-model planning where different models critique each other’s approaches

Next step: add a reproducible workflow leveraging adversarial testing outside of Claude Code to mitigate blind spots during planning and reduce test overfitting. Note that some of the above has limitations in complex codebases or longer time horizons, so I’m seeing diminishing returns from continued investment in certain features.

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
