# Ambit

**An open protocol for describing, authorizing and proving what AI agents do.**

Ambit is developed in the open by a group of researchers and engineers at [Ond](https://ond.cc). We found that the actions of autonomous agents lack a common governance abstraction, so we set out to build an open protocol for it. To prove it can run in real systems, we built [OSuite](https://ond.cc/osuite), its reference implementation.

The same action, such as a production deploy or a refund, can reach a real system as a shell command, a tool call or an API request. Ambit gives that action one shared description: what it is, what it may affect, who may authorize it, within what bounds it runs and what proof remains.

## Layers and status

| Layer | What it defines | Status |
| --- | --- | --- |
| Action | One canonical identity for an action across runtimes | Research, runs in OSuite |
| Effects | What an action may do, its evidence and what is still unknown | Published draft: [Action Effect Spec](https://github.com/OndCo/Action-Effect-Spec) |
| Authority | Who holds final authority, and an approval bound to the exact action | Research, runs in OSuite |
| Bounds | A lease that limits actor, session, destination, policy version and time | Research, runs in OSuite |
| Evidence | Receipts that survive replay, and rules for reusing evidence | Research; receipts run in OSuite |
| Conformance | Offline tests anyone can run, with no OSuite account | Published draft: [Action Effect Bench](https://github.com/OndCo/Action-Effect-Bench) |

Ambit is a working draft, not an adopted standard. The published layers currently live in the OndCo organization. Full overview: [ond.cc/ambit](https://ond.cc/ambit).

## Principle

The protocol should not depend on OSuite. OSuite should depend on the protocol.

## Take part

- Implement the effects layer in your own agent runtime.
- Open an issue wherever the specification is wrong, vague or too narrow.
- Run the benchmark against your implementation.
- Build an implementation that never touches OSuite.

Specifications and tests are MIT licensed.
