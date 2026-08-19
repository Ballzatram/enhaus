# Enhaus

**Own the MSK decision before anyone else owns the patient.**

Enhaus is a proof-of-concept musculoskeletal care navigation and transaction platform. The working thesis is that Enhaus can become the consumer front door for MSK care: understand intent, route safely, compare payment paths, match a provider, book care, measure the episode, and later attach carrier-backed protection for future accidental injuries.

> **Sell access after pain begins. Sell insurance before pain begins.**

## Public proof of concept

GitHub Pages: `https://ballzatram.github.io/enhaus/`

- `index.html` — investor thesis, market structure, competitive map, regulatory architecture and 5-year scenario
- `diligence.html` — quantified TAM/SAM/SOM, provider economics, insurance economics and Charlotte launch diligence
- `experience.html` — end-to-end **Try Enhaus** product mock
- `scope.html` — visual product and diligence scope of work
- `SCOPE.md` — working implementation scope and evidence gates
- `navigator.html` — compatibility route to the newer experience

## Product concept

The end-to-end experience is designed around five stages:

1. **Understand** — conversational intake converts natural language into a structured care profile.
2. **Route** — deterministic safety rules and non-diagnostic logic identify an appropriate first care path or escalate.
3. **Compare** — the user compares a transparent episode with an insurance-verification route.
4. **Book** — Enhaus ranks providers on specialty, price/payment fit, location, modality and availability.
5. **Stay connected** — Enhaus can track the episode, outcomes and escalation, then separately introduce future-accident protection.

The current demo uses synthetic provider records, illustrative prices and mock appointment availability. It does not diagnose, verify benefits, create appointments or sell insurance.

## Business thesis

The strongest Enhaus model has three revenue engines sharing one infrastructure layer:

- **Care transactions** — transparent MSK episodes and transaction/admin economics.
- **Navigation/software** — employer, provider and embedded-partner infrastructure.
- **Future-risk protection** — producer/MGA/admin economics around carrier-backed accident coverage purchased before a covered injury.

The core defensibility hypothesis is **not the insurance policy or AI chat itself**. It is a dense provider graph plus demand aggregation, transaction history, routing-to-outcome data and contracting leverage.

## Launch strategy

The current scope prioritizes a concentrated Charlotte pilot:

- 10–20 provider locations
- clinician-reviewed safety routing
- transparent episode pricing
- insurance-verification comparison
- 1,000–2,500 completed episodes in the initial operating test
- measured intake → recommendation → booking → completion funnel
- measured time to appointment, unit economics, outcomes and escalation
- employer / sports / gym / embedded channel pilots before broad geographic scale

See [`SCOPE.md`](SCOPE.md) for the full work plan and phase gates.

## Production architecture

```text
Consumer / Employer / Embedded Partner
                ↓
        Conversational Enhaus UI
                ↓
 AI intake + structured extraction
        ├── Safety policy / escalation
        ├── Care-profile schema
        └── Missing-info follow-ups
                ↓
        Provider matching service
        ├── Provider graph
        ├── Specialty + quality
        ├── Pricing / insurance
        ├── Geography / modality
        └── Availability
                ↓
       Payment / booking decision
        ├── Transparent episode
        └── Insurance verification
                ↓
      Episode + outcomes data loop
                ↓
 Optional future accident protection
     through licensed carrier stack
```

A production AI implementation should be server-side so credentials and protected data are not exposed in the browser. Models should produce schema-constrained structured outputs; deterministic policy code and licensed clinical governance should own safety escalation and final eligibility logic.

## Regulatory design principle

Enhaus should avoid regulated roles it does not need at launch. The current research architecture separates:

- Enhaus technology/navigation platform
- independent licensed clinical providers
- licensed insurance business entity / producers
- underwriting carrier
- external TPA / claims administrator when required

Provider referral compensation, corporate-practice rules, insurance producer licensing, TPA/MGA requirements, HIPAA/business-associate obligations, federal program rules and state-by-state PT scope all require qualified counsel before launch.

## Important

This repository is an early strategic and product proof of concept. Provider data, prices, coverage, availability, financial models and insurance economics shown in the site are illustrative unless a primary source is cited. Nothing in the repository is medical, legal, actuarial, accounting or investment advice.
