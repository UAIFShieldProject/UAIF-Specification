[🇷🇺 Русский](./README.ru.md) | [🇬🇧 English](./README.md)

---

# UAIF — Universal AI Filter

**Deterministic, input‑centric security specification for LLMs**  
Protects against Emoji Smuggling, Homoglyph attacks, and tokenization‑level exploits.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/UAIFShieldProject/UAIF-Specification.svg?style=social)](https://github.com/UAIFShieldProject/UAIF-Specification)

---

## 📖 Table of Contents

- [About](#-about)
- [Key Features](#-key-features)
- [Architecture](#-architecture)
- [Quick Start](#-quick-start)
- [Documentation](#-documentation)
- [License](#-license)
- [Contributing](#-contributing)

---

## 🧠 About

**UAIF** is an open‑source standard for deterministic LLM security. Unlike probabilistic Guardrails (NeMo, Llama Guard, Azure Prompt Shield), UAIF operates **before tokenization** and cleans input data at the byte level, without trying to "guess" the attacker's intent.

The project is published as **Prior Art** under the MIT License to prevent patenting and provide the industry with a free, verifiable standard.

---

## ⚡ Key Features

- **Deterministic** – no ML classifiers, pure mathematics.
- **Byte‑level normalisation** – removes invisible Unicode chars, variation selectors, and control codes.
- **Recursive decoding** – unrolls multi‑layer obfuscation (Base64, Hex, ROT13) with DoS protection.
- **Homoglyph filtering** – two‑stage visual‑semantic collapse (UTS #39 + NFC).
- **Adaptive Mixed‑script analysis** – preserves multilingual text without degradation (FPR <0.1%).
- **CPU‑native** – <5 ms latency, up to 66% OPEX reduction.
- **Bidirectional Security** – filters RAG context and agent tool calls.

---

## 🏗 Architecture

UAIF is a three‑stage pre‑processing gateway:

1. **Byte‑Level Scrubbing** – removes invisible control characters.
2. **Cascaded Recursive Decoding** – unwraps nested encodings.
3. **Visual‑Semantic Collapse** – normalises homoglyphs and mixed scripts.

**Mathematical axiom:**  
`N(I) = N(N(I))` — the normalisation function is deterministic and idempotent.

---

## 🚀 Quick Start

1. **Read the specification:**  
   📄 [PDF version](./spec/UAIF_Specification_v2.pdf)

2. **Explore the LaTeX source:**  
   📝 [LaTeX file](./spec/UAIF_Specification_v2.tex)

3. **Browse documentation:**  
   📚 [Architecture](./docs/architecture.md) | [Use Cases](./docs/use-cases.md) | [FAQ](./docs/faq.md)

4. **Join the community:**  
   Open issues, suggest improvements, fork and submit Pull Requests.

---

## 📚 Documentation

- [Full Specification (PDF)](./spec/UAIF_Specification_v2.pdf)
- [LaTeX Source](./spec/UAIF_Specification_v2.tex)
- [Architecture Overview](./docs/architecture.md)
- [Use Cases](./docs/use-cases.md)
- [FAQ](./docs/faq.md)
- [Full Manifesto (Russian)](./docs/manifesto.md)

---

## 📄 License

This project is released under the **MIT License**. See [LICENSE](./LICENSE) for details.

---

## 🤝 Contributing

We welcome contributions of all kinds: typo fixes, examples, translations, code improvements.  
Please read [CONTRIBUTING.md](./CONTRIBUTING.md).

---

## 📝 Citation

If you use UAIF in your research or products, please cite:

Brailovsky, A. (2026). Universal AI Filter (UAIF): A Deterministic Input-Centric Shield for Mitigating Tokenization-Level LLM Vulnerabilities. arXiv preprint.

@article{brailovsky2026uaif,
  title = {{Universal AI Filter (UAIF): A Deterministic Input-Centric Shield for Mitigating Tokenization-Level LLM Vulnerabilities}},
  author = {Brailovsky, Aleksandr},
  journal = {arXiv preprint},
  year = {2026}
}

---

© 2026 Studio "Architects" | UAIF™