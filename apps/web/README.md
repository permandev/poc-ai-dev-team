# apps/web

Frontend for the Task Manager project.

## Tech Stack

- **Framework**: Next.js (App Router)
- **Language**: TypeScript
- **Package Manager**: pnpm
- **Styling**: Tailwind CSS v4
- **UI Components**: shadcn/ui

## Folder Structure

```
apps/web/
├── app/          # Next.js App Router pages & layouts
├── components/   # Shared UI components (shadcn/ui + custom)
├── features/     # Feature-based modules (auth, tasks, etc.)
├── hooks/        # Custom React hooks
├── lib/          # Utilities and helpers
├── types/        # TypeScript type definitions
└── docs/         # Feature documentation
```

## Getting Started

```bash
pnpm install
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Scripts

```bash
pnpm dev      # Start development server (Turbopack)
pnpm build    # Build for production
pnpm start    # Start production server
pnpm lint     # Run ESLint
```

## Adding shadcn/ui Components

```bash
pnpm dlx shadcn@latest add <component-name>
```
