# Veterinary Practice Management — Feature & Functionality Survey

> Candidate #321 · Researched: 2026-05-03

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| ezyVet (IDEXX) | Cloud SaaS | Commercial / quote | https://www.ezyvet.com |
| Shepherd | Cloud SaaS | Commercial / quote | https://www.shepherd.vet |
| Provet Cloud | Cloud SaaS | Commercial / quote | https://www.provet.com |
| Digitail | Cloud SaaS | Commercial / quote | https://digitail.com |
| AVImark (Henry Schein) | Desktop/hybrid | Commercial / quote | https://www.henryscheinvet.com |
| Cornerstone (IDEXX) | Hybrid | Commercial / quote | https://software.idexx.com/products/cornerstone |
| DaySmart Vet | Cloud SaaS | Commercial / from $116/month | https://www.daysmart.com/vet |
| VETport | Cloud SaaS | Commercial / quote | https://www.vetport.com |
| NectarVet | Cloud SaaS | Commercial / per-vet pricing | https://www.nectarvet.com |

---

## Feature Analysis by Solution

### ezyVet (IDEXX)

**Core features**
- Cloud-based electronic medical records (EMR) with SOAP note structure
- Appointment scheduling with calendar management and resource booking
- Billing, invoicing, and payment processing with automated charge capture
- Prescription management and dispensing workflows
- Inventory and product management with automatic deduction on dispensing
- Client communication hub (SMS, email, two-way messaging)
- Client and pet portal with self-service appointment requests
- Reporting and financial analytics dashboards
- Multi-site and multi-doctor support

**Differentiating features**
- Deep bidirectional integration with IDEXX diagnostics suite (VetConnectPLUS, Web PACS)
- REST API with OAuth 2.0 and a formal partner programme supporting hundreds of third-party integrations
- Standard of Care alerts that surface care opportunity reminders based on patient history
- ezyVet Consult — embedded telemedicine consultation module
- Xero accounting integration for automated financial reconciliation

**UX patterns**
- Tab-based navigation with a single-patient-centric view keeping records and invoicing co-visible
- Progressive disclosure: advanced configuration and reporting is hidden behind role-specific menus
- New-practice onboarding support through guided setup wizards and dedicated onboarding specialists

**Integration points**
- REST API at https://developers.ezyvet.com (OAuth 2.0 Client Credentials; 60 calls/min per endpoint; 180 calls/min global)
- IDEXX diagnostics (reference lab + in-house), Antech
- SmartFlow ICU whiteboard, Vet Radar anaesthesia monitoring
- VetEnvoy / Petios for insurance eClaims (UK/AU)
- PayJunction, Stripe for payments
- Xero accounting

**Known gaps**
- Expensive for small or solo practices; pricing is enterprise-oriented
- Customisation of templates and workflows requires significant configuration effort
- Some users report the reporting module is powerful but has a steep learning curve

**Licence / IP notes**
- Proprietary commercial software; acquired by IDEXX Laboratories in 2021
- API access governed by partner agreement; no open-source components advertised

---

### Shepherd

**Core features**
- SOAP-based EMR that simultaneously builds the invoice as treatments are added
- Appointment scheduling tied to individual provider availability
- Automatic charge capture from medical record entries to invoice
- Inventory tracking updated in real time on product administration
- Two-way SMS client messaging (included at no extra charge)
- Digital whiteboard for hospitalised patient status
- Customisable digital forms and intake questionnaires
- Pet portal with appointment requests and prescription refill requests
- Wellness plan management

**Differentiating features**
- TranscribeAI: ambient AI scribe that places spoken exam-room content into the correct SOAP fields in real time
- Founded by a practising veterinarian; UX mirrors actual clinical cognitive flow
- Acquisition of Hippo Manager (March 2025) expanding user base and development capacity
- Consistently highest user satisfaction scores among active PIMS in independent surveys (2024–2025)

**UX patterns**
- Single-page exam flow — no tab switching between record and invoice
- Minimal onboarding friction; reviewers cite same-day readiness for simple practices
- Support response times cited as under two minutes in user reviews

**Integration points**
- Open API enabling custom integrations (diagnostics, telemedicine, payment, insurance, scripting)
- Lab integrations: Heska, Ellie Diagnostics, Zoetis VETSCAN FUSE, MicroVet, IDEXX Web PACS
- Client communication: Weave, Otto Flow
- Chckup patient feedback platform
- WaitWell queue management

**Known gaps**
- Newer entrant; smaller ecosystem of third-party integrations compared to ezyVet or Cornerstone
- Advanced multi-site and corporate group analytics are still maturing
- Specialty and emergency hospital workflows (anaesthesia, ICU boards) less developed than legacy platforms

**Licence / IP notes**
- Proprietary commercial software
- API access available; formal developer documentation not publicly published as of research date

---

### Provet Cloud

**Core features**
- Cloud EMR with SOAP notes, task management, and resource scheduling
- AI Scribe: native AI assistant that drafts SOAP notes during consultations
- Automated discharge instructions generated from consultation content
- Client communication and two-way messaging
- Billing, invoicing, and financial reporting
- Digital whiteboard for hospitalised patients
- Referral portal for specialist case hand-off
- Business intelligence dashboards
- Multi-language support (Danish, English, Finnish, Italian, Norwegian, Spanish, Swedish)

**Differentiating features**
- 150+ integrations and an open REST API with full data ownership guarantees
- Native referral portal enabling seamless specialist communication
- Strong presence in Scandinavian and European markets; regulatory compliance across multiple jurisdictions
- Telemedicine module included natively

**UX patterns**
- Workflow automation rules that trigger tasks, reminders, and communications based on clinical events
- Configurable consultation templates for different species and consultation types
- Role-based dashboards surfacing relevant information per staff type

**Integration points**
- REST API documented at https://developers.provetcloud.com (OAuth 2.0 with PKCE; JSON format)
- Webhooks for event-driven integration
- 150+ named integration partners including diagnostics, payments, accounting, pharmacy
- VetEnvoy / Petios insurance eClaims
- Xero, QuickBooks accounting

**Known gaps**
- Xero integration stability has drawn persistent negative reviews
- Less established in North American market; support availability during US business hours noted as inconsistent
- Some users report UI complexity for staff not trained in veterinary clinical workflows

**Licence / IP notes**
- Proprietary commercial software (Provet, part of Nordhealth group)
- API documented and open to partners; no open-source components

---

### Digitail

**Core features**
- AI-native all-in-one cloud PIMS with 15+ built-in AI workflows
- AI SOAP dictation and ambient documentation
- Smart charge capture minimising missed revenue
- Automated follow-up communications and reminders
- Real-time inventory tracking with automatic deduction on administration
- Client-facing Pet Parent App (scheduling, messaging, medical record access)
- Payment processing via Stripe
- Reporting and analytics

**Differentiating features**
- Positioned explicitly as AI-native with AI embedded throughout the workflow (not bolted on)
- "See up to 2× more patients per day" messaging underpinned by workflow automation
- Over 10,000 veterinary professionals using the platform as of 2025–2026
- Connected Pet Parent App with push notifications and real-time status updates
- 40+ integration partners; partnership programme open for new technology vendors

**UX patterns**
- Patient flow board providing at-a-glance visual status of all active patients
- Sleek, modern interface noted by reviewers as easiest to navigate among cloud alternatives
- Onboarding varies; some reviewers cite excellent experience, others slower support during migration

**Integration points**
- REST API at https://documentation.digitail.io (OAuth 2.0; JSON; requires partner approval)
- Stripe (payments), SendGrid (email), QuickBooks Online (accounting)
- Diagnostic lab partners, insurance providers, pharmacy networks, telemedicine platforms

**Known gaps**
- API access requires partner approval; not fully self-serve for independent developers
- Smaller ecosystem than ezyVet or Cornerstone at this stage of growth
- Support responsiveness reported inconsistently across reviews

**Licence / IP notes**
- Proprietary commercial software
- API available to approved partners; no open-source components

---

### AVImark (Henry Schein Veterinary Solutions)

**Core features**
- Electronic medical records and appointment calendars
- Patient reminders (automated recall by interval or rule)
- Dental charting module
- Estimates, invoicing, and accounts receivable
- Financial reporting suite
- Boarding calendar and kennel management
- Integration with 50+ third-party vendors and service providers
- AXIS-Q LENS: cloud-based diagnostic results dashboard aggregating data from multiple instruments

**Differentiating features**
- Most widely installed PIMS in North America; 11,000+ hospitals
- Long track record generating extensive training resources and community knowledge
- Hybrid on-premise/cloud data model giving practices control over local data storage
- AXIS-Q LENS provides trended diagnostics across multiple point-of-care instruments and reference labs

**UX patterns**
- Traditional desktop application paradigm; familiar for long-term users
- Extensive configuration options that require significant setup time
- Broad third-party training ecosystem (VetMedTeam, veterinary schools)

**Integration points**
- 50+ integration partners including PetDesk, Weave, VitusVet, Otto, Chckup, FetchIt, Next In Line
- IDEXX diagnostics, Antech
- Payment processing (multiple options, premium pricing common)

**Known gaps**
- Dated UI; desktop-centric architecture limits mobile and remote access
- Cloud capabilities are a hybrid overlay rather than native cloud
- Support quality degradation noted by reviewers following Covetrus acquisition and subsequent restructuring
- No native AI documentation or clinical decision support

**Licence / IP notes**
- Proprietary commercial software (Henry Schein Veterinary Solutions)
- Closed API ecosystem; integrations require formal partner agreements

---

### Cornerstone (IDEXX)

**Core features**
- Robust EMR with customisable templates and problem lists
- Appointment scheduling, multi-resource management
- Diagnostic ordering and result viewing natively integrated with IDEXX reference and in-house lab
- IDEXX Web PACS imaging within the PIMS
- Inventory and dispensary management
- Automated invoicing workflows
- Patient alerts for care opportunities and compliance gaps
- Multi-site support for hospital groups

**Differentiating features**
- Deepest native IDEXX diagnostics integration of any PIMS in the market
- Market-dominant position in larger hospitals and specialty/emergency settings
- IDEXX's full product stack (Neo, ezyVet, Cornerstone) provides upgrade path from startup to enterprise
- Long compliance and audit trail features for controlled substance and DEA reporting

**UX patterns**
- Feature-rich interface designed for multi-doctor, high-volume environments
- Role-based access control with granular permissions
- Heavy configuration required at setup; long-term payoff in automation and reporting

**Integration points**
- IDEXX integration ecosystem (largest in veterinary)
- Curated partner connectors for diagnostics, Web PACS, payments, booking
- No public open API; integrations through formal IDEXX partner programme

**Known gaps**
- Legacy architecture; cloud migration incremental rather than native
- High total cost of ownership; significant upfront and annual fees
- Less suited to small or startup practices
- Limited native telemedicine and client-facing digital features vs. newer entrants

**Licence / IP notes**
- Proprietary commercial software (IDEXX Laboratories)
- Closed API; partner programme required for integrations

---

### DaySmart Vet

**Core features**
- Cloud-based EMR with collaborative SOAP notes
- Online appointment booking with automated confirmations and reminders
- Digital intake forms sent to clients pre-appointment
- One- and two-way SMS texting
- Integrated credit card processing
- Inventory management
- Wellness plan creation and management
- 80+ practice performance reports
- Client-facing pet portal

**Differentiating features**
- Transparent, publicly listed pricing starting at $116/month; rare in the category
- Pay-as-you-grow model accessible for single-doctor startup practices
- 24/7 phone and email support included at all tiers
- 30+ partner integrations covering the core integration needs of small practices

**UX patterns**
- Designed explicitly for non-technical users and new-to-digital practices
- Onboarding materials and walkthroughs reduce time-to-first-appointment
- Mobile-friendly cloud interface accessible on any browser

**Integration points**
- 30+ partner integrations
- Integrated payment processing (in-house)
- Diagnostic lab connections
- Client communication tools

**Known gaps**
- Limited workflow automation depth compared to Provet Cloud or Digitail
- No native body diagram or anatomy marking for physical examination documentation
- Email delivery issues for clients using Gmail accounts (reported by multiple reviewers)
- Fewer integrations than enterprise-grade alternatives; not suited to large multi-doctor hospitals

**Licence / IP notes**
- Proprietary commercial software
- No open API advertised; integrations via curated partner programme

---

### VETport

**Core features**
- SOAP-based EMR with species-specific templates
- Appointment scheduling for single and multi-doctor practices
- Boarding and kennel management module
- Inventory and basket management
- Online appointment booking
- Multi-species support including equine, mixed-animal, and mobile practice modules
- SMS and email reminders
- Lab order and result management

**Differentiating features**
- Global reach: 12,500+ vets across 20+ countries with currency and regulatory flexibility
- Dedicated modules for equine, exotic, mobile, and mixed-animal practices
- Integration with Gribbles (AU/NZ lab), Fuji Labs, Avid (microchip)
- Slack integration for internal team communication
- AWS-based infrastructure for global availability

**UX patterns**
- Modular design allowing practices to activate only the features needed
- Multi-currency and multi-language support for international markets
- Mobile-optimised for mobile and farm-call practitioners

**Integration points**
- 20+ third-party integrations
- IDEXX, Antech, Gribbles, Fuji Labs, Avid
- VetEnvoy for insurance eClaims
- Open Edge, Direct Connect for payments
- Vet Rocket client communication

**Known gaps**
- UI complexity noted in reviews; steeper learning curve than newer entrants
- Smaller North American partner ecosystem than ezyVet or Cornerstone
- Less AI-native functionality compared to Digitail or Provet Cloud

**Licence / IP notes**
- Proprietary commercial software
- Integration partnerships through formal agreements

---

### NectarVet

**Core features**
- AI-assisted SOAP note generation completing exam documentation in under five minutes
- Appointment scheduling and online booking
- Two-way SMS messaging
- Inbuilt payment system
- Client-facing pet portal
- Zoetis diagnostics integration (VETSCAN FUSE and lab services)
- Startup-focused onboarding with dedicated support

**Differentiating features**
- Marketed exclusively at startup and new-graduate-owned practices
- Per-vet pricing model avoids per-transaction or flat-fee penalties for growing practices
- AI SOAP automation cited as reducing documentation time to under five minutes per appointment
- Dedicated startup support team provides personalised implementation assistance

**UX patterns**
- Minimal feature set intentionally curated for simplicity; avoids overwhelming new practice owners
- Guided onboarding reduces time to first live appointment
- Mobile-first design for practitioners accessing from multiple locations

**Integration points**
- Zoetis diagnostics and lab services
- Payment processing (inbuilt)
- Two-way SMS platform

**Known gaps**
- Feature depth insufficient for established or multi-doctor hospitals
- Smaller integration ecosystem than enterprise alternatives
- Limited reporting and analytics depth
- No disclosed open API for third-party development

**Licence / IP notes**
- Proprietary commercial software
- No open API advertised as of research date

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- SOAP-based electronic medical records with autosave
- Appointment scheduling with automated reminders (SMS + email)
- Integrated billing, invoicing, and payment processing
- Inventory management with automatic deduction on product administration
- Diagnostic lab order and result integration (IDEXX or Antech minimum)
- Client-facing portal with appointment requests and medical record access
- Two-way SMS client messaging
- Practice performance reporting and financial dashboards
- Controlled substance / DEA-compliant drug logging
- Multi-user, role-based access control

### Differentiating Features
- Ambient AI SOAP dictation and transcription (TranscribeAI, Provet AI Scribe, NectarVet AI)
- Open REST API with OAuth 2.0 and formal partner ecosystem
- Native telemedicine / video consultation module
- Referral portal for specialist case handoff (Provet Cloud)
- Automatic charge capture eliminating manual invoicing steps (Shepherd, Digitail)
- Digital whiteboard for hospitalised patients with real-time status
- Wellness plan creation and automated compliance tracking
- Pet parent mobile app with push notifications

### Underserved Areas / Opportunities
- Predictive wellness recall using patient history, breed risk, and local disease data — all existing systems rely on fixed-interval reminders
- Intelligent missed-charge detection and billing optimisation surfaced in real time rather than post-visit
- Structured clinical coding (SNOMED CT Veterinary Extension) integrated into the EMR workflow — no PIMS currently enforces or guides standardised coding at the point of care
- Cross-practice benchmarking and population health analytics — data remains siloed per practice
- Specialist-to-generalist referral workflow automation — existing tools are ad hoc
- Integrated pet insurance direct billing with automated pre-authorisation
- Body diagram / anatomy marking for physical examination documentation — notably absent even in leading platforms
- AI-powered differential diagnosis suggestion at the point of creating an assessment
- True multi-species forms and dose calculators that adapt dynamically to species, breed, and weight

### AI-Augmentation Candidates
- SOAP note generation from ambient audio (partially addressed by TranscribeAI, HappyDoc, Scribenote, VetRec — mostly as add-on products, not native PIMS features)
- Missed charge and under-coding detection applied to completed invoices
- Predictive recall scheduling based on patient risk factors rather than fixed intervals
- Clinical decision support: differential diagnosis suggestions, drug interaction checking, dose calculation
- Discharge summary and client instruction drafting in plain language matched to client communication preferences
- Controlled substance reconciliation and anomaly detection

---

## Legal & IP Summary

All solutions surveyed are proprietary commercial software under vendor-held licences. No open-source PIMS with significant market adoption was identified (OpenVPM is a nascent open-source initiative but had no evidence of material adoption at research date). Integration APIs are uniformly governed by partner agreements — none of the major vendors publish fully public, unauthenticated API specifications. No patents covering specific veterinary software features were identified in the research, though IDEXX's tight bundling of diagnostics hardware and software may raise vendor-lock concerns for practices evaluating independence. SNOMED CT Veterinary Extension is freely available under UMLS licence and represents the only standardised open IP asset directly relevant to the domain. There are no identified copyright or licence compatibility issues that would prevent an open-source alternative from being built.

---

## Recommended Feature Scope

**Must-have (MVP)**
- SOAP-based EMR with autosave, problem list, and species-aware templates
- Appointment scheduling with calendar, provider availability, and automated SMS/email reminders
- Billing, invoicing, and integrated payment processing with automatic charge capture from the medical record
- Inventory management with automatic deduction on dispensing
- Diagnostic lab integration (at minimum read/write for IDEXX and Antech)
- Controlled substance / DEA drug log with reconciliation reports
- Role-based access control for staff permissions

**Should-have (v1.1)**
- Ambient AI SOAP note generation from exam-room audio
- Client-facing pet portal with appointment requests, messaging, and medical record access
- Two-way SMS and email communication hub
- Wellness plan and automated recall scheduling (AI-driven, not fixed-interval)
- Basic practice performance and financial reporting suite
- REST API with OAuth 2.0 for third-party integrations

**Nice-to-have (backlog)**
- Native telemedicine / video consultation module with billing
- Referral portal for specialist case handoff with structured data transfer
- Body diagram and anatomy marking in the physical examination record
- SNOMED CT Veterinary Extension coding at the point of assessment
- AI-powered differential diagnosis suggestions
- Pet insurance direct billing and pre-authorisation workflow
- Multi-site / corporate group analytics and benchmarking dashboard
