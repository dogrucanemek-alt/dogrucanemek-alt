## Emek Can Doğru

Founder at **[VERAX](https://verax-ai.com)**. I work on the boundary between AI systems
and the things a company cannot afford to get wrong — its data and its money — and on
making what happens at that boundary provable rather than asserted.

Three products, one claim: a machine action should carry its own evidence.

### Conarium — governed data access

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

### Cedulon — the audit layer for agent-to-agent commerce

[**cedulon.com**](https://cedulon.com) · [source (Apache-2.0)](https://github.com/dogrucanemek-alt/cedulon) · `@cedulon/*` on npm, eight packages with build provenance

When agents start spending money, the hard part is not the payment. It is the evidence.

- A **trade manifest** is signed before the spend, so the offer cannot be rewritten after it.
- The policy decision point **denies by default**; an allowed payment gets a COSE_Sign1 receipt.
- Epoch **checkpoints** and a transparency log make the receipt chain append-only.
- A **rail-extract reconciliation** compares the chain against the payment rail in both
  directions, so a settlement with no receipt is named rather than assumed.

Missing evidence is itself evidence. It settles on a mock rail: no wallet is held and no
transaction is signed.

### Tugra — provenance-aware agent memory

[**tugra-ai.com**](https://tugra-ai.com) · [source (Apache-2.0)](https://github.com/dogrucanemek-alt/tugra) · `tugra` on npm

A memory format where every claim carries its source, its age and its boundary — the
subject the agent must not improvise on, which stays quarantined until a human approves
it. Stale facts announce themselves instead of ageing quietly into confident answers.

### Standards work

Four IETF Internet-Drafts, sole author. Individual submissions: not adopted by a working
group and not endorsed by the IETF. The drafts, the review threads and the
interoperability results are public, which is the point.

| Draft | Rev | What it defines |
|---|---|---|
| [draft-dogru-cedulon](https://datatracker.ietf.org/doc/draft-dogru-cedulon/) | -05 | The Cedulon protocol: manifest, decision token, receipt, checkpoint, reconciliation |
| [draft-dogru-cedulon-reattestation](https://datatracker.ietf.org/doc/draft-dogru-cedulon-reattestation/) | -00 | Carrying spend evidence across algorithm retirement |
| [draft-dogru-cedulon-streaming](https://datatracker.ietf.org/doc/draft-dogru-cedulon-streaming/) | -00 | Continuous completeness for agent spend |
| [draft-dogru-scitt-disclosure-evidence](https://datatracker.ietf.org/doc/draft-dogru-scitt-disclosure-evidence/) | -07 | Transformation evidence and coverage reconciliation, as Signed Statements on a SCITT Transparency Service ([RFC 9943](https://www.rfc-editor.org/info/rfc9943)) |

The SCITT draft deliberately defines payloads only. Delegation receipts, policy replay
and transparency logs are other people's work, and the draft says so.

### GACS

A vendor-neutral adversarial conformance suite for governed data access. Any
implementation can run it through a small adapter; the runner imports nothing from
mine. It reports capability status rather than a score, and it ships the cases my own
implementation **fails** next to the ones it passes — a suite whose author scores full
marks proves nothing.

### How I work

Claims are cheap, so these projects publish their own limits:
[LIMITATIONS.md](https://github.com/dogrucanemek-alt/conarium/blob/main/LIMITATIONS.md)
lists what Conarium does not do, including the inference channels that remain open.
[PRIOR-ART.md](https://github.com/dogrucanemek-alt/conarium/blob/main/docs/PRIOR-ART.md)
lists everyone else I could find doing similar work, and exists to be corrected.

Everything ships first inside my own 36-year-old furniture company, where a bad
assumption costs real money before it can cost anyone else's.

One-person team. No SOC 2, no independent penetration test, one production deployment.
Those are on the roadmap, and they are not claimed before they exist.

---

📫 [e.dogru@conarium.dev](mailto:e.dogru@conarium.dev) · [conarium.dev](https://conarium.dev) · [cedulon.com](https://cedulon.com) · [tugra-ai.com](https://tugra-ai.com) · [emekcandogru.com](https://emekcandogru.com)
