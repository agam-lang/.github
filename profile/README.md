<p align="center">
  <img src="https://img.shields.io/badge/Agam-Language-blueviolet?style=for-the-badge&logoColor=white" alt="Agam Language" />
  <img src="https://img.shields.io/badge/status-Active_Development-brightgreen?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/backends-LLVM_%7C_JIT_%7C_C-orange?style=for-the-badge" alt="Backends" />
  <img src="https://img.shields.io/badge/license-MIT%2FApache--2.0-blue?style=for-the-badge" alt="License" />
</p>

<h1 align="center">🔮 Agam Programming Language</h1>

<p align="center">
  <strong>One language. Systems to AI. Native performance.</strong>
</p>

<p align="center">
  <em>Python-level readability · Rust-like safety · clang++-class native performance · AI-native workflows</em>
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

### ⚡ Design Principles

| Principle | What it means |
|-----------|---------------|
| 🐍 **Readable** | Python-level readability for everyday code |
| 🦀 **Safe** | Rust-like safety with traceable compiler diagnostics |
| 🚀 **Fast** | Competes with optimized `clang++` on proven workloads |
| 🧠 **AI-Native** | Tensor, autodiff, and numerical workflows are language-native |
| 🎯 **Unified** | One language from scripts to systems to scientific computing |

### 📊 Performance Snapshot (Same-Host Comparison)

| Target | Runtime | vs. Winner |
|--------|--------:|:-----------|
| **Agam LLVM O3 + Call Cache** | **12.5ms** | 🏆 Winner |
| Clang C O3 | 23.5ms | +88% |
| Clang++ O3 | 22.8ms | +82% |
| Rust release | 23.8ms | +91% |
| Go release | 33.8ms | +171% |
| CPython | 359.2ms | +2778% |

---

## 🏗️ Organization Ecosystem

### 🔧 Core Language

| Repository | Description | Status |
|------------|-------------|--------|
| [`agam`](https://github.com/agam-lang/agam) | Core compiler, CLI (`agamc`), runtime, MIR/HIR/codegen | ⚙️ Active |
| [`std`](https://github.com/agam-lang/std) | Agam standard library | 📋 Scaffolded |
| [`agam-lang.github.io`](https://github.com/agam-lang/agam-lang.github.io) | Documentation website | 📋 Scaffolded |

### 🔬 Ecosystem & Platform

| Repository | Description | Status |
|------------|-------------|--------|
| [`agamlab`](https://github.com/agam-lang/agamlab) | MATLAB-like interactive scientific computing platform | 📋 Scaffolded |
| [`registry-index`](https://github.com/agam-lang/registry-index) | Central package registry index | 📋 Scaffolded |
| [`sdk-packs`](https://github.com/agam-lang/sdk-packs) | Pre-built SDK & toolchain bundles | 📋 Scaffolded |
| [`rfcs`](https://github.com/agam-lang/rfcs) | Language design RFCs and proposals | 📋 Scaffolded |

### 🔌 Tooling & IDE

| Repository | Description | Status |
|------------|-------------|--------|
| [`agam-vscode`](https://github.com/agam-lang/agam-vscode) | VS Code extension (syntax, LSP, snippets) | 📋 Scaffolded |
| [`agam-intellij`](https://github.com/agam-lang/agam-intellij) | IntelliJ/IDEA plugin | 📋 Scaffolded |
| [`playground`](https://github.com/agam-lang/playground) | Web-based Agam playground | 📋 Scaffolded |

### 📚 Community & Learning

| Repository | Description | Status |
|------------|-------------|--------|
| [`examples`](https://github.com/agam-lang/examples) | Curated example projects and tutorials | 📋 Scaffolded |
| [`benchmarks`](https://github.com/agam-lang/benchmarks) | Cross-language benchmark suite | 📋 Scaffolded |
| [`governance`](https://github.com/agam-lang/governance) | Organization policies & decision-making | 📋 Scaffolded |

---

## 🚀 Quick Start

```bash
# Build the compiler from source
cargo build -p agam_driver

# Create a new project
agamc new hello_agam && cd hello_agam

# Run with the best available backend
agamc run main.agam --fast

# Or use the JIT for quick iteration  
agamc run main.agam --backend jit

# Check toolchain readiness
agamc doctor
```

---

## 🔧 Compiler Architecture

```
Source (.agam) → Lexer → Parser → AST → Sema → HIR → MIR → { LLVM | JIT | C }
```

| Backend | Purpose | Status |
|---------|---------|--------|
| **LLVM** | Native AOT compilation | ⚙️ Primary product direction |
| **JIT** | Cranelift-based in-memory execution | ✅ Working |
| **C** | Portable fallback backend | ✅ Working |

---

## 📊 Platform Support

| Platform | Status |
|----------|--------|
| Windows x86_64 | ✅ Active |
| Linux x86_64 | ✅ Active |
| Android ARM64 | 🟡 In progress |
| macOS / iOS | 📋 Planned |

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](https://github.com/agam-lang/.github/blob/main/CONTRIBUTING.md) and [Code of Conduct](https://github.com/agam-lang/.github/blob/main/CODE_OF_CONDUCT.md).

Every repository includes an `.agent/` directory with structured guidance for AI-assisted development workflows.

---

## 📄 License

All repositories under `agam-lang` are dual-licensed under [MIT](https://github.com/agam-lang/agam/blob/main/LICENSE-MIT) and [Apache 2.0](https://github.com/agam-lang/agam/blob/main/LICENSE-APACHE).

---

<p align="center">
  <sub>Built with 💜 by the Agam community</sub>
</p>
