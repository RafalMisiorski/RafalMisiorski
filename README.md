# Hi, I'm Rafał

I build AI systems and then try to break them. Seven years as a quant in bank risk (stress testing,
model validation) taught me that a number nobody can reproduce is an opinion — so everything I publish
ships with a verification script.

## What I'm working on

A RAG agent in production shape — LangGraph + pgvector, with a grounding gate and a pre-registered
eval (retrieval hit@k, grounding rate, correctness). Building in public, in this profile's repos.

## Evaluation & correctness tooling

Zero dependencies, MIT, each verifiable on a clean clone in about a minute:

- **[sealeval](https://github.com/RafalMisiorski/sealeval)** — keeps AI-evaluation results honest:
  ground truth sha256-sealed *before* any system runs, refute-by-default blind judging. A threshold
  edited after seeing the score breaks the hash and is caught.
- **[provenance-memory](https://github.com/RafalMisiorski/provenance-memory)** — agent memory that
  never serves a stale fact and can always show *why* it recalled a value. Hardened by 5 adversarial
  audits (18 defects → named regression tests); 43 tests, 4,000 fuzz cases, 0.0% stale-recall.
- **[pieceofmind](https://github.com/RafalMisiorski/pieceofmind)** — finds the prompt rule silently
  corrupting your output (leave-one-out + exact Shapley, measured noise floor). On a worked task,
  cutting one flagged rule moved record-correctness 50% → 100%.

The common thread: I'd rather publish where my own work breaks than ship a claim I can't defend.
One of these tools exists because a benchmark I pre-registered disproved my own product's claim —
the method survived, the claim didn't.

## Elsewhere

Multi-agent platform running unattended since Dec 2025 (private) · Kaggle bronze, Hull Tactical
market prediction · MSc Data Science (ensemble NLP classifier, F1 0.983)

📍 Warsaw · [LinkedIn](https://linkedin.com/in/rafal-misiorski)

---
*Bio line (GitHub settings): `Building evaluation tooling for LLM & agent systems — Warsaw`*
*Pinned order: sealeval → provenance-memory → pieceofmind → ARC-AGI-3-Agents*
*Topics per repo: llm-evaluation · agent-memory · prompt-engineering · python*
