# INTEGRATE-LEARNINGS - Merge Feature Learnings with Project Memory

You take learnings captured during feature development and integrate them with the project's long-term memory.

## When to Run
After feature is complete and user has approved all functionality.

## Process

1. **Load Feature Learnings**: Read backlog/[feature]/learnings.md
2. **Analyze Current Memory**: Check relevant docs/ files
3. **Identify Integration Points**: What should be updated/added
4. **Propose Changes**: Show what will be updated and why
5. **Execute Updates**: Merge learnings into docs/ and CLAUDE.md

## Input Analysis

### From learnings.md
- New patterns discovered
- Domain rules learned
- Architectural decisions made
- Deviations from existing patterns
- Improvements to existing patterns
- New standards that emerged

### Current Memory Check
- docs/patterns/ - existing technical patterns
- docs/domain/ - current domain knowledge
- docs/decisions/ - architectural decisions
- CLAUDE.md - project standards and principles

## Integration Strategy

### For New Patterns
- If pattern used successfully in feature → Add to docs/patterns/
- If pattern is variation of existing → Update existing pattern with notes
- If pattern conflicts with existing → Document as alternative approach

### For Domain Knowledge
- New business rules → Add to relevant docs/domain/ file
- Clarifications to existing rules → Update docs/domain/ with details
- New domain concepts → Create new docs/domain/ file if needed

### For Architectural Decisions
- Significant decisions → Add to docs/decisions/
- Updates to existing decisions → Append to existing docs/decisions/ file
- New principles → Consider adding to CLAUDE.md

### For Standards
- New coding standards → Update CLAUDE.md
- Tool usage patterns → Update CLAUDE.md
- Workflow improvements → Update CLAUDE.md

## Output

Create integration summary:

```markdown
# Integration Summary for [Feature]

## Changes Made

### docs/patterns/
- **Updated**: auth.md - added OAuth refresh token pattern
- **Created**: api-validation.md - new validation approach from feature

### docs/domain/
- **Updated**: users.md - added role transition rules
- **Updated**: payments.md - clarified refund business logic

### docs/decisions/
- **Created**: database-migrations.md - established migration strategy

### CLAUDE.md
- **Added**: Testing standard for async operations
- **Updated**: API error handling convention

## Learnings Not Integrated
- [Pattern X] - used only once, keeping in feature notes for now
- [Decision Y] - feature-specific, not applicable to other areas

## Recommendations
- Review auth.md in 2 months to see if OAuth pattern is widely adopted
- Consider extracting validation pattern if used in 2+ more features
```

## Conflict Resolution

### When docs/ files have changed
- Review recent changes to understand what others added
- Merge compatible learnings
- Note conflicts in integration summary for discussion

### When learnings conflict with existing patterns
- Document both approaches with contexts where each applies
- Include rationale for when to use each

## Success Criteria

Integration complete when:
- All valuable learnings captured in appropriate docs/ files
- No conflicts remain unresolved
- Team can discover and reuse the learnings
- Feature learnings.md reflects what was integrated

## Key Principles

- **Preserve context**: Include why decisions were made
- **Avoid duplication**: Update existing docs rather than create new ones
- **Team first**: Consider how changes help other developers
- **Incremental**: Not all learnings need immediate integration
- **Traceable**: Clear connection between feature and resulting knowledge