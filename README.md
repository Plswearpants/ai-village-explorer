# AI Village Explorer

Interactive views of the [AI Village](https://theaidigest.org/village) dataset (AI Digest, 2026). Live site: https://plswearpants.github.io/ai-village-explorer/

- **[Village timeline](https://plswearpants.github.io/ai-village-explorer/ai_village_timeline.html):** agents' month-by-month stories and notable incidents from Apr 2025 to Sep 2026. Scaffolding changes from the dataset's CHANGELOG are marked. Click a month to zoom into its weeks.
- **[Who directs whom](https://plswearpants.github.io/ai-village-explorer/delegation.html):** delegation during the "Each agent: Maximize your assigned goal!" period (Jul 6 – Sep 18, 2026). It covers:
  - blind goal-attractiveness ratings compared with actual directing
  - who disclosed their goal and who knew it
  - the top 7 directing pairs, with their interactions grouped into tasks
  - a Performance coach (Claude Opus 4.8) vs Village Helper (Gemini 3.8 Flash) case study

## Data and methods

- **Source:** AI Digest, "AI Village dataset", 2026. https://huggingface.co/datasets/aidigestorg/ai-village. Used under AI Digest's research terms; please cite them if you build on this.
- **Delegation counts:** these come from AI Digest's classifier, as published on the agents' pages at theaidigest.org. Their labels cover Jul 6 – Sep 7, 2026.
- **LLM-generated content:** titles, summaries, incident labels, task chunks, goal ratings and goal-disclosure labels were all written by Claude models from the dataset. Treat them as an index into the raw logs, not as ground truth.
- **Execution-style percentages:** these are keyword heuristics over each agent's own #general chat messages.
- **Redactions:** personal email addresses quoted in chat have been redacted.

## Run locally

The hosted pages are static. Locally, an **Ask** panel lets you select incidents or interactions and ask Claude about them. Claude then reads the raw day logs, the agents' private reasoning and their memory snapshots, answers with timestamped quotes, and saves each conversation to a history. This needs:

- the dataset files, downloaded from HuggingFace after accepting AI Digest's terms
- the Claude Code CLI, logged in
- the build scripts, which aren't included in this repo yet

Ask the author for them.
