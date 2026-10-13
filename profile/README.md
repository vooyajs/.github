# Vooya

**Keep JavaScript. Move only the expensive part.**

We build Rust-powered tools that fit into existing JavaScript applications.
Keep the familiar APIs and application architecture; move a focused workload
to the runtime that suits it.

The name comes from “voyage to island”: JavaScript stays the application
surface, while a bounded capability travels to Rust/WASM in the browser or
native Rust in Node.js.

[Documentation](https://vooyajs.com/) ·
[Getting started](https://vooyajs.com/guide/getting-started) ·
[中文指南](https://vooyajs.com/zh-CN/guide/getting-started) ·
[Examples & experiments](https://vooyajs.github.io/vooya-lab/)

## Rust and WASM in your existing web app

[Vooya](https://github.com/vooyajs/vooya) connects Rust Components and Stores to
web applications. Write ordinary `.rs` files and import them through a framework
adapter. Vooya handles compilation, WASM loading, typed bindings, props and
events, state subscriptions, lifecycle, and cleanup.

[![Vooya architecture: bundlers and native toolchains at build time; framework adapters, WASM, and browser APIs at runtime.](https://raw.githubusercontent.com/vooyajs/vooya/main/docs/public/architecture.svg)](https://vooyajs.com/)

Rust is the implemented language provider. Vue and React are supported;
Solid and Svelte are experimental. Vite is the primary bundler path, with
experimental Rspack and Webpack integrations in the opt-in alpha. Dashed
providers in the diagram show planned extensions, not shipped language support.

Start with the **beta** quickstart; the **0.2 alpha** is an explicit opt-in.
The optional alpha preset prepares native Rust build tools. Browsers run the
generated JS and WASM. See [project status](https://vooyajs.com/project/status)
and the [compatibility matrix](https://vooyajs.com/project/compatibility) for
current support and prerequisites.

## Projects

| Project | What it does |
| --- | --- |
| [Vooya](https://github.com/vooyajs/vooya) | Rust/WASM Components and Stores for existing web applications |
| [Vooya FS](https://github.com/vooyajs/fs) | Native Rust batch filesystem operations behind a Node-style API; the continuation of Rush-FS |
| [Vooya Lab](https://github.com/vooyajs/vooya-lab) | Runnable browser experiments and integration evidence |

Choose the boundary first, then measure the workload. Moving code to Rust or
WASM does not automatically make it faster.

## Join in

Bring a real use case, report a bug, or help with a focused improvement.
Read [Contributing](https://github.com/vooyajs/vooya/blob/main/CONTRIBUTING.md),
browse [good first issues](https://github.com/vooyajs/vooya/issues?q=is%3Aissue%20is%3Aopen%20label%3A%22good%20first%20issue%22),
or start a [discussion](https://github.com/orgs/vooyajs/discussions).
