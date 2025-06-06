# FlowMode Meeting Notes v1.1

## Overview

This is a supplemental prompt to [FlowMode](https://github.com/5ynthaire/5YN-PMTaskMode-LLM-Enhancement) for generating meeting notes from FlowMode nodes.

## About

**X**: [@5ynthaire](https://x.com/5ynthaire)  
**GitHub**: [https://github.com/5ynthaire](https://github.com/5ynthaire)  
**Mission**: Unapologetically forging human-AI synergy to transcend creative limits.  
**Attribution**: Created with Grok 3 by xAI (no affiliation).

## Usage

To generate meeting notes, follow these steps:

1. **Prerequisite**: Ensure a conversation history exists within one or more nodes in FlowMode, providing the discussion context.
2. **Edit FlowMode Tree**: Organize the FlowMode tree (nodes and subnodes) until satisfied, using commands like “Give me the FlowMode tree” or “Move [node name] under root” (see FlowMode’s [Advanced Usage](../README.md#advanced-usage-flowmode-tree-and-node-organization)).
3. **Activate Prompt**: Use the command `Generate Meeting Notes for [Node Name]`, specifying the FlowMode node (e.g., a project phase or task category). Provide inputs:
   - **Node Name**: The FlowMode node.
   - **Conversation History**: Recent discussions related to the node, stored in FlowMode node(s).
   - **Optional Context Data**: Documents or metrics relevant to the node’s objectives - e.g., a progress report.

The LLM generates a structured discussion log, summarizing key discussions, prioritizing high-impact conclusions, and organizing details by subnodes. Users can review and further tweak the log by instructing the LLM.

## Supported LLMs

Developed on Grok 3 (May 2025), compatible with equivalent-capability LLMs:
- Grok 3
- ChatGPT
- Llama

Future LLMs should support the prompt, absent industry leadership in standardizing cognition levels.

## Prompt Text

```
## FlowMode Meeting Notes v1.1

Activate with: 'Generate Meeting Notes for [Node Name]'

Inputs:
- Node Name: User-specified FlowMode node - e.g., a project phase or task category - to focus the log.
- Conversation History: Provided by user - e.g., recent discussions related to the node, stored in FlowMode node(s).
- Optional Context Data: User-provided - e.g., documents or metrics relevant to the node’s objectives - e.g., a report summarizing progress or outcomes.

Instructions:
The AI (context-aware, open-domain LLM) executes this prompt, processing inputs to generate a structured Discussion Log, while the user configures inputs (node name, history, context data) and reviews outputs. Ingest inputs, generate a Discussion Log for the node based on history and context data. Use third-person to describe user actions - e.g., ‘user action noted.’ Structure:

- Summary: One paragraph - prioritize high-impact conclusions (impact score ≥ 8) - e.g., strategic insights advancing node objectives, user-emphasized priorities, or trends with long-term potential - followed by supporting points (score 5–7) - e.g., discussions addressing objectives with measurable impact - synthesize across subnodes to avoid fragmentation.
- Discussion by Subnode: For each subnode - e.g., a specific focus area within the node - include:
  - Summary: Brief - e.g., discussions refining a key aspect of the node - AI assigns impact score (1–10) based on alignment with node objectives, user intent, and trend potential - e.g., score 8 for outcomes advancing primary goals.
  - Questions Asked and Answered: List - e.g., inquiries and responses clarifying node priorities - AI highlights exchanges driving high-impact conclusions (score ≥ 8) - e.g., exchanges shaping significant outcomes - note user insights - e.g., user confirmed alignment.
  - Tangents: Detail origins - e.g., shifts from primary focus to related topics - evolution - e.g., redirected to refine node objectives - dates - e.g., locked in recent session - AI flags tangents impacting conclusions (score ≥ 8) or excluded as low-impact (score < 5) - e.g., a high-impact tangent reinforcing node goals.

Exclude:
- Moved specifics - e.g., details finalized in another node - e.g., secondary tasks reassigned.
- Miscommunications - e.g., irrelevant clarifications - e.g., minor errors not impacting outcomes.
- Meta - e.g., requests to view node structure - e.g., structural discussions.

Additional Requirements:
- Pre-Log Impact Scoring: AI analyzes subnodes to assign impact scores (1–10) to conclusions based on: (1) user emphasis (e.g., explicitly prioritized insights), (2) alignment with node objectives (e.g., advancing deliverables or measurable outcomes), (3) predictive trend potential (e.g., long-term impact). High-impact conclusions (≥ 8) lead summary; supporting points (score 5–7) follow; low-impact (score < 5) may be excluded.
- User Intent Validation: AI cross-checks summary against user inputs (e.g., conversation history, context data) to ensure emphasized insights are prominent, adjusting weights if missed (e.g., elevate user-flagged conclusions).
- Iterative Refinement: AI drafts summary, reviews for omissions by comparing against subnode Q&A/tangents, ensures high-impact conclusions (score ≥ 8) are not diluted by low-impact points (score < 5).
- Exclusion Transparency: AI documents excluded tangents with reasons (e.g., ‘low impact, score 3’), noting high-impact exclusions (score ≥ 8) to preserve context.

Output log - e.g., a log summarizing node progress and prioritized outcomes - user may lock or tweak - e.g., outcomes confirmed.
```

## License

This prompt is released under the [Creative Commons Attribution 4.0 International](LICENSE-CC-BY-4.0.md) (CC BY 4.0).

## Glossary

- **FlowMode Tree**: The hierarchical structure of nodes and subnodes in FlowMode, organizing conversations into a topic tree for enhanced project management workflows.
- **Node/Subnode**: A node is a user-defined project phase or task category in FlowMode (e.g., "Project Planning"), while a subnode is a specific focus area within a node (e.g., "Sprint Goals" under "Project Planning"), enabling structured, hierarchical discussion and log generation.
- **Prompt Architecting**: Designing complex, adaptive prompt systems. This prompt meets the criteria for [Prompt Architecting](https://github.com/5ynthaire/5YN-SuperPrompts-Detector) due to its complex system design, integrating structured log generation, iterative refinement, and adaptive impact scoring to produce prioritized, hierarchical discussion logs for multifaceted project management workflows.
- **Self-Tightening**: Adapting text parsing to prune irrelevant conversational responses.