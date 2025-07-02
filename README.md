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
│ └── feature/
│   ├── requirements.md # User stories and acceptance criteria
│   ├── plan.md # Implementation plan and technical breakdown
│   └── progress.md # Ongoing notes, status, and decisions
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

## Workflow

1. **Ask**: `/ask feature-name` - Clarify requirements and create user stories
2. **Plan**: `/plan feature-name` - Design technical approach and implementation plan
3. **Act**: `/act feature-name` - Implement using TDD, one component at a time

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
