# TanStack Router Monorepo Template

A modern monorepo template featuring React 19, TanStack Router, Vite 7, and Tailwind CSS v4 with Shadcn UI components.

## Tech Stack

- **Package Manager**: pnpm with Turbo for monorepo management
- **Frontend**: React 19
- **Routing**: TanStack Router (file-based routing with auto code-splitting)
- **Build**: Vite 7
- **Styling**: Tailwind CSS v4
- **UI Components**: Shadcn/Base UI
- **Linting/Formatting**: Biome
- **Testing**: Vitest + Testing Library

## Getting Started

### Prerequisites

- Node.js 20+
- pnpm 10.26.0+

### Installation

```bash
# Clone the template
git clone https://github.com/grayashh/tanstack-router-monorepo-template.git my-project
cd my-project

# Install dependencies
pnpm install

# Start development
pnpm dev
```

## Project Structure

```
.
├── apps/
│   └── web/                 # Example web application
│       ├── src/
│       │   ├── routes/      # File-based routes (TanStack Router)
│       │   └── components/  # App-specific components
│       └── public/          # Static assets
├── packages/
│   ├── ui/                  # Shared UI components (Shadcn style)
│   ├── typescript-config/   # Shared TypeScript configurations
│   └── biome-config/        # Shared Biome linting configurations
└── turbo.json               # Turbo configuration
```

## Commands

### Development

```bash
pnpm dev          # Start all apps in development mode
pnpm build        # Build all packages and apps
pnpm lint         # Lint all packages with Biome (auto-fix enabled)
pnpm format       # Format all packages with Biome
pnpm check        # Run Biome check (lint + format)
pnpm check-types  # Type check all packages
```

## Adding UI Components

To add Shadcn UI components, run from the monorepo root:

```bash
pnpm dlx shadcn@latest add button -c apps/web
```

This will place the UI components in `packages/ui/src/components`.

## Using Components

Import components from the shared UI package:

```tsx
import { Button } from "@workspace/ui/components/button"
```

## Adding a New App

1. Create a new directory under `apps/`
2. Copy the structure from `apps/web/`
3. Update `package.json` with the new app name
4. Add the app to `turbo.json` if needed

## Documentation

- [TanStack Router](https://tanstack.com/router/latest)
- [Vite](https://vitejs.dev/)
- [Tailwind CSS v4](https://tailwindcss.com/)
- [Shadcn UI](https://ui.shadcn.com/)
- [Turbo](https://turbo.build/)
- [Biome](https://biomejs.dev/)

## License

MIT
