
- Don't generate any code yet in this step
- Follow the instructions below to understand how to generate tasks
- Generate tasks in `./tasks/[task-name].md` file

# Introduction

Use this guide for powerful approach to managing development tasks. The focus is on clarity, practicality, and results. Follow the steps below to generate tasks.

## 1. Define the Problem

Start by answering these essential questions:

- **What** are you trying to build?
- **Why** is it needed?
- **Who** will use it?
- **When** does it need to be completed?

**Example:**
```
Problem: Build user authentication for our web application
Why: To secure user data and personalize experiences
Who: All users of our application
When: Needed by end of next sprint
```

## 2. Break It Down

Divide the problem into logical, manageable chunks:

1. Identify the major components
2. Break each component into specific tasks and clear tasks
3. Prioritize tasks based on importance and dependencies
4. Make it easy to understand and implement

**Example:**
```
1. User Authentication
  - [ ] Create login page UI
    - [ ] Create form for username and password
    - [ ] Create login button
  - [ ] Integrate login API endpoint
    - [ ] Add password validation
    - [ ] Create login fetch API
  - [ ] Create session management
    - [ ] Store JWT token in local storage
    - [ ] Set up automatic token refresh
    - [ ] Implement logout functionality
  - [ ] Add error handling and notifications
```

## 3. Prioritize

For each task, determine:

- **Importance**: How critical is this to core functionality?
- **Dependencies**: What must be completed first?
- **Difficulty**: How complex or time-consuming is this task?

Use a simple system:
- P0: Must have (core functionality)
- P1: Should have (important)
- P2: Nice to have (can be deferred)

## 4. Describe Tasks Clearly

For each task, include:

```
Task: [Brief, descriptive name]
Description: [1-2 sentence explanation]
Acceptance Criteria: [How do we know when it's done?]
Dependencies: [What needs to be completed first?]
```
## 5. Track Progress

Use these simple status categories:

- **Backlog**: Not started ([ ])
- **In Progress**: Currently working on it ([>])
- **Done**: Completed and verified ([x])

Update the status before and after each task, optionally with brief notes on progress or blockers.

## 6. Execute and Adjust

1. Focus on one task at a time
2. Adjust priorities as needed
3. Document changes to requirements or approach

## 7. Add Context

Add context if necessary. Follow [Create Context Guide](generate-context.mdc) for how to create context documents.

## 8. Generate Tasks

With all above steps completed, generate tasks based on this template. Create `tasks.md` file and add tasks to it.

```
# Task: [Task Name]

Description: [1-2 sentence explanation]
Acceptance Criteria: [How do we know when it's done?]
Dependencies: [What needs to be completed first?]

Status: [Backlog, In Progress, Done]
Notes: [Optional, brief notes on progress or blockers]

1. [Task 1]
  - context1.md
  - [ ] [Task 1.1]
  - [ ] [Task 1.2]
2. [Task 2]
  - [ ] [Task 2.1]
  - [ ] [Task 2.2]
3. [Task 3]
  - [ ] [Task 3.1]
  - [ ] [Task 3.2]
```

## Sample Task Template

```
## Task: Implement User Login API

Description: Create API endpoint that authenticates users and returns JWT token

Acceptance Criteria:
- Endpoint accepts username/password and validates credentials
- Returns JWT token for valid users
- Returns appropriate error for invalid credentials
- Includes rate limiting for failed attempts

Dependencies: Database user schema

Status: In Progress
Notes: Basic authentication working, adding rate limiting

1. Create login API endpoint
  - [ ] Create repository for saving user data
    - [ ] Create user model
    - [ ] Create repository interface
    - [ ] Implement repository methods
  - [ ] Create login controller
    - [ ] Create login request model
    - [ ] Create login response model
    - [ ] Create login service
    - [ ] Create login controller
  - [ ] Create login endpoint
  - [ ] Add rate limiting
  - [ ] Add error handling
  - [ ] Add logging
  - [ ] Add tests
```

## Project Wrap-up

After completion, briefly answer:

1. What worked well?
2. What could be improved?
3. What should we do differently next time?
4. What can be reused in future projects?

## Remember

- Keep it simple
- Focus on clear communication
- Update if needed
- Adjust as needed

Good task management isn't about perfect documentation—it's about clarity, focus, and getting things done.

