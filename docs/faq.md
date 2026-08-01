# UAIF — Frequently Asked Questions

### What problem does UAIF solve?
Current LLM security relies on probabilistic Guardrails that fail against sub-symbolic attacks (Emoji Smuggling, Homoglyphs, Zero-Width injections). UAIF is deterministic and sanitises input before tokenization.

### How is UAIF different from Guardrails (NeMo, Llama Guard)?
- **Guardrails** are probabilistic (ML classifiers) – they can be bypassed.
- **UAIF** is deterministic – no guessing, no hallucinations, runs on CPU.

### Does UAIF require GPU?
No. UAIF runs on standard CPU servers with <5 ms latency.

### Is UAIF open source?
Yes. UAIF is released under the MIT License.

### Does UAIF work with any LLM?
Yes. UAIF is agnostic – it works with GPT, Claude, GigaChat, YandexGPT, and any other LLM.

### How can I contribute?
Read [CONTRIBUTING.md](../CONTRIBUTING.md).

### Where can I read the full specification?
[UAIF_Specification_v2.pdf](../spec/UAIF_Specification_v2.pdf)

### Is UAIF patented?
UAIF is published as **Prior Art** under the MIT License. The concept is defensively published to prevent others from patenting it.
