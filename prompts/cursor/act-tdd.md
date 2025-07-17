# Act: TDD Implementation by Phase

## Mission

Implement the plan using strict TDD, one phase at a time, stopping after each phase for review.

## Instructions

### 1. Load Context

- Read `backlog/{feature}.md`
- Identify the requested phase
- Load component specifications for that phase
- Check Progress section for completed phases

### 2. TDD Implementation Process

For each component in the phase:

#### RED: Write ALL Tests for Component

```typescript
// Write complete test suite for the component
describe("ComponentName", () => {
  it("should do X when Y", () => {
    // Test case 1
  });

  it("should handle edge case Z", () => {
    // Test case 2
  });

  it("should throw error when invalid input", () => {
    // Test case 3
  });
  // ... all tests for this component
});
```

#### GREEN: Implement Component

- Implement the ENTIRE component to pass ALL tests
- Focus on making all tests pass

#### REFACTOR: Clean Component

- Refactor the complete component
- Extract helper methods
- Ensure SOLID principles
- Optimize implementation

### 3. Phase Completion

After implementing all components in the phase:

1. Run all tests
2. Fix any failures
3. Update the Progress section in `backlog/{feature}.md`:
   - Set Phase to next phase number
   - Clear Working on field
   - Add completion note to Notes section
4. Output: "Phase X complete. Review changes and commit before continuing"

## Constraints

- NEVER skip writing tests first
- One COMPONENT at a time (RED-GREEN-REFACTOR)
- Write ALL tests for a component before implementing
- Stop immediately after phase completion
- No implementation beyond current phase
- Keep each commit focused and atomic

## Error Handling

If blocked:

1. Document the issue in Notes section of `backlog/{feature}.md`
2. Suggest a solution
3. Ask user for guidance
4. Do NOT proceed to next phase
