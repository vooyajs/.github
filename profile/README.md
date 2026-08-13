# Vooya

**Keep JavaScript. Move only the expensive part.**

Vooya builds Rust-powered libraries that fit into existing JavaScript applications.
Instead of asking teams to rewrite an app, we keep familiar JavaScript APIs and
application architecture, then move a focused workload to the runtime best
suited to handle it.

The name comes from “voyage to island”: JavaScript stays the application surface,
while a bounded workload travels to the right island—native Rust through FFI,
Rust/WASM in the browser, or another environment-specific runtime.

## Start here

- [Vooya repository](https://github.com/vooyajs/vooya) — compiler, Vite plugin,
  framework adapters, examples, and verification suite.
- [Documentation](https://github.com/vooyajs/vooya/tree/main/docs) — setup,
  component authoring, ownership boundary, tooling, and current status.
- [Examples](https://github.com/vooyajs/vooya/tree/main/examples) — Vue and
  React source components, a task list, data grid, Canvas scatter plot, and
  trace-waterfall diagnostic demo.
- [Discussions](https://github.com/orgs/vooyajs/discussions) — questions and
  design conversations.

## Projects

| Project | Familiar JavaScript boundary | Island |
| --- | --- | --- |
| [Rush-FS](https://github.com/vooyajs/fs) | Node-style filesystem API | Native Rust bindings for filesystem work |
| [Vooya](https://github.com/vooyajs/vooya) | Vue/React component import | Rust/WASM-owned UI subtree |

Neither project asks an application to be rewritten in Rust. Each changes a
focused boundary and leaves the surrounding JavaScript application in place.

## What exists today

- Rust from `.voo` files compiled into application-level WebAssembly.
- Vite imports for Vue 3 and React 19 source components.
- Typed component props and events, scoped styles, source-mapped Rust
  diagnostics, and automated browser checks.
- A Vue precompiled-artifact reference path that consumers can use without a
  Rust toolchain.

Vooya is currently an alpha. Source component authors need Rust and the pinned
WASM toolchain; React precompiled-artifact consumption, SSR, hydration, and
state-preserving HMR are not implemented. WebAssembly is not assumed to make
ordinary DOM work faster—see the documented benchmark evidence before drawing a
performance conclusion.

## Contributing

Read the [project status](https://github.com/vooyajs/vooya/blob/main/docs/project/status.md),
run the relevant checks, and include a minimal reproduction for bugs. The
repository is dual-licensed under [MIT](https://github.com/vooyajs/vooya/blob/main/LICENSE-MIT)
or [Apache-2.0](https://github.com/vooyajs/vooya/blob/main/LICENSE-APACHE).
