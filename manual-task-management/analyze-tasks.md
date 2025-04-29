# Task Analysis and Update Guide

- This document complements the task generation process in [generate-tasks.mdc](./generate-tasks.mdc)
- Follow these instructions to analyze, refine, and update existing task documents
- Apply updates directly to the original task documents
- Always use sequential thinking

# Introduction

This guide provides a framework for analyzing, evaluating, and updating task documents created using the generate-tasks.mdc approach. Regular analysis ensures tasks remain relevant, properly prioritized, and effectively tracked. Follow these steps to maintain high-quality task management throughout your project.

## 1. Analyze Task Structure and Clarity

Evaluate each task against these criteria:

1. Is the task description clear and specific?
2. Are acceptance criteria measurable and complete?
3. Are dependencies accurately identified?
4. Is the task broken down to the appropriate level of detail?

For each task, rate clarity on a 1-3 scale:
- 1: Needs significant clarification
- 2: Somewhat clear but could be improved
- 3: Perfectly clear to any team member

**Example Analysis:**
```
Task: Implement User Login API
Clarity Rating: 2
Improvement Needed: Acceptance criteria should specify expected response formats and status codes
```

## 2. Evaluate Task Progress and Blockers

For tasks in progress or blocked:

1. Assess current status against expected timeline
2. Identify specific blockers and their impact
3. Determine if additional resources or reprioritization is needed
4. Update status markers with detailed notes

Use these status indicators with notes:
- [ ] **Blocked**: {Reason} - {Action needed}
- [>] **Behind Schedule**: {Reason} - {Recovery plan}
- [>] **On Track**: {Current progress note}
- [x] **Completed**: {Completion date} - {Validation notes}

**Example Update:**
```
- [>] Create login API endpoint
  Note: Behind schedule (2 days) due to unexpected authentication complexity. 
  Adding additional developer tomorrow to catch up.
```

## 3. Analyze Dependencies and Critical Path

Regularly review task dependencies to:

1. Identify bottlenecks blocking multiple tasks
2. Spot dependency cycles that need restructuring
3. Update dependency information as the project evolves
4. Highlight critical path tasks that directly impact deadlines

Visualize task dependencies when helpful:
```
Task A → Task B → Task C (Critical Path)
   ↓
Task D → Task E
```

Flag critical path tasks with [!] indicator:

**Example Update:**
```
- [>] [!] Setup user database schema
  Note: This task is blocking 3 other tasks and is now on critical path
```

## 4. Reassess Priorities Based on New Information

As the project progresses, continuously reevaluate priorities:

1. Has new information changed task importance?
2. Have stakeholder priorities shifted?
3. Have technical discoveries impacted the approach?
4. Are there new opportunities or risks to address?

Update priority designations with explanation:
```
Task: Implement password reset flow
Original Priority: P1
Updated Priority: P0
Reason: Security audit identified this as critical requirement
```

## 5. Add Emerging Tasks and Remove Obsolete Tasks

Projects evolve - keep task documents current:

1. Add new tasks that emerge during development
2. Mark obsolete tasks appropriately
3. Document the rationale for significant changes
4. Preserve task history for reference

Use these markers for task lifecycle changes:
- [+] **Added**: {Date} - {Reason}
- [-] **Removed**: {Date} - {Reason}
- [~] **Modified**: {Date} - {Changes}

**Example Updates:**
```
- [+] Add CAPTCHA to login form (Added 2023-05-15 - Security requirement)
- [-] Implement Facebook OAuth (Removed 2023-05-10 - Descoped from MVP)
```

## 6. Update Task Documentation Format

Enhance the task document structure for better clarity:

1. Add sections that emerged as important
2. Remove sections that proved unnecessary
3. Adjust formatting for better readability
4. Ensure consistent notation throughout

**Example Format Enhancement:**
```
## Task Section: Authentication
- Added color coding for priority levels
- Added emoji indicators for task types (🔒 Security, 🧪 Testing)
- Added collapsible sections for completed tasks
```

## Sample Task Analysis Template

```
## Task Analysis: User Authentication System

Review No: 1

### Structure Analysis
- Overall clarity score: 2/3
- Missing acceptance criteria in 2 subtasks
- Dependencies well-defined
- Improvement action: Add specific response code expectations

### Progress Assessment
- Overall: 60% complete (Expected: 75%)
- Critical blocker: Awaiting security team review
- Action: Escalate security review to management

### Priority Adjustments
- "Remember me" functionality: P1 → P2 (Moved to next release)
- Password complexity requirements: P2 → P1 (Security audit finding)

### Added/Removed Tasks
- [+] Add rate limiting to login attempts
- [-] Remove social media sharing option

### Process Insights
- Adding security review as explicit dependency helped
- Need earlier API documentation to reduce rework
- Breaking UI tasks by component improved parallelization
```

## Project-Wide Analysis

After significant milestones, analyze patterns across all tasks:

1. Which types of tasks consistently take longer than expected?
2. Which tasks had the most priority changes?
3. Where were dependencies most often missed?
4. Which areas had the most emerging requirements?

Document these insights for future projects:
```
# Project-Wide Task Analysis

## Estimation Patterns
- UI tasks: Generally underestimated by 20%
- API integration: Generally overestimated by 15%
- Testing tasks: Consistently underestimated by 40%

## Dependency Patterns
- Third-party integrations caused most cascading delays
- Database schema changes impacted more tasks than anticipated

## Priority Insights
- Security requirements frequently increased in priority
- Nice-to-have UI features frequently decreased in priority

## Process Recommendations for Next Project
1. Double time estimates for testing tasks
2. Add explicit security review phase before API development
3. Create more detailed acceptance criteria for UI tasks
4. Perform weekly dependency graph review
```

## Remember

- Task analysis should enhance, not burden the development process
- Updates should be clear and purposeful

Effective task analysis transforms task management from documentation into a strategic advantage for project success. 
