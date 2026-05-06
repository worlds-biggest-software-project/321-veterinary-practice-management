# Veterinary Practice Management

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source veterinary practice information management system (PIMS) covering patient records, appointments, billing, and prescription management.

Veterinary Practice Management is a candidate project for an open-source PIMS targeting independent and small-to-mid-size veterinary practices. It addresses the core operational needs of a clinic — SOAP-based EMR, scheduling, billing, inventory, diagnostic lab integration, and client communication — while embedding AI throughout the workflow rather than bolting it on as an upsell.

---

## Why Veterinary Practice Management?

- Almost all major PIMS (ezyVet, Cornerstone, Shepherd, Provet Cloud, AVImark) are quote-only, with mid-size hospital total cost of ownership commonly running $10,000–$50,000+ in year one.
- The most widely installed system in North America, AVImark, is desktop-centric with a dated UI and no native AI documentation or clinical decision support.
- Cornerstone and ezyVet are both owned by IDEXX, raising vendor-lock concerns for practices that want diagnostic-supplier independence.
- Ambient AI scribes (TranscribeAI, HappyDoc, Scribenote, VetRec) exist mostly as add-on products rather than native PIMS features, fragmenting the workflow.
- No open-source PIMS has achieved material market adoption; OpenVPM remains nascent. SNOMED CT Veterinary Extension is freely available under UMLS licence and is not enforced or guided at the point of care by any current PIMS.

---

## Key Features

### Electronic Medical Records

- SOAP-based EMR with autosave, problem list, and species-aware templates
- Automatic charge capture from medical record entries to invoice
- Digital whiteboard for hospitalised patient status
- Customisable digital intake forms and consultation templates
- Controlled substance / DEA-compliant drug logging with reconciliation reports

### Scheduling, Billing & Inventory

- Appointment scheduling with provider availability and resource booking
- Automated SMS and email reminders
- Integrated billing, invoicing, and payment processing
- Inventory management with automatic deduction on dispensing
- Practice performance and financial reporting

### Diagnostics & Clinical Workflow

- Bidirectional diagnostic lab integration (IDEXX, Antech at minimum)
- Prescription management and dispensing workflows
- Referral portal for specialist case handoff with structured data transfer
- Wellness plan creation and automated compliance tracking
- Body diagram and anatomy marking in the physical examination record

### Client Engagement

- Two-way SMS and email communication hub
- Client-facing pet portal with appointment requests, messaging, and medical record access
- Native telemedicine / video consultation module with billing
- Pet parent mobile app with push notifications

### Platform & Integration

- REST API with OAuth 2.0 for third-party integrations
- Role-based access control with granular permissions
- Multi-site and multi-doctor support
- Webhooks for event-driven integration

---

## AI-Native Advantage

Ambient AI SOAP note generation from exam-room audio places spoken content directly into the correct SOAP fields in real time, addressing documentation overhead cited as a leading cause of veterinary burnout. AI-powered diagnostic triage cross-references symptom inputs with lab results and patient history to surface differential diagnoses before the vet enters the room. Predictive wellness recall uses patient history, breed risk factors, and local disease prevalence rather than fixed-interval reminders, while intelligent missed-charge detection flags under-coded procedures in real time — a recoverable revenue source commonly estimated at 5–15% of practice billings. Natural-language drafting of discharge summaries and follow-up messages adapts to each pet owner's communication history.

---

## Tech Stack & Deployment

Cloud-native deployment is expected, matching the >80% of new PIMS implementations that are cloud-based, with a path to self-hosted operation for practices that want local data control. Open standards include AAHA accreditation requirements, AVMA digital records guidelines, DEA 21 CFR Part 1304 controlled substance logging, IDEXX/Antech diagnostics integration protocols, VetXML/EDIFACT for inter-vendor data exchange, and SNOMED CT Veterinary Extension for structured clinical coding. A documented REST API with OAuth 2.0 and webhooks enables third-party integrations across diagnostics, payments, accounting, insurance, and pharmacy partners.

---

## Market Context

The veterinary practice management software market is estimated at USD 718 million–1.52 billion in 2026, projected to grow at 9–13% CAGR to USD 1.2–4.6 billion by 2032–2035. Incumbent pricing is overwhelmingly quote-only; the rare transparent option (DaySmart Vet) starts at $116/month, while mid-size hospital total cost of ownership typically runs $10,000–$50,000+ in year one. Primary buyers are solo and small practice owners, multi-doctor independent hospitals, veterinary corporate groups, and emergency/specialty hospitals.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
