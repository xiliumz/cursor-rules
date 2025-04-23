# Task Management Cursor Rules

A repository containing custom rules and configurations for managing tasks efficiently using Cursor IDE.

## Overview

This repository serves as a centralized location for storing and managing task-related cursor rules, helping to streamline workflow and improve productivity in the Cursor IDE environment.

## Rules

- **.cursor/rules/prd-transform.mdc**: To transform a PRD into the standard format by extracting key sections into the PRD template. **How to use**: "Transform [prd-template.md] to standard format."
- **.cursor/rules/task-generation.mdc**: Steps to generate tasks from a standard PRD by extracting features, numbering them, and detailing tasks. **How to use**: "Generate tasks from standard-prd.md by extracting features, numbering them, and detailing tasks."
- **.cursor/rules/analyze-task.mdc**: Instructions for analyzing tasks to determine if subtasks are needed and formatting them. **How to use**: "Analyze task [task-number] for subtasks."
- **.cursor/rules/execute-task.mdc**: Guidelines for identifying and executing tasks, handling subtasks, and updating statuses. **How to use**: "Execute the next task."

---

- **.cursor/rules/prd-template.md**: Standard PRD template with sections for product overview, objectives, features, user stories, and non-functional requirements.
- **.cursor/rules/build-prd.mdc**: Build a PRD from user's input. **How to use**: "Build a PRD based on my instructions."

## Recommended Execution Order

1. **.cursor/rules/prd-transform.mdc** (using `prd-template.md`): Standardize the raw PRD into the standard format.
2. **.cursor/rules/task-generation.mdc**: Generate tasks based on the standardized PRD's features.
3. **.cursor/rules/analyze-task.mdc**: Analyze tasks for complexity and create subtasks if needed.
4. **.cursor/rules/execute-task.mdc**: Execute and complete tasks and subtasks, updating statuses accordingly.
