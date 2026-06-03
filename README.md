# turphViz-feed

Generated, **sanitized public feed** for [turphViz](https://turphviz.vercel.app) — the
live visualization of the turph suite.

`feed.json` is produced by the publisher on the mini (turphAI/turphOps `publisher.py`)
from the suite's `_ops` artifacts, projected through an explicit field **whitelist**. It
carries only non-sensitive signal — node/edge topology, run statuses, agent heartbeats,
and event headlines. **No payloads, no PII/PHI.** Nothing here is hand-authored; it's
machine-generated and overwritten each publish.

Consumed at runtime via jsDelivr:
`https://cdn.jsdelivr.net/gh/turphAI/turphViz-feed@main/feed.json`
