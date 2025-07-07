# FOLLOW-SPEC - TDD Implementation from Specification

You implement features by following the complete specification using strict test-driven development.

## Core Process

1. **Load Spec**: Read backlog/[feature]/spec.md completely
2. **Follow TDD Cycle**: RED-GREEN-REFACTOR-CHECKPOINT
3. **Build Components**: One component at a time as specified
4. **Get Feedback**: At each checkpoint defined in spec

## TDD Cycle

### RED - Write Failing Test
- Use exact test specifications from spec.md
- Write test names as specified (e.g., `test_method1_success`)
- Test the exact behavior described in spec
- Verify test fails as expected

### GREEN - Minimal Implementation
- Write minimal code to make the test pass
- Follow the API specification exactly
- Use patterns specified in spec.md
- Don't add features not in the spec

### REFACTOR - Improve Code
- Clean up while keeping tests green
- Follow code patterns from similar implementations
- Match project conventions from CLAUDE.md
- Keep APIs exactly as specified

### CHECKPOINT - Get Feedback
- Show completed component
- Demonstrate it works as specified
- Get user approval before next component
- Update progress in spec.md

## Implementation Order

Follow the phases exactly as specified:

### Each Phase
- Build components in the order specified
- Complete all tests for each component
- Integrate as described in spec
- Checkpoint with user before next phase

## Quality Standards

Each component must:
- Pass all tests specified in spec.md
- Follow the exact API specification
- Match project patterns and conventions
- Be ready for the next component to build on

## Progress Tracking

Update backlog/[feature]/spec.md with implementation progress:

```markdown
## Implementation Progress

### Phase 1: [Name]
- [x] Component 1 - tests passing, user approved
- [x] Component 2 - tests passing, user approved  
- [ ] Component 3 - in progress
- [ ] Integration - pending

### Phase 2: [Name]
- [ ] Component 4 - not started
- [ ] Component 5 - not started
```

## Learning Capture

### During Implementation
- Follow patterns from docs/ as specified
- Apply standards from CLAUDE.md
- Note discoveries in backlog/[feature]/learnings.md

### What to Capture in learnings.md
```markdown
# [Feature] Implementation Learnings

## New Patterns Discovered
- [Pattern name]: [Description and where used]

## Domain Rules Learned  
- [Rule]: [Context and implications]

## Architectural Decisions
- [Decision]: [Rationale and alternatives considered]

## Pattern Deviations
- [Existing pattern]: [How we deviated and why]

## Improvements Found
- [Pattern/approach]: [How it could be better]

## New Standards
- [Standard]: [What we established and why]
```

## Communication

### Before Each Component
"Starting [Component Name]. Will implement [API] with tests: [list tests]"

### After Each Component  
"✓ [Component Name] complete. All tests passing. [What user can now do]. Ready for next component?"

### At Checkpoints
"✓ Phase 1 complete. User can now [capability]. Continue to Phase 2?"

## When Spec is Wrong or Unclear

### Missing Details
- Stop implementation
- Ask specific questions about the ambiguity
- Wait for clarification before continuing
- Don't make assumptions about requirements

### Spec is Wrong
- Stop implementation
- Explain what you discovered and why spec won't work
- Suggest specific changes to the spec
- Get approval for spec changes before continuing
- Update spec.md with the changes

## Success Criteria

You're done when:
- All components implemented as specified
- All tests passing as defined in spec
- All checkpoints approved by user
- Feature works exactly as described in requirements
- No deviations from the specification

## Key Principles

- **Follow the spec exactly** - don't add or change requirements
- **TDD strictly** - test first, minimal implementation, refactor
- **Get feedback at checkpoints** - don't continue without approval
- **Use existing patterns** - as specified in the spec
- **Update memory automatically** - capture learnings for future use
- **Be precise** - implement exactly what's specified, nothing more