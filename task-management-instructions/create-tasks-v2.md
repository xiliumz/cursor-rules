# Task Creation Guidelines

## Basic Requirements

- Create tasks based on user requests
- Ask for clarification if the request is unclear
- Each task should take 1-4 hours (break larger tasks into subtasks)
- Make tasks specific and detailed, not broad or vague
- Your job is only creating tasks

## Getting Context

1. Check package.json for:

   - Dependencies
   - Scripts
   - Project configuration

2. Review existing code for:

   - Code patterns
   - Architecture
   - Implementation examples

3. Check configuration files for:

   - Environment settings
   - Security requirements
   - Application settings

4. Review docs/ directory for:
   - Architecture diagrams
   - API specifications
   - Style guides

## Task File Format

- Create files under tasks/ directory
- Name format: task-<task-name>.md (use kebab-case)
- Include these sections:
  1. Description (1-2 sentences)
  2. Context (why the task matters)
  3. Subtasks (nested checklist, max 3 levels)

## Checklist Format

```markdown
- [ ] Main task
  - [ ] Subtask
    - [ ] Detailed step
- [ ] Main task
  - [ ] Subtask
```

## Example

```markdown
# Task: Create MetricSummaryCard component

## Description

Implement a reusable soil data summary card component to display a soil metric label and numeric value.

## Context

**General:** On the soil data page of the farm performance module, individual metric summary cards are needed to provide a quick overview of soil properties (e.g., pH, moisture, organic carbon). MetricSummaryCard will standardize layout, styling, and accessibility for these metrics.

**Codebase:**

- Uses React with TypeScript and Tailwind CSS (see `tailwind.config.js`).
- UI consistency is enforced via system components; wrap with `StatisticCard` from `src/system-components/statistic-card`.
- Components in `src/modules/farm-performance/components/soil-data` should be exported via `index.ts`.
- Tests use Jest and React Testing Library; snapshots live in `__tests__` folders.

## Tasks

- [ ] Create `metric-summary-card.tsx` in `src/modules/farm-performance/components/soil-data/`
  - [ ] Define `MetricSummaryCardProps`:
    - `label: string`
    - `value: number | string`
    - `unit?: string`
    - `color: string`
    - `footerIcon?: ReactNode`
    - `footerText?: string`
  - [ ] Render root card container using custom div with Tailwind classes
  - [ ] Build header section:
    - [ ] Flex row, items-center, gap 12px, padding, with background color.
    - [ ] Render LetterSymbol component inside a 48×48px square with dynamic background color, rounded, and centered.
  - [ ] Build content section:
    - [ ] Column layout with gap, integrated within header section.
    - [ ] Render `label` with ValueIndicator component using text-sm styling.
    - [ ] Render `value` with ValueIndicator component using text-xl styling, appending `unit` if provided.
  - [ ] Build footer section:
    - [ ] Flex row, items-center, gap 4px, padding, rounded bottom corners, border top.
    - [ ] Render `footerIcon` and `footerText` styled with Urbanist 10px.
- [ ] Update `index.ts` in the same directory to export `MetricSummaryCard`
- [ ] Write unit tests in `src/modules/farm-performance/components/soil-data/__tests__/MetricSummaryCard.test.tsx` for:
  - [ ] Header rendering.
  - [ ] Optional `unit`, `footerIcon`, and `footerText` rendering.
  - [ ] Snapshot output with all props.
```
