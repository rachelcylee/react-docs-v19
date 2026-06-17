# React 19 Documentation Study

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-black?logo=next.js&logoColor=white)
![Notion](https://img.shields.io/badge/Notes-Notion-black?logo=notion&logoColor=white)

A week-by-week study log working through the official React documentation (react.dev), rebuilt around React 19. Full notes — with code examples, diagrams, and screenshots — are written up in Notion; this repo is the index.

## Structure

| Week | Focus | Topics | Notion |
|---|---|---|---|
| 1 | Setup & Fundamentals | Environment setup (Node, Yarn, CRA); what React is and how SPA/CSR rendering works; component tree structure; intro to hooks (`useState`, `useEffect`, `useContext`); component design principles (loose coupling, high cohesion, DRY, SRP); managing state with `useState` (the Tic-Tac-Toe board example); events & why lists need keys; the Virtual DOM and reconciliation; basic JSX | [link](https://react-docs-study.notion.site/Week1-29bde7fcec3d81868529c91c6b3e909a) |
| 2 | Next.js Project Setup & Data Fetching | Setting up Next.js with TypeScript; comparing Client-Side, Server-Side, and Static data fetching (trade-offs and when to use each); Tailwind CSS install troubleshooting | [link](https://react-docs-study.notion.site/week2-29bde7fcec3d80f288c4c0ec8bfc3088) |
| 3 | Tooling & TypeScript | ESLint/Prettier setup; typed components and hooks (`useState`, `useReducer`, `useContext`, `useMemo`, `useCallback`); `interface` vs `type`; React Developer Tools; React Compiler (automatic memoization, opt-in/opt-out directives) | [link](https://react-docs-study.notion.site/Week3-29bde7fcec3d812d9787f2c89416811c) |
| 4 | Describing the UI (I) | Your first component; importing/exporting components; root components and routing (SPA vs MPA, Next.js file-based routing, hydration, streaming + `Suspense`); JSX syntax rules; using JavaScript in JSX; passing props (defaults, spread, children) | [link](https://react-docs-study.notion.site/Week4-29bde7fcec3d815485bdcc891a5b92c6) |
| 5 | Describing the UI (II) | Conditional rendering; rendering lists with `map`/`filter` and keys; keeping components pure (side effects, Strict Mode); the UI as a tree — render tree vs module dependency tree, and how a bundler actually builds (transpile → tree-shake → minify → bundle) | [link](https://react-docs-study.notion.site/Week5-29bde7fcec3d81268742c0450fb03609?pvs=74) |
| 6 | Adding Interactivity (I) | Event handling and propagation (capture/bubble, `stopPropagation`, `preventDefault`); state as a component's memory; the render-and-commit cycle, including a deep dive into the Fiber tree, reconciliation, double buffering, and the scheduler | [link](https://react-docs-study.notion.site/Week6-29bde7fcec3d81c9b65ed131fe91766b?pvs=74) |
| 7 | Adding Interactivity (II) | State as a snapshot (closures and why stale state happens in handlers); batching and queued state updates; updating object and array state immutably | [link](https://react-docs-study.notion.site/Week7-29bde7fcec3d81d19ebeca53661d386b?pvs=74) |
| 8 | Managing State (I) | Reacting to input with state (the 5-step declarative UI process); structuring state (avoiding redundancy, contradictions, and deep nesting); lifting state up; controlled vs uncontrolled components | [link](https://react-docs-study.notion.site/Week8-29bde7fcec3d81c2a358ef39a867868a?pvs=74) |
| 9 | Escape Hatches | Refs vs state; manipulating the DOM with refs; React 19's `ref`-as-a-prop (replacing `forwardRef`); `useImperativeHandle`; `flushSync` | [link](https://react-docs-study.notion.site/Week9-29bde7fcec3d81d0aed5e83d4d408948?pvs=74) |


## Beyond the docs

A few weeks go past what the official docs cover on the surface: Week 6 traces the Fiber tree and scheduler internals behind "render and commit," Week 7 digs into closures and lexical scope to explain why stale state happens in event handlers, and Week 5 breaks down what a bundler is actually doing during a production build.

## React 19 notes

A couple of things specifically called out as new in React 19 while going through the docs:

- `ref` can now be passed as a regular prop to function components — `forwardRef` is no longer needed for the common case.
- The React Compiler can automatically memoize components and values, reducing manual `useMemo`/`useCallback`/`React.memo` usage.

## Format

Each week's full notes live in Notion (code blocks render better there, and there are screenshots that don't translate well to markdown). This README is meant as a table of contents — click through to a week for the complete writeup.
