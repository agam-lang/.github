<p align="center">
  <img src="https://img.shields.io/badge/Agam-Language-blueviolet?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHRleHQgeD0iNTAlIiB5PSI1MCUiIGRvbWluYW50LWJhc2VsaW5lPSJjZW50cmFsIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmb250LXNpemU9IjIwIj7wn5SFPC90ZXh0Pjwvc3ZnPg==&logoColor=white" alt="Agam Language" />
  <img src="https://img.shields.io/badge/status-Active_Development-brightgreen?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/backends-LLVM_%7C_JIT_%7C_C-orange?style=for-the-badge" alt="Backends" />
</p>

<h1 align="center">🔮 Agam Programming Language</h1>

<p align="center">
  <strong>One language. Systems to AI. Native performance.</strong>
</p>

<p align="center">
  Python-level readability · Rust-like safety · clang++-class native performance · AI-native workflows
</p>

---

## What is Agam?

**Agam** is a compiled programming language and toolchain that unifies systems programming, automation, and AI/numerical computing into one coherent language — without splitting into disconnected sub-languages or relying on foreign library wrappers.

```agam
@lang.base
fn main():
    let total = 40 + 2
    if total == 42:
        return 0
    return 1
```

### Key Design Goals

- 🐍 **Python-level readability** for everyday code
- 🦀 **Rust-like safety** with traceable compiler diagnostics
- ⚡ **clang++-class native performance** on proven workloads
- 🧠 **AI, tensor, and numerical workflows** as language-native constructs

### Performance Snapshot

On the same host, same workload (`fibonacci` recursive), Agam LLVM O3 with call-cache lands at **12.5ms** — faster than Clang++ O3 (22.8ms), Rust release (23.8ms), and Go release (33.8ms).

---

## 🏗️ Organization Repositories

### Core Language

| Repository | Description |
|------------|-------------|
| [`agam`](https://github.com/agam-lang/agam) | Core compiler, CLI (`agamc`), runtime, MIR/HIR/codegen |
| [`std`](https://github.com/agam-lang/std) | Agam standard library |
| [`agam-lang.github.io`](https://github.com/agam-lang/agam-lang.github.io) | Documentation website |

### Ecosystem & Platform

| Repository | Description |
|------------|-------------|
| [`agamlab`](https://github.com/agam-lang/agamlab) | MATLAB-like interactive scientific computing platform |
| [`registry-index`](https://github.com/agam-lang/registry-index) | Central package registry index |
| [`sdk-packs`](https://github.com/agam-lang/sdk-packs) | Pre-built SDK & toolchain bundles |
| [`rfcs`](https://github.com/agam-lang/rfcs) | Language design RFCs and proposals |

### Tooling & IDE

| Repository | Description |
|------------|-------------|
| [`agam-vscode`](https://github.com/agam-lang/agam-vscode) | VS Code extension (syntax, LSP, snippets) |
| [`agam-intellij`](https://github.com/agam-lang/agam-intellij) | IntelliJ/IDEA plugin |
| [`playground`](https://github.com/agam-lang/playground) | Web-based Agam playground |

### Community & Learning

| Repository | Description |
|------------|-------------|
| [`examples`](https://github.com/agam-lang/examples) | Curated example projects and tutorials |
| [`benchmarks`](https://github.com/agam-lang/benchmarks) | Cross-language benchmark suite |
| [`governance`](https://github.com/agam-lang/governance) | Organization policies & decision-making |

---

## 🚀 Quick Start

```bash
# Build the compiler from source
cargo build -p agam_driver

# Create a new project
agamc new hello_agam
cd hello_agam

# Run with the best available backend
agamc run main.agam --fast

# Or use the JIT for quick iteration
agamc run main.agam --backend jit
```

---

## 🔧 Compiler Architecture

```
Source → Lexer → Parser → AST → Sema → HIR → MIR → { LLVM | JIT | C }
```

Agam compiles through a multi-layer pipeline with three execution backends:

- **LLVM** — Primary native AOT path (product direction)
- **JIT** — Cranelift-based in-memory execution for fast iteration
- **C** — Portable fallback backend

---

## 📊 Backends & Targets

| Platform | Status |
|----------|--------|
| Windows x86_64 | ✅ Active |
| Linux x86_64 | ✅ Active |
| Android ARM64 | 🟡 In progress |
| macOS / iOS | 📋 Planned |

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](https://github.com/agam-lang/.github/blob/main/CONTRIBUTING.md) and [Code of Conduct](https://github.com/agam-lang/.github/blob/main/CODE_OF_CONDUCT.md).

---

## 📄 License

Agam is dual-licensed under [MIT](https://github.com/agam-lang/agam/blob/main/LICENSE-MIT) and [Apache 2.0](https://github.com/agam-lang/agam/blob/main/LICENSE-APACHE).

---

<p align="center">
  <sub>Built with 💜 by the Agam community</sub>
</p>
