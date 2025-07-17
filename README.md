# AI Coding Methodology: Ask, Plan, Act

A systematic approach to collaborating with AI coding agents using persistent memory, TDD,
and structured workflows to produce quality software.

This methodology is detailed in the blog post: [AI Coding Methodology: Ask, Plan,
Act](https://isidrok.github.io/posts/ai-coding-methodology)

## Overview

This repository contains the methodology and prompts for effective AI-assisted software
development. The Ask/Plan/Act framework addresses common AI agent limitations while
leveraging their code generation strengths.

## The Methodology

### Three-Phase Approach

1. **Ask:** Discover and document comprehensive requirements
2. **Plan:** Design technical approach and break down implementation
3. **Act:** Execute using TDD, one component at a time

### File Structure

```bash
project/
├── backlog/
│ ├── template.md # Template for feature plans
│ └── feature-name.md # Combined requirements, plan, progress, and notes
├── docs/ # Generated project knowledge
├── CLAUDE.md # Project-level AI agent rules and context
└── src/
  └── module/
    └── CLAUDE.md # Module-specific AI agent rules and context
```

## Prompts

The methodology uses five specialized prompts:

- **ask.md** - Gathers functional requirements, organizing them into user stories with
  acceptance criteria
- **plan.md** - Creates technical approach, breaking down implementation into phases and
  components
- **act.md** - Implements one component at a time using TDD
- **reflect.md** - Analyzes conversations and code to extract architectural decisions and
  conventions
- **consolidate.md** - Reviews documentation to remove duplication and ensure consistency

### Cursor Workflow

For Cursor's limited context (128k tokens) and request constraints (500/month), a streamlined two-command workflow:

- **cursor/plan.md** - Efficiently gathers requirements and creates comprehensive implementation plan
- **cursor/act.md** - TDD implementation by phase, one component at a time with mandatory stops

## Workflow

### Standard Workflow (Claude, GPT-4, etc.)

1. **Ask**: `/ask feature-name` - Clarify requirements and create user stories
2. **Plan**: `/plan feature-name` - Design technical approach and implementation plan
3. **Act**: `/act feature-name` - Implement using TDD, one component at a time

### Cursor Workflow

1. **Plan**: `/plan feature-name` - Gather requirements and create implementation plan in `backlog/feature-name.md`
2. **Review**: Manually review and adjust the generated plan
3. **Act**: `/act feature-name phase-1` - Implement Phase 1 using TDD (one component at a time)
4. **Iterate**: Review, commit, then `/act feature-name phase-2` for next phase

## Benefits

- **Persistent Memory**: Filesystem-based knowledge that survives sessions
- **Quality by Default**: TDD and structured planning ensure robust software
- **Reduced Rework**: Clear requirements and planning eliminate misunderstandings
- **Self-Improving**: AI agents build and maintain their own project documentation

## Use Case

The methodology was used to build the [KB Sport App](https://github.com/isidrok/kb-sport-app), a kettlebell workout tracking application with computer vision-based repetition counting. [Try it out!](https://isidrok.github.io/kb-sport-app/).

## When to Use

- Complex features requiring multiple components
- Projects needing persistent context across sessions
- Teams wanting systematic AI collaboration
- Applications where quality and testing are critical

For simple tasks, treat AI agents as pair programming partners while applying the same
principles of requirements clarification and code review.
