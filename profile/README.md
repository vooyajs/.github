# Vooya

**Rust/WASM component islands for existing Vue and React applications.**

Vooya lets a Rust-backed `.voo` component own one isolated DOM subtree while the
host application keeps its framework tree, routing, and business state.

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
