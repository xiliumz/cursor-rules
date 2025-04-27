- Locate the `./tasks` directory and list all available task definition files.
- Identify the task the user wants to execute. If the user doesn't specify, select the first task file alphabetically.
- Perform the actions described in this document.

# Task Execution and Status Updates

## Introduction

This guide explains how to effectively execute tasks and maintain accurate status updates throughout the development process. Clear task execution and consistent status tracking are essential for project visibility and team coordination.

## Determining Your Task Capacity

Before starting task execution, determine how many tasks you can effectively handle in one session:

1. **Assess task complexity**
   - Complex tasks require more focused attention
   - Simple tasks can be batched more easily
   - Be honest about the cognitive load of each task

2. **Consider your energy levels**
   - Schedule demanding tasks during your peak productivity hours
   - Save simpler tasks for when energy is lower
   - Account for potential context-switching costs

3. **Set realistic limits**
   - It's better to complete 2-3 tasks well than to attempt 5-6 with poor results
   - Quality should never be sacrificed for quantity
   - Build in buffer time for unexpected complications

4. **Determine the number of tasks you can handle**
   - If you think you can handle more than 3 tasks, take it. I prefer you can take a lot of tasks at once.

## Task Execution Workflow

### 1. Preparation Phase

Before starting a task:

1. **Review the task and context**
   - Read the task description thoroughly
   - Review all referenced context documents (e.g., `auth.md`)
   - Understand acceptance criteria and dependencies

2. **Confirm task readiness**
   - Ensure all dependencies are completed
   - Verify you have necessary access and resources
   - Clarify any questions with stakeholders

3. **Update task status**
   ```markdown
   - [ ] Create login API endpoint (Status: In Progress - Jane)
   ```

### 2. Execution Phase

While working on the task:

1. **Follow the subtask sequence**
   - Work through subtasks in order
   - Update status as you progress

2. **Document important findings**
   - Note any unexpected issues
   - Document design decisions
   - Record useful information for future reference

3. **Regular status updates**
   - Update before and after each task or subtask execution
   - Include brief progress notes
   ```markdown
   - [x] Create user model (Completed)
   - [>] Create repository interface (In progress - added basic CRUD methods)
   - [ ] Implement repository methods
   ```

### 3. Completion Phase

When finishing a task:

1. **Verify against acceptance criteria**
   - Ensure all requirements are met
   - Test functionality thoroughly
   - Complete all subtasks

2. **Update final status**
   - Mark task as complete
   - Include completion date
   - Add any relevant notes
   ```markdown
   - [x] Create login API endpoint (Completed - Added rate limiting)
   ```

3. **Update context documents**
   - Revise context files with new implementation details (See [Create Context Guide](generate-context.mdc) for guidelines)
   - Document any changes to the original plan

4. **Handle Completed Task Files**
   - Check if *all* tasks and subtasks within the specific task file (e.g., `auth.md` in the examples) are marked as `[x] Completed`.
   - If the entire file represents a completed unit of work:
     - **Identify or Create Context:** Determine if a relevant context document already exists (e.g., in a `./context` directory). If one exists, update it to reflect the completed work's final state or outcomes. If no relevant context document exists, create a new one summarizing the task and its results. Refer to [Create Context Guide](generate-context.mdc) for guidance on structuring context documents.
     - **Delete Task File:** After ensuring the context is captured (either by updating an existing document or creating a new one), delete the completed task file from the `./tasks` directory to keep the task list focused on active work.

## Status Tracking System

### Status Symbols

Use clear symbols for task status:

```markdown
- [ ] Not started
- [>] In progress
- [!] Blocked (include reason)
- [?] Needs clarification
- [x] Completed
```

### Status Updates Format

```markdown
- [Status] Task description (Additional information)
```

Examples:
```markdown
- [ ] Create user model
- [>] Build authentication service (Working on token generation)
- [!] Configure database connection (Blocked: waiting for credentials)
- [x] Set up project structure (Completed)
```

## Practical Examples

### Example 1: Basic Task Update Flow

**Initial state:**
```markdown
## User Authentication
- auth.md
  - [ ] Create login API endpoint
    - [ ] Create user model
    - [ ] Create repository interface
    - [ ] Implement repository methods
```

**Execution 1 update:**
```markdown
## User Authentication
- auth.md
  - [>] Create login API endpoint (In progress - Jane)
    - [x] Create user model (Completed)
    - [>] Create repository interface (Adding validation methods)
    - [ ] Implement repository methods
```

**Execution 2 update:**
```markdown
## User Authentication
- auth.md
  - [>] Create login API endpoint (In progress - Jane)
    - [x] Create user model (Completed)
    - [x] Create repository interface (Completed)
    - [>] Implement repository methods (Working on error handling)
```

**Final update:**
```markdown
## User Authentication
- auth.md
  - [x] Create login API endpoint (Completed)
    - [x] Create user model (Completed)
    - [x] Create repository interface (Completed)
    - [x] Implement repository methods (Completed - Added caching)
```

### Example 2: Handling Blockers

```markdown
## Payment Processing
- payment-system.md
  - [>] Implement payment gateway integration
    - [x] Create payment service interface (Completed)
    - [!] Connect to payment provider API (Blocked: API key pending from finance team)
    - [ ] Implement error handling
```

**After resolving blocker:**
```markdown
## Payment Processing
- payment-system.md
  - [>] Implement payment gateway integration
    - [x] Create payment service interface (Completed)
    - [>] Connect to payment provider API (Received key, implementing connection)
    - [ ] Implement error handling
```

### Example 3: Task That Needs Adjustment

**Original task:**
```markdown
## User Dashboard
- dashboard.md
  - [ ] Create analytics widget
    - [ ] Design data visualization
    - [ ] Implement chart component
    - [ ] Connect to analytics API
```

**Updated with new requirements:**
```markdown
## User Dashboard
- dashboard.md
  - [>] Create analytics widget (Updated scope: added filter functionality)
    - [x] Design data visualization (Completed)
    - [>] Implement chart component (Adding requested filters)
    - [ ] Connect to analytics API
    - [+] Add date range filter [New requirement]
```

## Common Pitfalls to Avoid

1. **Outdated status** - Not updating frequently enough
2. **Vague updates** - "Working on it" vs. specific progress
3. **Missing blockers** - Not highlighting impediments early
4. **Incomplete context** - Not linking important information
5. **Isolated updates** - Not communicating changes to team members

## Best Practices for Task Execution

1. **Focus on one task at a time** - Minimize context switching
2. **Update status before end of day** - Ensure visibility for team
3. **Be specific about blockers** - Include what's needed to unblock
4. **Link to relevant resources** - Code, PRs, documentation
5. **Flag scope changes early** - Note if requirements shift
6. **Include time estimates and actuals** - Help improve future estimates

## Conclusion

Effective task execution and status updates create transparency, and provide valuable project history. By following a consistent approach to updating task status, you'll build a more efficient development process.

Remember that the goal of status updates is communication—they should be clear, honest, and helpful for everyone.
