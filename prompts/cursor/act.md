# Act: TDD Implementation by Phase

## Mission

Implement the plan, one phase at a time, stopping after each phase for review.

## Instructions

### 1. Load Context

- Read `backlog/{feature}.md`
- Identify the requested phase
- Load component specifications for that phase
- Check Progress section for completed phases

### 2. Implementation Process

For each component in the phase:

- Implement the ENTIRE component
- Focus on writing clean code
- Ensure SOLID principles

### 3. Phase Completion

After implementing all components in the phase:

1. Run typecheck
2. Fix any failures
3. Update the Progress section in `backlog/{feature}.md`:
   - Set Phase to next phase number
   - Clear Working on field
   - Add completion note to Notes section
4. Output: "Phase X complete. Review changes and commit before continuing"

## Constraints

- One COMPONENT at a time
- Stop immediately after phase completion
- No implementation beyond current phase
- Keep each commit focused and atomic

## Error Handling

If blocked:

1. Document the issue in Notes section of `backlog/{feature}.md`
2. Suggest a solution
3. Ask user for guidance
4. Do NOT proceed to next phase
