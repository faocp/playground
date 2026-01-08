# CLAUDE.md

## Project Overview
A simple todo application with a tasteful retro feel, using HTML, CSS, vanilla JavaScript.

## Conventions
- Use ES6+ syntax
- Prefer const over let
- Use semantic HTML elements
- Mobile-first CSS

## Workflow

- **Work incrementally**: Use subagents for discrete steps to preserve context window space.
- **Always consult docs**: Use Context7 MCP to read current documentation for any language, framework, or library. Your training data may be outdated.
- **Verify before returning**: Run tests, verify builds, and check your work. Never return incomplete or unverified code.
- **Update project docs**: After completing tasks or learning project-specific details, update `.github/copilot-instructions.md` or any `agent.md` files accordingly.
- **Manage terminals**: Reuse existing terminals when possible; close unneeded ones.

## Common Workflow Commands
"Create a plan for [feature]"           # Plan first
"Implement the [component]"             # Build it
"Write tests for [functionality]"       # Test it
"Commit with message: [description]"    # Save it
"Push to GitHub"                        # Ship it

## Coding Principles

### Structure
- Use a consistent, predictable project layout grouped by feature.
- Identify shared structure before scaffolding. Use framework-native composition (layouts, providers, base templates) for repeated elements.
- Duplication requiring the same fix in multiple places is a smell, not a pattern.

### Architecture
- Prefer flat, explicit code over abstractions or deep hierarchies.
- Avoid metaprogramming and unnecessary indirection.
- Minimize coupling so files can be safely regenerated in isolation.

### Functions
- Keep control flow linear; avoid deeply nested logic.
- Use small-to-medium functions with explicit state passing—no globals.

### Naming & Comments
- Use descriptive but simple names.
- Comment only to note invariants, assumptions, or external requirements.

### Logging & Errors
- Emit detailed, structured logs at key boundaries.
- Make errors explicit and informative.

### Regenerability
- Write code so any file can be rewritten from scratch without breaking the system.
- Prefer declarative configuration (JSON/YAML) over imperative setup.

### Modifications
- Follow existing patterns when extending or refactoring.
- Prefer full-file rewrites over micro-edits unless instructed otherwise.

### Testing
- Favor deterministic, testable behavior.
- Keep tests simple and focused on observable outcomes.
