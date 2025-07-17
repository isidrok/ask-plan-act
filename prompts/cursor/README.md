# Cursor Workflow Guide

Optimized two-command workflow for Cursor's limited context and request constraints.

## Overview

1. **`/plan feature-name`** - Gather requirements and create implementation plan
2. **`/act feature-name phase-X`** - Implement using TDD, one phase at a time

## Workflow

### Step 1: Planning
```
/plan user-authentication
```

Provide all requirements upfront:
- User registration with email/password
- Login/logout functionality
- JWT token management
- Password reset flow

Cursor will create `backlog/user-authentication.md` with phases and components.

### Step 2: Review & Edit Plan
Manually review and adjust the generated plan before implementation.

### Step 3: Implementation
```
/act user-authentication phase-1
```

Cursor implements Phase 1 components using TDD:
1. Writes all tests for Component A
2. Implements Component A
3. Refactors Component A
4. Repeats for all phase components
5. Stops for review/commit

### Step 4: Continue
```
/act user-authentication phase-2
```

Repeat until all phases complete.

## Example Plan Structure

```markdown
## Phase 1: Core Authentication

### Component: AuthService
**Purpose**: Handle user authentication logic

**Public API**:
```typescript
interface AuthService {
    register(email: string, password: string): Promise<User>
    login(email: string, password: string): Promise<AuthToken>
    logout(token: string): Promise<void>
}
```

**Unit Tests** (in order):
1. test_register_creates_user - Validates user creation
2. test_register_hashes_password - Ensures password security
3. test_register_rejects_duplicate - Prevents duplicate emails
```

## Tips

- Provide comprehensive requirements upfront to minimize back-and-forth
- Keep phases focused - one clear deliverable per phase
- Review and commit after each phase
- Use Notes section for implementation decisions
- Let Cursor leverage its RAG for codebase scanning