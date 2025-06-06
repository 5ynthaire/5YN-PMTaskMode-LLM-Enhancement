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

## Supported LLMs

Developed on Grok (May 2025), compatible with equivalent-capability LLMs:  
- Grok  
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