# Enhaus Scope of Work

**North star:** Build a trusted MSK front door that routes people to the right care, makes the economics understandable, and stays connected through the episode.

The working thesis is that Enhaus should first prove it can aggregate and route demand into efficient musculoskeletal care. Carrier-backed future-accident protection can be added after the care engine works. Enhaus should not retain insurance risk or perform AI diagnosis at launch.

## Workstreams

### 1. Consumer product and AI intake
- Natural-language intake and structured extraction
- Missing-information follow-up logic
- Location, payment and modality preferences
- Explainable care-path recommendation
- Mobile-first booking and transaction experience
- Production server-side model integration with schema-constrained outputs

### 2. Clinical safety and governance
- Clinician-reviewed red-flag rules
- Escalation workflows
- Non-diagnostic language and scope controls
- Routing-policy versioning and audit logs
- Outcome and safety review process

### 3. Provider graph and network
- Recruit 10–20 Charlotte provider locations for the first pilot
- Track specialty, modality, geography, availability, pricing and payer participation
- Define provider quality and outcome fields
- Build a provider-data adapter/API rather than hard-coding records

### 4. Care episodes and provider economics
- Define the initial Care Now episode
- Replace illustrative pricing with signed provider economics
- Define consumer payment and provider settlement flows
- Test fixed-price vs insurance-verification routes
- Measure provider acquisition/admin savings and capacity value

### 5. Insurance architecture
- Engage accident-and-health regulatory counsel
- Determine licensed business-entity/producer structure
- Obtain carrier and administrator/TPA interest or term sheets
- Design future-accident benefits and exclusions
- Keep existing symptoms outside the insured product
- Avoid retaining underwriting risk at launch

### 6. Employer and embedded distribution
- Test employer navigation pilots
- Test sports, gym, outdoor and membership channels
- Measure CAC and conversion by channel
- Use broad pre-injury populations for future insurance distribution

### 7. Data, analytics and outcomes
- Intake → recommendation → booking conversion
- Time to first appointment
- Episode completion and support utilization
- Functional outcomes and escalation
- Provider cohort performance
- Repeat and referral behavior
- Insurance attachment, persistency and claims once live

### 8. Investor and financial diligence
- Maintain TAM/SAM/SOM model
- Maintain competitive map
- Maintain state regulatory architecture
- Update provider and insurance economics with real contracts
- Maintain 5-year operating scenarios and downside sensitivities

## Phase plan

### Phase 1 — Prove the care engine
**Target:** Charlotte MVP.

Build the intake, safety-routing, provider-matching, payment-choice and booking flow. Develop a dense initial provider network and run 1,000–2,500 completed episodes.

**Gate:** positive and repeatable episode contribution, strong booking conversion, acceptable clinical-safety performance and useful appointment access.

### Phase 2 — Prove distribution leverage
Add 2–5 employer/embedded pilots, expand provider density and compare DTC acquisition economics against employer, sports, gym and membership channels.

**Gate:** B2B2C distribution produces materially better CAC, conversion, retention or volume quality than pure DTC.

### Phase 3 — Attach future-risk protection
Launch only through a compliant licensed structure with a carrier retaining underwriting risk. Integrate enrollment and covered-claim navigation into the Enhaus care network.

**Gate:** the insured layer adds margin, retention or partner value without confusing consumers or weakening the core care product.

### Phase 4 — Replicate market economics
Expand into additional metros using a repeatable provider-contracting, product and enterprise-distribution playbook.

**Gate:** provider economics, conversion, outcomes and channel CAC replicate outside Charlotte.

## Key evidence gates

1. **Consumer trust:** intake → recommendation → booking conversion.
2. **Provider economics:** signed rates and demonstrated provider-side value.
3. **Access:** median time to a useful first appointment, initially targeting <72 hours.
4. **Clinical safety:** clinician-approved escalation policy and audited performance.
5. **Outcomes:** measurable functional improvement and escalation cohorts.
6. **Distribution:** CAC and retention by DTC vs employer/embedded channel.
7. **Insurance fit:** carrier term sheet, consumer comprehension, attachment and persistency.

## Explicitly out of scope at launch

- Retaining insurance underwriting risk
- Becoming a comprehensive health plan
- AI medical diagnosis
- Building a shallow nationwide provider network before local density
- Simple provider-paid referral bounties without healthcare-law approval
- Internal claims administration before the economics justify TPA licensing/operations
- Medicare/Medicaid monetization assumptions before federal/state healthcare-law review

## Current public POC

- `index.html` — investor thesis
- `diligence.html` — quantified diligence
- `experience.html` — end-to-end Try Enhaus experience
- `scope.html` — visual scope of work
- `navigator.html` — legacy route / compatibility link

## Important

This scope is a strategic development document, not legal, medical, actuarial, accounting or investment advice. Healthcare and insurance counsel, licensed clinical governance, privacy/security architecture and carrier/provider contracting are required before a real launch.
