# Best Practices & Clean Code Guidelines

> [!IMPORTANT]
> This document serves as the **SINGLE SOURCE OF TRUTH** for maintaining code quality in this project. All team members (human and AI) must adhere to these guidelines.

## 1. General Principles
- **DRY (Don't Repeat Yourself)**: Extract common logic into utils, hooks, or components.
- **SOLID**: Follow SOLID principles, especially Single Responsibility. Small, focused functions/components are easier to test and maintain.
- **KISS (Keep It Simple, Stupid)**: Avoid over-engineering. Write code that is easy to read and understand.
- **YAGNI (You Ain't Gonna Need It)**: Don't build features or abstractions for hypothetical future use cases.

## 2. TypeScript Guidelines
- **Strict Mode**: `strict: true` is enabled. Do not disable it.
- **No `any`**: Explicitly define types. Use `unknown` if the type is truly not known yet, but narrow it down before use.
- **Interfaces vs Types**: Use `interface` for public API definitions and object shapes that might be extended. Use `type` for unions, primitives, and tuples.
- **Props**: Define component props using an interface named `<ComponentName>Props`.

```typescript
// BAD
const UserCard = (props: any) => { ... }

// GOOD
interface UserCardProps {
  name: string;
  age: number;
}
const UserCard = ({ name, age }: UserCardProps) => { ... }
```

## 3. React & React Native (Solito) Patterns
- **Functional Components**: Use functional components with Hooks. Avoid Class components.
- **Hooks**:
    - Follow the [Rules of Hooks](https://reactjs.org/docs/hooks-rules.html).
    - Create custom hooks to separate logic from UI.
- **Component Composition**: Prefer composition over inheritance or excessive prop drilling.
- **File Structure**:
    - One component per file (mostly).
    - Colocate specific styles or sub-components if they are not reused elsewhere.

## 4. State Management
- **Local State**: Use `useState` for simple, local UI state (e.g., toggle menus, simpler form inputs).
- **Server State**: Use libraries like `TanStack Query` (if available) or Supabase hooks for fetching/caching data.
- **Global State**: Use Context API sparingly for global settings (theme, auth user). Avoid "Context Hell". simpler global stores (like Zustand) are preferred if simple Context isn't enough.

## 5. Styling (Tailwind / NativeWind)
- **Utility First**: proper use of utility classes.
- **Ordering**: Follow standard Tailwind class ordering (Layout -> Box Model -> Typography -> Visual -> Misc).
- **Custom Classes**: Avoid `@apply` in CSS files unless creating a reusable abstraction that cannot be a component.
- **Responsiveness**: Use `sm:`, `md:`, `lg:` prefixes for responsive designs.

## 6. Testing Strategy
- **Unit Tests**: Test utility functions and complex logic hooks.
- **Integration/Component Tests**: Test that components render correctly and handle user interactions (e.g., React Testing Library).
- **E2E**: Critical flows (Login, Checkout) should be covered by E2E tests (Playwright).
- **Test ID**: Use `testID` (React Native) or `data-testid` (Web) for selecting elements in tests.

## 7. Git Workflow
- **Branch Naming**:
    - `feature/description-of-feature`
    - `fix/description-of-bug`
    - `refactor/description-of-change`
- **Commit Messages**: Use [Conventional Commits](https://www.conventionalcommits.org/).
    - `feat: add user login`
    - `fix: correct typo in dashboard`
    - `chore: update dependencies`
- **Pull Requests**:
    - PRs must address a specific task.
    - Description should explain *what* changed and *why*.
    - Visual changes must include screenshots.

## 8. Directory Structure (Monorepo)
- Follow the Solito structure:
    - `apps/next`: Next.js app
    - `apps/expo`: Expo app
    - `packages/app`: Shared app code (screens, components, providers)

---
*Maintained by Marcus (Development Manager)*
