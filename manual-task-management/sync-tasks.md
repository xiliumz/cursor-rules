Step 1: Manage Task Status Based on Changes
- Reflect on the code changes you made in this session. If you didn't make any changes, jump to Step 2.
- If you made changes, locate the relevant task definition file(s) within the `./tasks/` directory.
- Update the status marker (e.g., change `[ ]` to `[x]`) for the completed task(s) in the corresponding file(s).

Step 2: Identify and Verify the Next Unimplemented Task
- Scan the markdown files within the `./tasks/` directory.
- Find the first task marked as incomplete (e.g., `[ ]`). Let's call this the "candidate task".
  *Example Task File (`./tasks/ui_components.md`):*
    ```markdown
    - [x] Create Button component
    - [ ] Create Badge component  <- This is the first incomplete task.
    - [ ] Create Card component
    ```
- Verify if the candidate task is already implemented in the codebase. This might involve:
    - Searching the codebase for keywords related to the task (e.g., function names, component names, filenames).
    - Manually inspecting the relevant parts of the code.
- If the candidate task **is implemented** despite being marked incomplete:
    - Find the *next* task marked `[ ]` in the task files.
    - Repeat the verification process (Step 2) for this new candidate task.
- If the candidate task **is not implemented**:
    - This is your next task to work on. Stop the process here.
- Continue this process until you identify an incomplete task (`[ ]`) that has not yet been implemented in the code.
