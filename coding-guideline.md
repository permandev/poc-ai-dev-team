# 🧠 Coding Guidelines — Task Management Project

## 1. General Principles

* Code must be **readable, maintainable, and consistent**
* Prefer **simple solutions over complex ones**
* Write code that both **humans and AI can understand**

---

## 2. Language & Stack

* TypeScript (strict mode)
* Next.js (App Router)
* pnpm
* Tailwind CSS
* shadcn/ui

---

## 3. Naming Conventions

### Variables & Functions

* camelCase

```ts
const taskList = []
function createTask() {}
```

### Components

* PascalCase

```tsx
TaskCard.tsx
TaskList.tsx
```

### Files

* kebab-case or PascalCase (consistent within folder)

---

## 4. Component Structure

Preferred pattern:

```tsx
type Props = {
  title: string
}

export function TaskCard({ title }: Props) {
  return <div>{title}</div>
}
```

Rules:

* Keep component small
* Avoid large monolithic components

---

## 5. Folder Organization

Use **feature-based structure**

/features/task
TaskCard.tsx
TaskList.tsx
task.service.ts

---

## 6. Business Logic

* DO NOT put business logic in UI components
* Use service layer

```ts
// task.service.ts
export function createTask() {
  // logic here
}
```

---

## 7. API Calls

* Centralize API calls in `/lib/api` or feature service
* Do not call API directly inside components

---

## 8. Styling

* Use Tailwind CSS
* Use shadcn/ui components as base
* Avoid inline styles

---

## 9. State Management

* Prefer local state first
* Use global state only when necessary

---

## 10. Error Handling

* Always handle API errors
* Show user-friendly messages

---

## 11. Git & Branch Strategy (Git Flow)

We use a simplified Git Flow strategy.

### Main Branches

#### `main`

* Production-ready code
* Only reviewed and approved code can be merged

#### `develop`

* Integration branch for ongoing development
* Feature branches merge into `develop`

---

### Branch Naming Convention

#### Feature

```bash
feature/task-create-page
```

#### Bug Fix

```bash
fix/task-status-bug
```

#### Refactor

```bash
refactor/task-service
```

#### Chore

```bash
chore/update-dependencies
```

---

### Workflow

1. Create branch from `develop`
2. Implement feature or fix
3. Open Pull Request to `develop`
4. Review and test
5. Merge after approval

Production release flow:

```bash
develop → main
```

---

### Pull Request Rules

* PR title should follow conventional commits
* PR must link to issue/task
* PR should be small and focused
* Require at least 1 review before merge

---

### Commit Convention

Use conventional commits:

```bash
feat: add task creation form
fix: handle empty title validation
refactor: simplify task service
chore: update dependencies
```

---

### AI Development Rules

When AI tools or agents are used:

* AI must create changes in feature/fix branches only
* AI-generated code must go through PR review
* Never allow direct push to `main`

---

### Deployment Strategy

#### Development

* Auto deploy from `develop`

#### Production

* Deploy only from `main`

---

### Future Improvements

Potential future additions:

* release/*
* hotfix/*
* semantic versioning
* automated changelog generation

---

## 12. Pull Request Rules

* Every PR must:

  * Link to issue
  * Pass checklist
  * Be reviewed before merge

---

## 13. AI Usage Guidelines

* AI-generated code must be reviewed
* Do not blindly copy from AI
* Always test AI-generated logic

Optional:

* Include prompt used (for traceability)

---

## 14. Code Quality

* Avoid duplicated logic
* Use reusable functions
* Keep functions small and focused

---

## 15. Definition of Done

A task is complete when:

* Code works correctly
* No critical bugs
* Reviewed and approved
* Merged to main branch

---

## 16. Future Rules (to evolve)

* Add testing guideline
* Add performance guideline
* Add security best practices

---

