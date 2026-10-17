# Freehold

**Your data, on hardware you control.** Freehold is an open-source stack for a personal AI agent that holds your context locally, decides what may leave the device under policies you write, and proves things about you without revealing them.

Formerly *Personal Context Infrastructure (PCI)*. Apache-2.0.

## What is here

Everything lives in one repository, [freehold-earth/freehold](https://github.com/freehold-earth/freehold):

| Directory | What it is |
|---|---|
| `context-store/` | Encrypted, local-first storage with CRDT sync and on-device semantic search (TypeScript) |
| `agent/` | The personal agent: policy evaluation, request synthesis, local inference (Python) |
| `spec/` | S-PAL, the policy language that states what may be disclosed, to whom, for how long, for what use and where it may be processed; protocol specs; reference encoder |
| `contracts/` | On-chain enforcement of S-PAL commitments on Cardano (Aiken) |
| `zkp/` | Zero-knowledge proof service on Midnight (Compact + TypeScript) |
| `identity/` | W3C DIDs: `did:key` today, Midnight Passport planned |
| `demo/` | Interactive demo apps |
| `infra/` | Docker Compose for development and test |
| `docs/` | Manifesto, architecture, and the architecture decision records |

## Where to start

- [Manifesto](https://github.com/freehold-earth/freehold/blob/main/docs/concepts/manifesto.md): why this exists
- [Technical manifesto](https://github.com/freehold-earth/freehold/blob/main/docs/architecture/technical-manifesto.md): the five-layer architecture
- [Architecture decisions](https://github.com/freehold-earth/freehold/tree/main/docs/decisions): including [ADR-008](https://github.com/freehold-earth/freehold/blob/main/docs/decisions/008-positioning-nightframes-passport.md) on how Freehold relates to Midnight's Passport and agent vision
- [Project board](https://github.com/users/peteski22/projects/1) and [open issues](https://github.com/freehold-earth/freehold/issues), labelled by `area:<directory>`

## Principles

- **Local-first.** Context and the model that reasons over it stay on devices you or your community control by default.
- **Policy, not promises.** S-PAL terms are cryptographically committed and enforced on-chain, not written into a privacy policy.
- **Prove, don't reveal.** Verifiers get a zero-knowledge proof of the claim they need, not the data behind it.
- **Community cloud.** When a phone or laptop is not enough, a library, co-op or family server you know beats a hyperscaler you don't.

Built on [Cardano](https://cardano.org) and [Midnight](https://midnight.network). Not affiliated with either.
