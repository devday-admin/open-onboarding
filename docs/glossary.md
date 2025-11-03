# AI-Assisted Development Glossary

Common terms you'll encounter when using AI tools for onboarding.

## AI Tools & Platforms

**Claude Code**
> Official command-line interface for Claude AI. Used for interactive coding assistance through conversation.

**Cursor**
> AI-powered code editor (fork of VSCode) with built-in AI chat and code completion.

**Cline**
> VSCode extension that provides Claude AI integration with memory persistence across sessions.

**Codex / Autonomous Agents**
> AI systems that can work independently for extended periods with minimal human intervention.

**MCP (Model Context Protocol)**
> Standardized way for AI models to access external tools and services securely. Preferred over Skills for production use.

## Configuration Terms

**CLAUDE.md**
> Configuration file for Claude Code that gets injected into every conversation. Lives in `~/.claude/CLAUDE.md` (global) or `.claude/CLAUDE.md` (project-specific).

**.cursorrules**
> Configuration file for Cursor that defines AI behavior rules and conventions.

**.clinerules**
> Configuration file for Cline that sets up memory banks and context management.

**Output Style**
> Session-level configuration in Claude Code that changes how Claude communicates (verbose, concise, software-architect, etc.).

**Slash Commands**
> Quick commands (like `/review` or `/refactor`) that inject predefined prompts into a single interaction.

**Skills**
> Autonomous tools that Claude Code can invoke. ⚠️ Use with caution - has security implications.

**Sub-Agents**
> Isolated conversations that Claude spawns to handle complex tasks independently while maintaining your project context.

## Onboarding-Specific Terms

**First Week Config**
> AI configuration designed for new developers in their first 1-2 weeks. Emphasizes explanation, safety, and learning.

**Pair Programming Config**
> AI configuration that acts as a mentor during coding sessions. Teaching-focused and interactive.

**Codebase Explorer Config**
> Read-only focused configuration for safely exploring and understanding unfamiliar code.

**Onboarding Buddy**
> Cursor's mentorship-style configuration for new developers.

**Context Pollution**
> When too many configurations or instructions confuse the AI or consume too much context window, leading to degraded performance.

## AI Interaction Terms

**Context Window**
> The amount of text (measured in tokens) that the AI can "remember" and work with at once. Larger is better but costs more.

**Token**
> Basic unit of text processing for AI. Roughly 1 token = 0.75 words. Context limits are measured in tokens.

**Prompt**
> The input/question/instruction you give to the AI.

**System Prompt**
> Hidden instructions that tell the AI how to behave. Your CLAUDE.md content becomes part of this.

**Few-Shot Learning**
> Providing examples in your prompt to show the AI what you want. Example: "Like this file: X, create Y"

**Chain of Thought**
> When AI "thinks out loud" by explaining its reasoning step-by-step.

## Development Workflow Terms

**Trunk-Based Development**
> Git workflow where everyone commits to main branch frequently with short-lived feature branches.

**Standard Development Workflow (SDW)**
> Team's established process for making code changes from planning to deployment.

**Definition of Done (DoD)**
> Checklist that defines when a task is truly complete (code written, tested, reviewed, documented, deployed, etc.).

**Technical Debt**
> Code that works but needs improvement. Shortcuts taken that will need fixing later.

**Code Smell**
> Pattern in code that suggests a deeper problem. Not a bug, but indicates poor design.

## Code Quality Terms

**DRY (Don't Repeat Yourself)**
> Principle of avoiding code duplication. Extract repeated code into reusable functions.

**SOLID Principles**
> Five design principles for maintainable object-oriented code: Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion.

**Refactoring**
> Improving code structure without changing its behavior. Making code cleaner, more readable, or more maintainable.

**Linting**
> Automated code analysis to find potential errors, style violations, or anti-patterns.

**Test Coverage**
> Percentage of code that is tested by automated tests. Higher coverage = more confidence in changes.

## AI-Assisted Development Patterns

**Explain Before Modify**
> Pattern where AI explains what it will change and why before making changes.

**Safe Exploration**
> Read-only codebase investigation without making changes. Good for learning.

**Gradual Complexity**
> Starting with simple tasks and progressively tackling more complex work as skills grow.

**Teaching-Style Response**
> When AI explains concepts thoroughly with context, examples, and reasoning (vs. just giving answers).

**Confirmation Prompts**
> When AI asks for permission before taking actions that could modify code or state.

## Common Acronyms in AI Tools

**LLM (Large Language Model)**
> AI model trained on vast amounts of text. Claude, GPT-4, etc.

**IDE (Integrated Development Environment)**
> Software for writing code (VSCode, JetBrains, etc.). Cursor is an AI-powered IDE.

**CLI (Command Line Interface)**
> Text-based interface for running commands. Claude Code is a CLI tool.

**API (Application Programming Interface)**
> Way for programs to talk to each other. Cline uses Claude's API.

**QA (Quality Assurance)**
> Team/process for testing software quality. Also refers to testing itself.

**CI/CD (Continuous Integration/Continuous Deployment)**
> Automated pipeline for testing and deploying code changes.

**PR (Pull Request)**
> Proposed code changes submitted for review before merging to main branch.

## Onboarding Progression Terms

**Week 1 Goals**
> Understanding architecture, exploring safely, making small changes with guidance.

**Week 2-4 Goals**
> Taking on starter tasks, pair programming, building confidence through contributions.

**Month 2+ Goals**
> Independent work, standard team velocity, mentoring others.

**Learning Plateau**
> Normal period where progress feels slower. Keep going!

**Impostor Syndrome**
> Feeling like you don't belong or aren't good enough despite evidence otherwise. Very common for new developers!

## Getting Help Terms

**Blocked / Blocker**
> When you can't make progress due to waiting for something or not knowing how to proceed.

**Rubber Ducking**
> Explaining your problem out loud (to a rubber duck, or AI!) which often helps you solve it yourself.

**Stack Overflow**
> Popular Q&A site for programming questions. Good resource, but AI can often explain answers better.

**RTFM (Read The F***ing Manual)**
> (Polite version: Read The Fine Manual) - Suggests checking documentation first. But asking questions is still okay!

## AI Ethics & Safety

**Hallucination**
> When AI confidently states incorrect information. Always verify important claims.

**Prompt Injection**
> Security issue where malicious input tricks the AI. Good configs protect against this.

**Data Privacy**
> Being careful not to share confidential code or information with AI tools. Check your company's AI usage policy.

**Copyleft / GPL-3.0**
> Open source license used by this repository. Code must remain open source.

## Pro Tips

**When you see unfamiliar terms**:
- Ask the AI! "What does [term] mean?"
- Ask your mentor
- Add to this glossary via PR

**Building Your Mental Model**:
- Terms will make more sense as you use them
- Don't memorize - learn through practice
- Come back to this glossary as reference

**Contributing**:
- Found a term we missed? Add it!
- See incorrect definition? Fix it!
- Help future new developers!

---

**Note**: This glossary focuses on terms relevant to AI-assisted onboarding. For general programming terms, ask your AI tool or mentor!
