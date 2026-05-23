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

## 🌟 What is Agam?

**Agam** is a compiled programming language and toolchain that unifies systems programming, automation, and AI/numerical computing into one coherent language — without splitting into disconnected sub-languages or relying on foreign library wrappers. 

Built on a comprehensive **12+ pillar architecture** and executing a rigorous **6-tier development roadmap**, Agam provides seamless cross-platform native UI capabilities, hardware-accelerated GPU/NPU performance, and world-class cybersecurity primitives. The project is designed from the ground up to offer the ergonomics of Python with the performance guarantees and safety of Rust and C++.

### ⚡ Core Design Principles

| Principle | What it means |
|-----------|---------------|
| 🐍 **Readable** | Ergonomic, indentation-significant syntax for everyday code. |
| 🦀 **Safe** | Rust-like safety, traceable diagnostics, and strong type semantics. |
| 🚀 **Fast** | Direct LLVM backend optimizing to match or exceed optimized `clang++`. |
| 🧠 **AI-Native** | Tensor, autodiff, and numerical workflows are language-native capabilities. |
| 🎯 **Unified** | One language from basic scripts to scalable systems and scientific computing. |

---

## 🛠️ The Technology Stack

Agam's compiler architecture scales from quick iteration to robust production deployment.

* **Multiple Syntax Modes:** 
  * `@lang.base` for clean, Python-like readability.
  * `@lang.base.dynamic` for scripting and dynamic binding.
  * `@lang.advance` for explicit, brace-delimited systems programming.
* **Versatile Backends:** 
  * **LLVM:** The primary AOT product direction for maximum native performance.
  * **JIT (Cranelift):** Fast in-memory execution for testing and local execution loops.
  * **C Backend:** A portable fallback target.
* **Hardware Accelerated:** Built-in `@gpu` kernel syntax, natively lowering to NVPTX and integrating GPU fast-math and memory models directly into the semantic layer.

```agam
@lang.base
fn main():
    let total = 40 + 2
    if total == 42:
        return 0
    return 1
```

### 📊 Performance Snapshot (Same-Host Comparison)

Agam's optimization pipeline, including its unique call-cache specialization layer, delivers highly competitive runtime metrics.

| Target | Runtime | vs. Winner | Memory Footprint |
|--------|--------:|:-----------|:-----------------|
| **Agam LLVM O3 + Call Cache** | **12.5ms** | 🏆 Winner | ~3.6 MiB |
| Clang C O3 | 23.5ms | +88% | ~3.6 MiB |
| Clang++ O3 | 22.8ms | +82% | ~3.6 MiB |
| Rust release | 23.8ms | +91% | ~4.0 MiB |
| Go release | 33.8ms | +171% | ~5.6 MiB |
| CPython | 359.2ms | +2778% | ~11.6 MiB |

*(Note: Agam's native GPU/NPU `@gpu` kernel pipeline actively expands our performance advantage in hardware-accelerated parallel workloads).*

---

## 🗺️ The 6-Tier Strategic Roadmap

Agam is executing against a structured, 6-tier roadmap designed to establish it as a world-class production language:

* **Tier 0: Foundation Completion** — Type system, formal grammar, object model, and module visibility. *(Active Priority)*
* **Tier 1: Developer Experience** — Elite LSP error recovery, zero-friction visual toolchain, and unified package management.
* **Tier 2: Runtime & Security** — World-class cybersecurity (capabilities, taint, formal proofs) and secure supply-chain sandboxing.
* **Tier 3: Platform & Ecosystem** — Universal FFI (zero-friction interop with C/C++/Python/Java), Omni-platform native rendering, and WASM.
* **Tier 4: Performance & Optimization** — GPU/NPU completion, hardware introspection, and a 120 FPS hardware-accelerated visual engine.
* **Tier 5: AI-Native Differentiation** — Autodiff, tensor types, and ML training loop primitives built directly into the language.
* **Tier 6: Frontier** — Self-hosting and AI-native compiler intelligence.

---

## 🏗️ Organization Ecosystem

Agam's ecosystem spans across multiple repositories under the `@agam-lang` organization to cleanly separate compiler internals from platform layers and community tooling.

### 🔧 Core Language & Toolchain
* [`agam`](https://github.com/agam-lang/agam) — The core compiler, CLI (`agamc`), runtime, and optimization pipelines.
* [`std`](https://github.com/agam-lang/std) — The Agam standard library (I/O, networking, data structures).
* [`registry-index`](https://github.com/agam-lang/registry-index) — The central package registry index.
* [`sdk-packs`](https://github.com/agam-lang/sdk-packs) — Pre-built SDK and toolchain bundles for multi-platform distribution.
* [`rfcs`](https://github.com/agam-lang/rfcs) — Language design RFCs and community proposals.

### 🔬 AI & Scientific Ecosystem
* [`agamlab`](https://github.com/agam-lang/agamlab) — A MATLAB-like interactive scientific computing and exploration platform.
* [`agam-ml`](https://github.com/agam-lang/agam-ml) — Machine learning foundations.
* [`benchmarks`](https://github.com/agam-lang/benchmarks) — Comprehensive cross-language benchmark suite covering algorithms, I/O, ML primitives, and GPU offloading.

### 🔌 Tooling & IDE Integrations
* [`agam-vscode`](https://github.com/agam-lang/agam-vscode) — Official VS Code extension providing rich syntax, LSP integration, and debugging.
* [`agam-intellij`](https://github.com/agam-lang/agam-intellij) — Official IntelliJ/IDEA plugin.
* [`agam-cli`](https://github.com/agam-lang/agam-cli) — Extracted CLI utilities and terminal UI components.
* [`playground`](https://github.com/agam-lang/playground) — Web-based environment to run and share Agam code.

### 📚 Libraries & Frameworks
* [`agam-web`](https://github.com/agam-lang/agam-web) — Web framework and routing.
* [`agam-db`](https://github.com/agam-lang/agam-db) — Database drivers and ORM capabilities.
* [`agam-http`](https://github.com/agam-lang/agam-http) / [`agam-json`](https://github.com/agam-lang/agam-json) / [`agam-crypto`](https://github.com/agam-lang/agam-crypto) / [`agam-async`](https://github.com/agam-lang/agam-async)

### 🎓 Learning & Community
* [`agam-book`](https://github.com/agam-lang/agam-book) — The definitive guide to the Agam Programming Language.
* [`agam-by-example`](https://github.com/agam-lang/agam-by-example) — Interactive examples to learn Agam syntax and idioms.
* [`examples`](https://github.com/agam-lang/examples) — Curated example projects demonstrating best practices.
* [`awesome-agam`](https://github.com/agam-lang/awesome-agam) — A curated list of awesome Agam frameworks, libraries, and software.
* [`governance`](https://github.com/agam-lang/governance) — Organization policies, decision-making frameworks, and steering.

---

## 🚀 Quick Start

Get started with Agam directly from source:

```bash
# Build the compiler from source
cargo build -p agam_driver

# Create a new project
agamc new hello_agam && cd hello_agam

# Run with the best available native or JIT backend
agamc run main.agam --fast

# Explicitly use the Cranelift JIT for rapid iteration
agamc run main.agam --backend jit

# Check local toolchain and LLVM readiness
agamc doctor
```

---

## 🤝 Contributing

We welcome contributions across all repositories! Whether you are interested in compiler internals, standard library development, documentation, or benchmarking, there is a place for you.

Please review our [Contributing Guide](https://github.com/agam-lang/.github/blob/main/CONTRIBUTING.md) and [Code of Conduct](https://github.com/agam-lang/.github/blob/main/CODE_OF_CONDUCT.md).

*Note: Every repository in the Agam ecosystem includes an `.agent/` directory containing structured guidance, rule sets, and checklists to support AI-assisted and human collaborative development workflows.*

---

## 📄 License

All repositories under the `agam-lang` organization are dual-licensed under the [MIT License](https://github.com/agam-lang/agam/blob/main/LICENSE-MIT) and the [Apache 2.0 License](https://github.com/agam-lang/agam/blob/main/LICENSE-APACHE).

---

<p align="center">
  <sub>Built with 💜 by the Agam community</sub>
</p>
