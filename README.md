## Emekcan Doğru

Founder at **[VERAX](https://verax-ai.com)** (İzmir, Türkiye). I work on the boundary
between AI systems and real company data — specifically, on making what happens at that
boundary provable rather than asserted.

### Conarium

[**conarium.dev**](https://conarium.dev) · [source (MIT)](https://github.com/dogrucanemek-alt/conarium) · `@conarium-ai/core` on npm

A governed gateway between AI assistants and databases. Three things it does, in the
order they matter:

- **Enforces before disclosure** — table allow-lists, row caps, deterministic masking,
  and columns that may not appear in a predicate at all.
- **Signs a portable receipt** for every access — hash-chained, verifiable offline by a
  single file that imports nothing from the package it checks.
- **Reconciles against the source's own counters** — because a log written by the
  gateway cannot reveal an access that never reached it.

Running in production at one company: 121,366 identities masked across 121,374 records.
[What that number is, and what it is not.](https://conarium.dev/report-001.html)

### Standards work

[**draft-dogru-scitt-disclosure-evidence**](https://datatracker.ietf.org/doc/draft-dogru-scitt-disclosure-evidence/)
— an IETF Internet-Draft defining two evidence payloads for auditable data disclosure:
transformation evidence and coverage reconciliation, carried as Signed Statements on a
SCITT Transparency Service ([RFC 9943](https://www.rfc-editor.org/info/rfc9943)).

It deliberately defines payloads only. Delegation receipts, policy replay and
transparency logs are other people's work, and the draft says so.

### GACS

A vendor-neutral adversarial conformance suite for governed data access. Any
implementation can run it through a small adapter; the runner imports nothing from
mine. It reports capability status rather than a score, and it ships the cases my own
implementation **fails** next to the ones it passes — a suite whose author scores full
marks proves nothing.

### How I work

Claims are cheap, so this project publishes its own limits:
[LIMITATIONS.md](https://github.com/dogrucanemek-alt/conarium/blob/main/LIMITATIONS.md)
lists what Conarium does not do, including the inference channels that remain open.
[PRIOR-ART.md](https://github.com/dogrucanemek-alt/conarium/blob/main/docs/PRIOR-ART.md)
lists everyone else I could find doing similar work, and exists to be corrected.

One-person team. No SOC 2, no independent penetration test, one production deployment.
Those are on the roadmap, and they are not claimed before they exist.

---

📫 [e.dogru@conarium.dev](mailto:e.dogru@conarium.dev) · [conarium.dev](https://conarium.dev) · [verax-ai.com](https://verax-ai.com)
