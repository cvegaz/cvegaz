### Carlos Vega — Backend Engineer

I build production systems where a language model does the perceiving and
deterministic code does the deciding.
Python · FastAPI · Go · PostgreSQL · AWS.

---

**[Voxa](https://github.com/cvegaz/voxa)** · [tryvoxa.com](https://tryvoxa.com)
Voice-to-spreadsheet capture: you upload an Excel template, Voxa reads its
schema, transcribes what you narrate and fills the row. FastAPI · React ·
PostgreSQL on AWS, provisioned with Terraform. Releases carry no long-lived
credentials and no inbound SSH — GitHub OIDC into AWS, multi-arch images to
GHCR, rollout through SSM. 600+ tests that run with no network and no API key.

**[voxa-core](https://github.com/cvegaz/voxa-core)**
The engine underneath, extracted once a second product showed how much of the
first was domain-agnostic: transcription, the LLM call with retry and error
translation, tolerant JSON parsing, the data contracts. Products consume it
through a single prompt-builder seam, so no domain leaks into the generic path.

**PlayPro Stats** · [playprosystems.com](https://playprosystems.com)
Voice play-by-play statistics for American football, built for a paying client.
The model extracts only what was narrated — an unmentioned field stays absent,
never a courtesy zero — while a deterministic rules engine computes downs,
possession, turnovers, yard-line math and scoring. An eval harness scores
per-field accuracy against a golden narration set. Private repo; the engine
above is public.

---

**How I work.** Test-first, and the tests run offline by design. Every
non-trivial decision is written down as an ADR in the repo, with the
alternatives I rejected and what the choice costs — 19 in Voxa, 28 in
playPro Stats.

**The full portfolio, with the trade-offs spelled out →
[cvegaz.github.io](https://cvegaz.github.io)**
