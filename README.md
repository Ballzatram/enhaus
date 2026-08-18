# Enhaus

**Recovery, matched.**

Enhaus is a proof-of-concept musculoskeletal care navigation and protection platform. The current prototype combines two product concepts:

1. **AI Provider Navigator** — a conversational intake experience that gathers a user's injury context, prior treatment, insurance, and care preferences, checks for basic red-flag symptoms, and ranks matching providers.
2. **Strategy Dashboard** — an interactive summary of the temporary-insurance / MSK-access thesis, product architecture, illustrative economics, risks, and pilot roadmap.

## Run locally

The current POC is intentionally dependency-free.

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

You can also open `index.html` directly in a browser.

## Provider Navigator flow

The demo progressively captures:

- name
- injury / pain description
- body area
- timing and cause
- functional impact
- prior history / prior treatment
- whether a doctor or clinician has evaluated the current issue
- imaging history
- insurance carrier
- preference for in-person vs. virtual care

The conversation is intentionally framed as **care navigation, not medical diagnosis**. A limited red-flag branch halts routine provider matching when certain high-risk symptoms are described.

Provider results are currently generated from mock Charlotte-area records and ranked on:

- specialty / body-area fit
- stated insurance compatibility
- proximity
- in-person / virtual preference
- availability
- baseline provider fit score

## Production architecture

The current browser-only logic is designed to be replaced incrementally rather than rewritten:

```text
User
  ↓
Conversational UI
  ↓
AI intake + structured extraction
  ├─→ Safety / escalation policy
  ├─→ Care-profile JSON
  └─→ Missing-information follow-ups
          ↓
Provider matching service
  ├─→ Provider directory
  ├─→ Specialty taxonomy
  ├─→ Insurance / network verification
  ├─→ Location / travel time
  └─→ Scheduling availability
          ↓
Ranked, explainable matches
```

A production implementation should use a server-side AI endpoint so API credentials never reach the browser. The model should produce schema-constrained structured outputs, while deterministic policy code handles safety escalation and final provider eligibility rules.

## Product thesis

Enhaus separates two distinct needs:

- **Care Now:** transparent, fixed-price access after pain or injury already exists.
- **Injury Protect:** carrier-backed accident protection purchased before the covered injury occurs.

The core thesis is:

> Sell access after pain begins. Sell insurance before pain begins.

The provider-navigation layer can serve both products and becomes the foundation for an outcomes and routing data loop.

## Important

This repository is an early proof of concept. Mock provider data is not a representation of real provider participation, insurance acceptance, clinical quality, appointment availability, or medical advice.