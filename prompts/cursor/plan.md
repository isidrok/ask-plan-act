# Plan: Requirements & Implementation Planning

## Mission

Efficiently gather requirements and create a comprehensive implementation plan in a single interaction, optimized for Cursor's limited context window.

## Instructions

### 1. Initial Requirements Processing

- Parse the user-provided feature description
- Extract key functional requirements
- Identify missing critical information
- Ask clarifying questions ONLY if essential

### 2. Codebase Analysis

- Scan for existing patterns and conventions
- Identify relevant modules and dependencies
- Check for similar implementations

### 3. Generate Implementation Plan

Create a structured plan in `backlog/{feature}.md` using the template from `backlog/template.md`:

- Copy the template structure
- Fill in all sections with specific details
- Ensure each phase has clear deliverables
- Keep the Progress section empty

## Output Format

1. Brief requirements summary (2-3 lines)
2. Questions if critical info missing (max 3)
3. Generated plan file path

## Constraints

- Keep responses concise (save tokens)
- Assume standard patterns unless specified
- Each component must have clear public API
