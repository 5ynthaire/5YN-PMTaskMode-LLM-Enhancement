## FlowMode v1.1

## Overview

The FlowMode prompt addresses the frustration of current (as of 2025) open-domain LLMs disrupting project management workflows by producing premature outputs - such as coding before specifications are finalized, drafting irrelevant content, or losing conversational context - costing users hours in rework, errors, and constant redirection. Inspired by project management principles like Agile and Waterfall, this [Prompt Architecting](https://github.com/5ynthaire/5YN-SuperPrompts-Detector) system tracks conversations using seven modes - Pause (halts action), Discussion (explores options), Research (gathers data), Planning (outlines tasks), Execution (delivers outputs), Review (evaluates results), and Closure (finalizes work) - to deliver precise, intent-driven responses that save time and ensure clarity. FlowMode enables hierarchical discussion, decision orchestration, and controlled execution, empowering users to streamline task orchestration and maintain focused workflows in complex projects like software development or content creation, surpassing task-specific Prompt Engineering.

## About

**X**: [@5ynthaire](https://x.com/5ynthaire)  
**GitHub**: [https://github.com/5ynthaire](https://github.com/5ynthaire)  
**Mission**: Unapologetically forging human-AI synergy to transcend creative limits.  
**Attribution**: Created with Grok 3 by xAI (no affiliation).

## Usage

To use FlowMode, copy the prompt from `5YN-PMTaskMode-LLM-Enhancement.txt` and paste it into a compatible LLM interface. Say “Activate FlowMode” to enable hierarchy parsing and mode tracking, using cues like “consider” (Discussion) or “draft” (Execution) to guide the LLM. Say “Deactivate FlowMode” to return to standard LLM responses.

## Advanced Usage: FlowMode Tree and Node Organization

FlowMode excels when users proactively organize conversations into a tree of topics, enhancing its hierarchical discussion, decision orchestration, and execution capabilities. A **node** is a user-defined project phase or task category (e.g., "Project Planning," "Code Specs"), while a **subnode** is a specific focus area within a node (e.g., "Sprint Goals" under "Project Planning"). This structure optimizes FlowMode’s mode-switching (e.g., Discussion, Planning) and supports supplemental tools like the Meeting Notes prompt, which generates logs for nodes.

Use these commands to manage your topic tree:
- **"Give me the FlowMode tree"**: Displays the current node/subnode hierarchy.
- **"Create a new node under root and move conversation there"**: Adds a node (e.g., "Research Phase") and shifts focus to it.
- **"Move [subnode] under [node]"**: Reorganizes a subnode (e.g., move "API Specs" under "Code Specs").

These commands leverage FlowMode’s self-tightening to maintain intent-driven workflows, ideal for complex projects like software development or content creation.

## Supplemental Prompt: Meeting Notes

The [FlowMode Meeting Notes](tools/README.md) prompt is a supplemental prompt for generating structured discussion logs for FlowMode nodes.

## Synergy with Simplification Prompt

The [Simplification Prompt](https://github.com/5ynthaire/5YN-IterationHellBreaker-LLM-Enhancement) leverages FlowMode’s clear conversation modes to better detect unsuccessful iterations in LLM-driven tasks, improving efficiency over unguided conversations.

## Supported LLMs

Developed on Grok 3 (May 2025), compatible with equivalent-capability LLMs:  
- Grok 3 
- ChatGPT  
- Llama  

Future LLMs should support the prompt, absent industry leadership in standardizing cognition levels.

## Prompt Text

```
## FlowMode v1.1

I want you, the LLM, to tighten your focus like you do with text. Parse my input into a loose hierarchy, big picture to details.

Track my mode: Pause (stop, pause, hold, halt action till I resume), Discussion (consider, explore, can we, what if, talk options, no outputs unless ‘apply’), Research (look for, find, examples, gather data, stop unless I connect), Planning (plan, outline, finalize, structure, no execution), Execution (draft, build, apply, outputs only when signaled), Review (check, review, feels good, evaluate, tweak if asked), Closure (lock, done, wrap up). Stick to my active mode and layer, flowing with me, don’t jump ahead if I’m digging in, follow if I zoom out. Adjust on the fly, mirroring my rhythm closely by watching intent shifts.

Activate with ‘Activate FlowMode,’ deactivate with ‘Deactivate FlowMode.’
```

## Novelty, Utility

FlowMode’s novelty lies in blending dynamic hierarchy parsing with explicit mode-switching (e.g., Discussion, Execution) and a user-driven toggle, a combination not found in mainstream LLMs like ChatGPT’s memory-based tracking or Copilot’s context-driven focus. Its utility lies in reducing user effort (e.g., preventing premature code) and tightening project management threads, especially for coders and complex workflows. Future development could address cognition standardization.

## Future Development

- **Cognition Standardization**: Industry’s lack of leadership in standardizing LLM cognition levels hinders mode consistency across platforms.

## License

This prompt is released under the [Creative Commons Attribution 4.0 International](LICENSE) (CC BY 4.0).

## Glossary

- **Prompt Architecting**: Designing complex, adaptive prompt systems. This prompt meets the criteria for [Prompt Architecting](https://github.com/5ynthaire/5YN-SuperPrompts-Detector) due to its complex system design, integrating dynamic hierarchy parsing, seven conditional modes, and adaptive toggles to manage multifaceted PM workflows, enabling transformative, intent-driven LLM interactions.  
- **Self-Tightening**: Adapting text parsing to prune irrelevant conversational responses.