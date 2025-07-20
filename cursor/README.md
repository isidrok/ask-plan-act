# Cursor ASK-PLAN-ACT Workflow

This folder contains custom prompts for Cursor that implement a token-efficient, TDD-focused development workflow.

## Overview

The ASK-PLAN-ACT workflow divides development into three distinct phases, each optimized for different AI models to maximize efficiency and minimize token usage:

1. **ASK** (Gemini Flash - Free): Gather requirements
2. **PLAN** (Gemini Pro - 1 request/message): Create detailed TDD plan
3. **ACT** (Gemini Flash - Free): Implement using TDD

## Workflow Phases

### 1. ASK Phase (`ask.md`)
- **Model**: Gemini Flash (free, no request limit)
- **Purpose**: Gather and clarify requirements
- **Process**:
  - Analyzes existing codebase for context
  - Asks batched questions to minimize back-and-forth
  - Creates `backlog/[feature-name]/requirements.md`

### 2. PLAN Phase (`plan.md`)
- **Model**: Gemini Pro (1 request per message)
- **Purpose**: Create comprehensive TDD implementation plan
- **Process**:
  - Reads requirements from backlog
  - Presents technical approach for approval
  - Creates detailed plan with:
    - Component APIs for new code
    - Specific changes for existing code
    - Test scenarios (not full test code)
    - Phased implementation approach
  - Creates `backlog/[feature-name]/plan.md`

### 3. ACT Phase (`act.md`)
- **Model**: Gemini Flash (free, unlimited)
- **Purpose**: Execute the plan using strict TDD
- **Process**:
  - Follows RED → GREEN → REFACTOR cycle
  - Implements one component at a time
  - Updates `backlog/[feature-name]/progress.md`
  - Allows for interactive development

## File Structure

```
backlog/
└── [feature-name]/
    ├── requirements.md  # Created by ASK
    ├── plan.md         # Created by PLAN
    └── progress.md     # Updated by ACT
```

## Usage

1. Start with ASK to gather requirements:
   ```
   /ask Help me build a user authentication system
   ```

2. Once requirements are clear, use PLAN to design the solution:
   ```
   /plan Create a TDD plan for the user authentication feature
   ```

3. Finally, use ACT to implement:
   ```
   /act Implement the authentication system following the plan
   ```

## Benefits

- **Token Efficient**: Uses free models for high-interaction phases
- **TDD Focused**: Ensures quality through test-first development
- **Traceable**: All decisions and progress tracked in backlog
- **Flexible**: Plans provide structure without being overly rigid
- **Model Appropriate**: Leverages each model's strengths

## Tips

- Keep feature names consistent across phases (e.g., "user-auth")
- Review the plan before starting ACT phase
- Use the progress.md file to track deviations and decisions
- The more detailed the requirements, the better the plan
- Plans should be detailed enough that a less capable model can execute them