# Standards & API Reference

> Project: Veterinary Practice Management · Generated: 2026-05-03

## Industry Standards & Specifications

### ISO Standards

**ISO/IEC 27001 — Information Security Management**
- URL: https://www.iso.org/isoiec-27001-information-security.html
- Widely expected by corporate veterinary groups and insurers as a baseline for cloud-based PIMS vendors. Governs how patient records, financial data, and staff PII are stored and protected.

**ISO 8601 — Date and Time Representation**
- URL: https://www.iso.org/iso-8601-date-and-time-format.html
- Relevant for all scheduling, appointment, and medical record timestamp fields across a multi-timezone PIMS — particularly important for multi-country deployments (ezyVet, VETport, Provet Cloud).

**ISO 4217 — Currency Codes**
- URL: https://www.iso.org/iso-4217-currency-codes.html
- Required for invoicing and billing modules in practices operating across multiple countries or accepting payment in multiple currencies.

---

### W3C & IETF Standards

**RFC 6749 — OAuth 2.0 Authorization Framework**
- URL: https://datatracker.ietf.org/doc/html/rfc6749
- All major veterinary PIMS APIs (ezyVet, Provet Cloud, Digitail) use OAuth 2.0 for API authentication. Defines grant types including Client Credentials (server-to-server integrations) and Authorization Code with PKCE (user-facing integrations).

**RFC 7636 — Proof Key for Code Exchange (PKCE)**
- URL: https://datatracker.ietf.org/doc/html/rfc7636
- Provet Cloud mandates PKCE for public OAuth clients. Recommended as the default for any PIMS API supporting third-party developer access.

**RFC 7231 — HTTP/1.1 Semantics and Content**
- URL: https://datatracker.ietf.org/doc/html/rfc7231
- Baseline for all REST API design across veterinary software integrations; governs status codes, methods, and content negotiation used by all surveyed APIs.

**RFC 8259 — The JavaScript Object Notation (JSON) Data Interchange Format**
- URL: https://datatracker.ietf.org/doc/html/rfc8259
- JSON is the universal data exchange format for all surveyed veterinary PIMS APIs (ezyVet, Provet Cloud, Digitail). Compliance with RFC 8259 ensures interoperability with diagnostic lab connectors and third-party platforms.

**RFC 5988 / RFC 8288 — Web Linking (Pagination)**
- URL: https://datatracker.ietf.org/doc/html/rfc8288
- Relevant for PIMS APIs returning paginated lists (patient records, appointment history, invoice line items). Proper Link header use enables consistent pagination across large datasets.

---

### Data Model & API Specifications

**OpenAPI Specification 3.1 (OAS 3.1)**
- URL: https://spec.openapis.org/oas/v3.1.0.html
- The industry standard for machine-readable REST API documentation. Enables auto-generated client SDKs, interactive documentation (Swagger UI), and contract testing. None of the major PIMS vendors currently publish a full public OAS 3.1 document — this is a gap an open-source alternative could address. OpenVPM (https://openvpm.com) explicitly positions its API-first design as a differentiator.

**SNOMED CT Veterinary Extension (VetSCT)**
- URL: https://vtsl.vetmed.vt.edu/extension/ and https://www.nlm.nih.gov/research/umls/sourcereleasedocs/current/SNOMEDCT_VET/
- Maintained by the Center for Veterinary Terminology and Standards at Virginia Tech under authorisation from SNOMED International. The September 2025 production release is available via UMLS licence. Provides standardised clinical terminology for diagnoses, procedures, and findings aligned with the SNOMED CT International Edition. VetXML's diagnostic code list maps to SNOMED CT. No current PIMS enforces or guides its use at the point of care — a significant interoperability and research opportunity.

**VetXML**
- URL: http://www.vetxml.co.uk
- An XML-based data exchange standard developed in the UK by the VetXML Consortium (co-founded by VetEnvoy/Petios and SPVS). Defines a transport-layer schema for electronic exchange of insurance claims, lab reports, and microchip registrations between PIMS and external systems. Used primarily in the UK market; globally the veterinary sector lacks an equivalent to HL7 FHIR.

**DICOM — Digital Imaging and Communications in Medicine**
- URL: https://www.dicomstandard.org/
- International standard (also published as ISO 12052) for storing, transmitting, and displaying medical imaging data. Used in veterinary radiology (DR/CR, CT, MRI, ultrasound) for PACS integration. IDEXX Web PACS, Fovea Cloud PACS, VisioPACS, and Candelis all implement DICOM. The DICOM Worklist service enables PIMS-to-modality patient data pre-population.

**JSON Schema (Draft 2020-12)**
- URL: https://json-schema.org/specification
- Relevant for validating request and response payloads in PIMS API integrations. Recommended for defining and documenting data models for patient records, invoices, and diagnostic results in any new system.

---

### Regulatory & Compliance Standards

**AAHA Medical Records Standards**
- URL: https://www.aaha.org/trends-magazine/publications/view-from-the-board-considerations-for-choosing-veterinary-practice-management-software/
- Voluntary but widely adopted standards from the American Animal Hospital Association covering minimum medical record content requirements: patient identification, problem list, physical examination record, diagnostic results, diagnoses, treatment plans, and discharge summaries. Accredited hospitals (approximately 12–15% of US practices) must comply; PIMS should make compliance straightforward.

**DEA 21 CFR Part 1304 — Controlled Substance Recordkeeping**
- URL: https://www.dea.gov/drug-regulations
- Federal US requirement mandating records of all Schedule II–V controlled substances be maintained for a minimum of two years (longer in many states). Required fields include: drug name, container size, strength, bottle number, date, explanation of use, lot number, expiration date, amount added, amount used, running balance, and staff initials with waste witness. An estimated 96% of veterinary practices fail DEA inspections due to recordkeeping errors — a high-value automation target.

**AVMA Guidelines for Digital Veterinary Records**
- URL: https://www.avma.org
- Guidance from the American Veterinary Medical Association on maintaining legally defensible electronic patient records including authenticity, correction audit trails, and confidentiality requirements applicable across US state veterinary practice acts.

**GDPR — General Data Protection Regulation (EU)**
- URL: https://gdpr-info.eu/
- Applies to any PIMS processing personal data of EU-based pet owners or staff. Requires prior consent for marketing data processing, right to erasure, data portability, and breach notification within 72 hours. Relevant for Provet Cloud and VETport's European user bases.

**CCPA / CPRA — California Consumer Privacy Act (as amended)**
- URL: https://oag.ca.gov/privacy/ccpa
- Applies to veterinary software vendors and practices operating in California. Post-January 2026 regulations (approved September 2025) add new obligations covering automated decision-making technology, cybersecurity audits, and risk assessments taking effect 2027.

**State Veterinary Practice Acts (US)**
- Each US state maintains its own veterinary practice act governing medical record retention periods (commonly 3–7 years), controlled substance logging requirements, and patient confidentiality. A PIMS must provide configurable retention and export to meet state-specific requirements.

---

### Security & Authentication Standards

**OAuth 2.0 (RFC 6749) + PKCE (RFC 7636)**
- See entries above. Used by all surveyed PIMS APIs; mandatory for any integration scenario involving third-party developer access to patient or billing data.

**OpenID Connect 1.0**
- URL: https://openid.net/connect/
- Identity layer on top of OAuth 2.0; used by Provet Cloud for user authentication via its API. Relevant for multi-tenant PIMS deployments requiring federated identity across corporate veterinary groups.

**OWASP API Security Top 10 (2023)**
- URL: https://owasp.org/API-Security/editions/2023/en/0x00-header/
- Defines the most critical API security risks (broken object-level authorisation, authentication failures, injection, etc.). Especially relevant given that PIMS APIs expose sensitive patient records and financial data. Rate limiting (e.g., ezyVet's 60 calls/min per endpoint) is a partial mitigation for denial-of-service.

**TLS 1.2 / 1.3 (RFC 5246 / RFC 8446)**
- URL: https://datatracker.ietf.org/doc/html/rfc8446
- Baseline encryption requirement for all data in transit for cloud PIMS and their APIs. TLS 1.3 is the current recommended standard; TLS 1.2 may be required for legacy diagnostic equipment connectivity.

**SOC 2 Type II**
- URL: https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services
- Common attestation expected by corporate veterinary chains and enterprise buyers. Covers security, availability, processing integrity, confidentiality, and privacy of cloud-hosted patient and financial data.

---

### MCP Server Specifications

The Model Context Protocol (MCP) is potentially relevant for a new AI-native PIMS or for AI scribe tools that need to read from and write back to a PIMS in real time. As of the research date, no veterinary PIMS has published an MCP server. An open-source PIMS with a published MCP server would allow any MCP-compatible AI agent (Claude, GPT, etc.) to query patient histories, generate SOAP notes, and post structured data back — without bespoke per-integration development. This represents a forward-looking differentiator.

- MCP specification: https://modelcontextprotocol.io/specification
- MCP server development guide: https://modelcontextprotocol.io/docs

---

## Similar Products — Developer Documentation & APIs

### ezyVet

- **Description:** Cloud PIMS owned by IDEXX; dominant in mid-to-large practices and specialty hospitals. REST API used by hundreds of integration partners globally.
- **API Documentation:** https://developers.ezyvet.com/docs/v1/
- **Developer Portal:** https://developers.ezyvet.com/
- **SDKs/Libraries:** Community SDK available on GitHub (https://github.com/anirvanBhaduri/ezyvet-api-sdk — Python query builder; unofficial)
- **Developer Guide:** https://www.ezyvet.com/build-a-custom-integration
- **Standards:** REST / JSON; OAuth 2.0 Client Credentials
- **Authentication:** OAuth 2.0 Client Credentials grant
- **Rate Limits:** 60 calls/min per endpoint; 180 calls/min global per partner
- **Environments:** Production: https://api.ezyvet.com; Trial: https://api.trial.ezyvet.com

---

### Provet Cloud

- **Description:** Cloud PIMS by Nordhealth; strong in Europe and Australasia; 3,000+ clinics in 45+ countries. 150+ integrations with an open REST API and webhooks.
- **API Documentation:** https://developers.provetcloud.com/restapi/
- **Endpoint Reference:** https://developers.provetcloud.com/restapi/endpoints.html
- **Webhooks:** https://developers.provetcloud.com/restapi/webhooks.html
- **Integration Guide:** https://support.provet.cloud/hc/en-gb/articles/360010249038
- **Standards:** REST / JSON; OAuth 2.0 (Authorization Code + PKCE, Client Credentials)
- **Authentication:** OAuth 2.0; access tokens expire after 10 hours; refresh tokens expire after 30 days of non-use
- **Notes:** PKCE is required for public clients; Authorization Code flow for user-facing apps; Client Credentials for background system integrations

---

### Digitail

- **Description:** AI-native cloud PIMS; 10,000+ veterinary professionals; 40+ integration partners. API access available to approved partners, clinics, and technology vendors.
- **API Documentation:** https://documentation.digitail.io/
- **Partnership Programme:** https://digitail.com/partnership-opportunities/
- **Standards:** REST / JSON; OAuth 2.0
- **Authentication:** OAuth 2.0; partner approval required before API credentials are issued
- **Example Endpoint:** `GET https://developer.digitail.io/api/v1/vets/{id}`
- **Notes:** API covers appointments, blood types, breeds, charges, clinics, and veterinary staff. Full endpoint list available post-approval.

---

### Shepherd

- **Description:** Cloud PIMS founded by a practising veterinarian; highest user satisfaction scores in the category; acquired Hippo Manager in March 2025.
- **API Documentation:** Not publicly published; available to integration partners on request
- **Integration Overview:** https://www.shepherd.vet/integrations/
- **Open API blog post:** https://www.shepherd.vet/blog/open-api-access-in-veterinary-software-what-does-it-mean-for-your-practice/
- **Standards:** REST / JSON (inferred from integration blog)
- **Authentication:** Not publicly documented; OAuth 2.0 assumed
- **Notes:** Supports two-way data sharing with named integration partners. Custom integrations (PDF estimates, background data workflows) documented at a high level only.

---

### VetEnvoy / Petios

- **Description:** Veterinary communications hub for eClaims, lab reports, and microchip registrations. Co-founded VetXML Consortium. In 2025 rebranded as Petios and migrated to a SaaS platform.
- **Standard:** VetXML (XML schema for veterinary data exchange, open and freely available)
- **VetXML Consortium:** http://www.vetxml.co.uk
- **ezyVet integration guide:** https://docs.ezyvet.com/en/see-all-integrations/insurance/vetenvoy-insurance/
- **Provet Cloud integration guide:** https://support.provet.cloud/hc/en-gb/articles/7745173692701
- **Notes:** Petios functions as the transport hub; VetXML is the standardised message envelope. Primarily UK-focused; limited North American adoption.

---

### IDEXX Web PACS

- **Description:** Cloud-based PACS (Picture Archiving and Communication System) for veterinary radiology. Integrated natively with Cornerstone and ezyVet; accessible from other PIMS via DICOM interfaces.
- **Product Page:** https://www.idexx.com/en/veterinary/diagnostic-imaging-telemedicine-consultants/web-pacs/
- **Standards:** DICOM (ISO 12052)
- **Authentication:** IDEXX partner/account credentials
- **Notes:** Enables practices to view full diagnostic-quality images within the PIMS. DICOM Worklist service pre-populates patient metadata on imaging modalities from PIMS appointment data.

---

### HappyDoc (AI Veterinary Scribe)

- **Description:** Ambient AI scribe trained on 1.7 million+ veterinary appointments. Generates SOAP notes in real time, pulls patient history from PIMS, and writes structured notes back bidirectionally.
- **Website:** https://happydoc.ai/
- **PIMS Integrations:** Avimark, Cornerstone, Impromed, ezyVet, and others via browser extension
- **Standards:** REST API (inferred); PIMS-specific integration connectors
- **Authentication:** Per-integration credentials
- **Notes:** Scout, HappyDoc's built-in AI assistant, summarises history, edits notes, creates templates, and surfaces practice performance insights. Bidirectional read/write distinguishes it from transcription-only tools.

---

### VetRec

- **Description:** Standalone AI veterinary scribe producing automated SOAP notes from exam-room audio. PIMS-agnostic; output can be pasted or imported.
- **Website:** https://vetrec.io/
- **Standards:** Not publicly documented
- **Notes:** Focused on transcription accuracy with veterinary-tuned language models. No disclosed bidirectional PIMS integration as of research date.

---

### Scribenote

- **Description:** Veterinarian AI scribe app processing multilayered audio inputs through veterinary-specific AI systems. Generates structured SOAP notes with concurrent conversation capture and medical terminology interpretation.
- **Website:** https://scribenote.com/
- **Standards:** Not publicly documented
- **Notes:** Marketed as supporting multilingual audio and complex multi-speaker exam-room environments.

---

## Notes

**Fragmentation of veterinary data standards:** The veterinary sector lacks an equivalent to human healthcare's HL7 FHIR. VetXML is the closest analogue but is confined to the UK insurance and lab-reporting context. SNOMED CT Veterinary Extension provides standardised clinical terminology but no current PIMS integrates it at the point of care. An open-source PIMS that adopts SNOMED CT coding as a first-class data model would be a significant step toward interoperability and research data reuse.

**API openness gap:** All major commercial PIMS restrict API access through partner agreements, with no publicly self-serviceable developer environments. This is a meaningful barrier to the veterinary technology ecosystem and a direct opportunity for an open-source, API-first alternative.

**MCP opportunity:** No veterinary PIMS has published an MCP server. As AI agents become standard tools in clinical workflows, a PIMS exposing an MCP interface would enable any compliant AI agent to read patient history, draft SOAP notes, and post structured records back — without bespoke per-integration development. This could become a decisive architectural advantage for a new entrant.

**Controlled substance compliance:** DEA 21 CFR Part 1304 requirements are highly structured and rule-based — an ideal automation target. Current solutions (VetSnap, CUBEX, Repleni-Trac) are stand-alone add-ons rather than native PIMS features. A PIMS with built-in DEA-compliant controlled substance logging and automated reconciliation would reduce one of the highest-risk compliance gaps in the industry.
