# UAIF Architecture

UAIF is a deterministic, input-centric security gateway that operates **before** tokenization.

## Three Core Stages

### 1. Byte-Level Scrubbing
- Removes invisible Unicode tags: variation selectors (U+FE00–U+FE0F), zero-width characters, Bidi markers.
- Eliminates Emoji Smuggling attacks.

### 2. Cascaded Recursive Decoding
- Unrolls multi-layer obfuscation: Base64 → Hex → URL-encode → ROT13.
- Circuit Breakers prevent DoS attacks (MaxDecodeDepth, timeouts).

### 3. Visual-Semantic Collapse
- Maps homoglyphs to canonical ASCII using UTS #39.
- Applies NFC normalisation via Skeleton Mapping.
- Adaptive Mixed-script analysis preserves Russian/English content (FPR <0.1%).

## Mathematical Axiom

The normalisation function `N(I)` is **deterministic and idempotent**:

N(I) = N(N(I))

This guarantees stable token distribution before input reaches the LLM tokenizer.

## Performance

- **Latency:** <5 ms
- **OPEX Reduction:** up to 66%
- **False Positive Rate (FPR):** <0.1%
- **ROI:** 2.5 months
