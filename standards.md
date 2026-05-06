# Standards & API Reference

> Project: Food Safety & Traceability · Generated: 2026-05-03

## Industry Standards & Specifications

### ISO Standards

**ISO 22000:2018 — Food Safety Management Systems**
- URL: https://www.iso.org/standard/65464.html
- The primary international standard for food safety management. Specifies requirements for any organisation in the food chain to demonstrate its ability to control food safety hazards. Relevant to system design for audit readiness, HACCP integration, and documentation workflows.

**ISO 22005:2007 — Traceability in the Feed and Food Chain**
- URL: https://www.iso.org/standard/36297.html
- General principles and basic requirements for the design and implementation of a feed and food traceability system. Directly applicable to data models, scope definition (one-step-back / one-step-forward), and system architecture decisions.

**ISO/IEC 15459 — Unique Identifiers for Transport Units, Packages, and Goods**
- URL: https://www.iso.org/standard/54781.html
- Defines the structure of unique item identifiers (UIIs) used in supply chain management. Underpins GS1 GTIN, SSCC, and GLN schemes used in food traceability lot coding.

**ISO/IEC 19987:2017 — EPCIS Standard (GS1 adoption)**
- URL: https://www.iso.org/standard/70557.html
- ISO/IEC ratification of GS1 EPCIS, providing governmental and regulated-sector recognition. Enables compliance claims with EPCIS-based traceability systems in formal procurement and regulatory contexts.

**ISO 31000:2018 — Risk Management**
- URL: https://www.iso.org/standard/65694.html
- Risk management principles applicable to food safety hazard assessment workflows and supplier risk scoring features of a traceability platform.

---

### GS1 Standards (De-Facto Global Trade Standards)

**GS1 EPCIS 2.0 / CBV 2.0 (ISO/IEC 19987)**
- URL: https://www.gs1.org/standards/epcis
- OpenAPI Spec: https://ref.gs1.org/standards/epcis/openapi.json
- Swagger UI: https://editor.swagger.io/?url=https%3A%2F%2Fref.gs1.org%2Fstandards%2Fepcis%2Fopenapi.json
- Artefacts: https://ref.gs1.org/standards/epcis/artefacts
- The flagship GS1 supply chain visibility standard. EPCIS 2.0 defines a REST/JSON-LD API for capture and query of supply chain events (the "what, when, where, why, and how" of product movements). FSMA 204's Critical Tracking Events (CTEs) and Key Data Elements (KDEs) map directly to EPCIS event structures. Support for food safety extensions (chemical/microorganism concentrations) is included in 2.0.

**GS1 Global Traceability Standard (GTS)**
- URL: https://www.gs1.org/standards/gs1-global-traceability-standard/current-standard
- PDF: https://www.gs1.org/sites/default/files/docs/traceability/GS1_Global_Traceability_Standard_i2.pdf
- Defines the requirements for implementing a traceability system using GS1 identifiers. Provides the conceptual framework (traceability unit, traceability step, traceable item) that maps to database schema design in any food traceability platform.

**GS1 Digital Link**
- URL: https://www.gs1.org/standards/gs1-digital-link
- US Guide: https://www.gs1us.org/industries-and-insights/standards/gs1-digital-link
- Encodes GS1 identifiers (GTIN, batch/lot, best-before date) into a web URI, enabling a single 2D barcode (QR code) to serve POS scanning, supply chain traceability, and consumer product information simultaneously. The GS1 "Sunrise 2027" mandate is driving global adoption of 2D codes on consumer packaging. Directly relevant to consumer-facing traceability features and label generation.

**GS1 US FSMA 204 EPCIS Recommendations**
- URL: https://documents.gs1us.org/adobe/assets/deliver/urn:aaid:aem:0c934e38-7cd7-4a86-aac3-c54b4c9ef293/EPCIS-Recommendations-FSMA-204-Critical-Tracking-Events.pdf
- Practical mapping guide from FDA FSMA 204 CTEs/KDEs to EPCIS 2.0 event structures. Essential reference for any FSMA-compliant traceability system implementation.

---

### Regulatory Frameworks

**FDA FSMA 204 — Food Traceability Final Rule**
- URL: https://www.fda.gov/food/food-safety-modernization-act-fsma/fsma-final-rule-requirements-additional-traceability-records-certain-foods
- Food Traceability List: https://www.fda.gov/food/food-safety-modernization-act-fsma/food-traceability-list
- Requires covered entities to maintain and electronically produce Critical Tracking Events (CTEs) and Key Data Elements (KDEs) within 24 hours of FDA request for foods on the Food Traceability List (fresh produce, cheeses, fish, ready-to-eat deli salads, etc.). Compliance deadline is July 20, 2028 (extended from January 2026). Any food traceability platform targeting the US market must implement FSMA 204 CTE/KDE data structures.

**EU Regulation (EC) No 178/2002 — General Food Law**
- URL: https://www.legislation.gov.uk/eur/2002/178/article/18
- Mandates one-step-forward, one-step-back traceability for all food and feed products at every stage of the supply chain across the EU. Record retention of at least 5 years required. Foundational legal requirement for any platform serving the European market.

**Codex Alimentarius**
- URL: https://www.fao.org/fao-who-codexalimentarius
- International food safety standards developed by FAO/WHO. Provides the global reference framework for food safety, labelling, hygiene, and traceability codes of practice used as baseline requirements in international trade disputes and national legislation worldwide.

**HACCP — Hazard Analysis and Critical Control Points**
- FDA Guidelines: https://www.fda.gov/food/hazard-analysis-critical-control-point-haccp/haccp-principles-application-guidelines
- The internationally recognised preventive framework for identifying and controlling food safety hazards. HACCP compliance is a prerequisite for GFSI-recognised certification schemes (SQF, BRC, FSSC 22000). A food safety traceability platform should support HACCP plan documentation, critical control point (CCP) monitoring data ingestion via IoT/API, and corrective action record-keeping.

**GFSI (Global Food Safety Initiative) Benchmark Schemes**
- URL: https://mygfsi.com/
- An industry-driven initiative that benchmarks food safety management schemes (BRCGS, SQF, FSSC 22000, IFS Food). Certification against a GFSI-recognised scheme is increasingly required by major retailers. Platforms supporting audit readiness and CCP documentation support these certification paths.

---

### W3C & IETF Standards

**W3C Verifiable Credentials Data Model 2.0**
- URL: https://www.w3.org/TR/vc-data-model-2.0/
- W3C Recommendation (May 2025). Provides a standard way to express cryptographically verifiable digital credentials (certificates, audit results, origin claims). Directly applicable to food traceability for issuing tamper-evident certificates of origin, organic certification, and safety inspection results that can be independently verified without relying on a central authority.

**W3C Decentralized Identifiers (DIDs) v1.1**
- URL: https://www.w3.org/TR/did-1.1/
- Standard for globally unique, cryptographically verifiable identifiers that do not require a centralised registry. Applicable to assigning persistent digital identities to food batches, producers, processing facilities, and inspectors in a decentralised traceability architecture.

**JSON-LD 1.1 (W3C Recommendation)**
- URL: https://www.w3.org/TR/json-ld11/
- The serialisation format used by EPCIS 2.0 for event data. Enables linked data representations that connect food traceability records to external knowledge graphs (GS1 Web Vocabulary, schema.org) for semantic interoperability.

**RFC 7519 — JSON Web Tokens (JWT)**
- URL: https://datatracker.ietf.org/doc/html/rfc7519
- Standard for compact, URL-safe token representation. Used for authentication tokens in REST API integrations between traceability platforms, supplier systems, and ERP/WMS integrations.

**RFC 6749 — OAuth 2.0 Authorization Framework**
- URL: https://datatracker.ietf.org/doc/html/rfc6749
- De-facto standard for delegated API access. Required for secure third-party integrations (ERP, retailer systems, government portals) in any food traceability platform.

---

### Data Model & API Specifications

**OpenAPI 3.1**
- URL: https://spec.openapis.org/oas/v3.1.0
- The GS1 EPCIS 2.0 REST API is specified in OpenAPI 3.1. Any food traceability platform exposing a REST API should provide an OpenAPI specification for developer tooling, SDK generation, and partner integration.

**GS1 Web Vocabulary**
- URL: https://www.gs1.org/voc/
- A shared vocabulary for describing GS1 identifiers and product attributes using linked data principles (JSON-LD, RDFa). Extends schema.org with food-specific attributes (batch/lot, best-before, net content, allergens). Enables semantic interoperability between traceability platforms.

**Schema.org Product / FoodEstablishment**
- URL: https://schema.org/Product and https://schema.org/FoodEstablishment
- W3C community vocabulary for structured product metadata. Combined with GS1 and UNECE vocabularies in JSON-LD contexts for enhanced food product descriptions. Relevant for consumer-facing product information pages linked via GS1 Digital Link QR codes.

**GDST 1.0 — Global Dialogue on Seafood Traceability**
- URL: https://thegdst.org/
- Developer Docs: https://developer.thegdst.org/article/9a95s5t81p-communication-protocol-supplementary-guide
- GitHub: https://github.com/gdst
- Industry standard built as an extension of GS1 EPCIS 2.0, specific to wild-caught and aquaculture supply chains. Defines seafood-specific KDEs (vessel ID, fishing area, species, catch method) and interoperability requirements. Reference implementation for how EPCIS can be domain-extended for specific commodity sectors.

---

### Security & Authentication Standards

**OAuth 2.0 / OpenID Connect**
- OAuth 2.0: https://datatracker.ietf.org/doc/html/rfc6749
- OIDC: https://openid.net/connect/
- Standard protocols for secure delegated access and identity federation. Required for enterprise integrations with retailer portals, government food safety systems, and ERP/WMS platforms.

**OWASP API Security Top 10**
- URL: https://owasp.org/www-project-api-security/
- Reference for securing REST APIs handling sensitive food supply chain data. Particularly relevant given regulatory audit requirements and the sensitivity of recall-related data.

**NIST Cybersecurity Framework**
- URL: https://www.nist.gov/cyberframework
- Applicable when food traceability data includes critical infrastructure operators (large food producers, distributors). Aligns with FDA's increasing focus on digital supply chain security.

---

## Similar Products — Developer Documentation & APIs

### GS1 EPCIS 2.0 (Reference Implementation)
- **Description:** The GS1 standard REST API for supply chain event data capture and query. All major food traceability platforms either implement EPCIS natively or provide EPCIS export. This is the canonical interoperability layer for the industry.
- **API Documentation:** https://ref.gs1.org/standards/epcis/artefacts
- **OpenAPI Spec:** https://ref.gs1.org/standards/epcis/openapi.json
- **Interactive Docs:** https://editor.swagger.io/?url=https%3A%2F%2Fref.gs1.org%2Fstandards%2Fepcis%2Fopenapi.json
- **Standards:** REST/JSON-LD, OpenAPI 3.1, ISO/IEC 19987
- **Authentication:** Implementation-dependent; OAuth 2.0 recommended

### OpenEPCIS (Open Source)
- **Description:** A fully open-source, GS1-compliant implementation of the EPCIS 2.0 standard. Production-ready modular libraries for EPCIS event capture, format conversion (XML ↔ JSON-LD), test data generation, and identifier translation.
- **API Documentation:** https://openepcis.io/docs/
- **Swagger UI:** https://tools.openepcis.io/q/swagger-ui/
- **SDKs/Libraries:** Java (primary); available via Maven
- **GitHub Organisation:** https://github.com/openepcis/
- **Community Edition Repo:** https://github.com/openepcis/epcis-repository-ce
- **Standards:** GS1 EPCIS 2.0, REST/JSON-LD
- **Authentication:** Standard HTTP auth; configurable per deployment
- **Licence:** Apache 2.0

### Wholechain
- **Description:** Blockchain-anchored supply chain traceability platform aligned with GS1 and GDST standards. Targets food, seafood, and agricultural supply chains. Provides open API access and integrations with ERPs, WMS, and QR code printing systems.
- **API Documentation:** https://developers.wholechain.com/GettingStarted/Introduction/
- **Support Docs:** https://support.wholechain.com/article/327-wholechain-api-documentation
- **Integrations Page:** https://wholechain.com/integrations
- **Standards:** GS1 EPCIS, GDST 1.0, REST
- **Authentication:** API key / OAuth

### Trustwell FoodLogiQ
- **Description:** FSMA 204-compliant supply chain traceability, supplier management, quality management, and recall platform. REST API available for integration with ERP and WMS systems. API tokens are role-scoped for enterprise security.
- **API Access:** Available via FoodLogiQ Connect platform Resource Center (login required)
- **Product Page:** https://www.trustwell.com/products/foodlogiq/
- **Standards:** REST/JSON, GS1-aligned KDE/CTE structures, FSMA 204
- **Authentication:** API token (role-scoped), generated in Administration area

### SafetyChain
- **Description:** Plant-floor food safety and quality management platform with real-time data collection from IoT devices, scales, and sensors. Provides REST APIs for extracting record data and for supplier onboarding workflows.
- **API Documentation:** https://developers.safetychain.com/
- **Product Page:** https://safetychain.com/
- **SDKs/Libraries:** REST (language-agnostic)
- **Standards:** REST/JSON; integrates with ERP, WMS, LIMS, MES systems
- **Authentication:** API key / Bearer token

### Intelex (EHSQ Platform)
- **Description:** Environmental, health, safety, and quality management platform used in food manufacturing for audit management, incident tracking, and corrective actions. REST API with resource-oriented URLs and standard HTTP verbs.
- **API Documentation:** https://developers.intelex.com/
- **Product Page:** https://www.intelex.com/products/applications/api
- **Standards:** REST/JSON, OpenAPI
- **Authentication:** HTTP Basic / OAuth 2.0

### IBM Food Trust (Supply Chain Intelligence Suite)
- **Description:** Blockchain-based (Hyperledger Fabric) farm-to-fork traceability platform used by Walmart, Nestlé, Unilever, and others. APIs support uploading supply chain events, transactions, master data, and certificate data from ERP systems.
- **Product Page:** https://www.ibm.com/products/supply-chain-intelligence-suite/food-trust
- **Developer Zone:** Available via IBM Food Trust platform (account required)
- **GitHub (Hyperledger Sample):** https://github.com/IBM/PublicRegulationFabric-Food-IBPV20
- **Standards:** Hyperledger Fabric, REST, GS1-aligned data model
- **Authentication:** IBM Cloud IAM / API key

### rfxcel / Antares Vision Group
- **Description:** Full-stack serialisation and traceability platform supporting multi-format data exchange with ERP/WMS/regulatory systems. Supports GS1 EPCIS, EDI, XML, CSV, AS2, SFTP, HTTPS. Primarily pharmaceutical, with growing food applications.
- **Product Page:** https://rfxcel.com/
- **User Guide:** https://help.rfxcel.net/rfxcel-user-guide/5.8.30/
- **Standards:** GS1 EPCIS, GS1 DPMS, EDI (ASN 856), XML, HL7, SAP IDoc; AS2, FTP, SFTP, HTTPS
- **Authentication:** SSL/HTTPS with user credentials; web service API

### GS1 US Data Hub API
- **Description:** GS1 US developer portal for managing product master data (GTIN registration, product attributes) via REST API. Relevant for platforms that need to validate or look up GS1 product identifiers.
- **API Developer Guide:** https://documents.gs1us.org/adobe/assets/deliver/urn:aaid:aem:b91e282f-2d95-4e37-b9db-05e31cd263bc/gs1-us-data-hub-api-developer-portal-user-guide.pdf
- **MyProduct API Guide:** https://documents.gs1us.org/adobe/assets/deliver/urn:aaid:aem:0c8fec6a-377b-4bcd-9ba3-14baaabe8609/gs1-us-data-hub-myproduct-create-manage-api-user-guide.pdf
- **Standards:** REST, GS1 identifiers
- **Authentication:** OAuth 2.0

---

## Notes

**Evolving standards landscape:** The food traceability standards environment is maturing rapidly in response to FSMA 204 (US, compliance by July 2028) and EU General Food Law digitisation pressure. GS1 EPCIS 2.0, GS1 Digital Link, and W3C Verifiable Credentials are converging into a coherent interoperability stack, but widespread cross-platform interoperability is not yet a reality — most deployments remain siloed.

**GDST as a model:** The GDST 1.0 standard demonstrates how EPCIS 2.0 can be extended with sector-specific KDEs. This pattern is likely to be replicated for other commodity sectors (fresh produce, dairy, meat), and an AI-native platform should be designed to accommodate custom EPCIS extensions.

**IoT integration gap:** While IoT sensor data (temperature, humidity, GPS) is commercially important for cold-chain compliance, there is no universally adopted standard for ingesting IoT events into EPCIS repositories. This is an underserved area where a platform could define a clear integration pattern.

**Blockchain maturity:** Hyperledger Fabric (IBM Food Trust) and Ethereum-derived approaches (Wholechain) are the dominant blockchain substrates, but blockchain adoption remains limited to large enterprise deployments. Lighter-weight append-only data integrity approaches (cryptographic hashing, W3C VCs) may offer better cost/benefit for mid-market users.

**Open-source gap:** OpenEPCIS (Apache 2.0) is the only mature open-source EPCIS 2.0 implementation. There is no open-source, AI-native food safety traceability platform combining EPCIS compliance, FSMA 204 workflows, HACCP documentation, and intelligent anomaly detection — representing the primary opportunity for this candidate project.
