# AISecurityMastery
Production-grade blueprints, threat models, and hands-on labs for security enterprise GenAI, RAG pipelines, and autonomous agents on AWS and GCP.

# AI Security Mastery Playbook (July 2026 – August 2027)

* **Timeframe:** July 2026 – August 2027 (60 Weeks Total)  
* **Commitment:** 3 Hours/Week (1.5 Hours Study/Watch, 1.5 Hours Lab/Deliverable)  
* **Target:** ~60–90 CISSP Group A CPEs (Mapped directly to Domains)

---

## Phase 1: Foundations & Core Vulnerabilities (Weeks 1–12)
*Focus: Primers on LLM architectures, threat modeling frameworks, and the core OWASP top 10 flaws.*

### Week 1 (July 13, 2026): GenAI Foundations & Security Taxonomy
*   **Study (1.5 hrs):** NIST AI 100-1 (Artificial Intelligence Taxonomy) & OWASP LLM Core Principles.
*   **Lab (1.5 hrs):** Deploy a basic Amazon Bedrock / Vertex AI text generation pipeline via CLI/SDK; inspect raw JSON payload schemas.
*   **Deliverable:** API architecture topology mapping data entry and exit points.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 2 (July 20, 2026): Transformer Architectures & Data Touchpoints
*   **Study (1.5 hrs):** Deep dive into Attention mechanisms, tokenization steps, and where weights/biases reside inside an active runtime pipeline.
*   **Lab (1.5 hrs):** Build a local script to tokenize inputs, inspect attention maps, and log contextual window allocations.
*   **Deliverable:** Token-to-byte boundaries data flow diagram.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 3 (July 27, 2026): Advanced Threat Modeling for AI (STRIDE & PASTA)
*   **Study (1.5 hrs):** OWASP LLM Threat Modeling Guide & Microsoft's Bug Bar for AI Systems.
*   **Lab (1.5 hrs):** Deconstruct a standard enterprise chatbot design using a STRIDE matrix.
*   **Deliverable:** STRIDE threat matrix mapping out trust boundaries.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 4 (August 3, 2026): OWASP LLM01: Prompt Injection (Direct & Indirect)
*   **Study (1.5 hrs):** Review documented real-world indirect prompt injection attack vectors via external data sources.
*   **Lab (1.5 hrs):** Set up an isolated python model call; craft an adversarial system instructions bypass payload.
*   **Deliverable:** Working injection payload code proof and documentation of impact.
*   **Domain / CPE:** Domain 4 (Network/Comm Security) // 3 CPEs

### Week 5 (August 10, 2026): OWASP LLM02 & LLM06: Insecure Output Handling & Sensitive Data Disclosure
*   **Study (1.5 hrs):** Read cross-site scripting (XSS) and privilege escalation vectors resulting from raw LLM output execution.
*   **Lab (1.5 hrs):** Simulate a scenario where an LLM returns a hidden command payload that executes in a mock downstream application.
*   **Deliverable:** Remediation document tracking output validation rules.
*   **Domain / CPE:** Domain 8 (Software Development Security) // 3 CPEs

### Week 6 (August 17, 2026): OWASP LLM03 & LLM05: Training Data Poisoning & Supply Chain Risks
*   **Study (1.5 hrs):** Analyze base model vulnerabilities, fine-tuning compromises, and third-party plugin/model verification steps.
*   **Lab (1.5 hrs):** Evaluate a mock Hugging Face model lineage using verification hashes and scan for serialized code execution exploits (e.g., pickle exploits).
*   **Deliverable:** Third-party AI supply chain validation checklist.
*   **Domain / CPE:** Domain 8 (Software Development Security) // 3 CPEs

### Week 7 (August 24, 2026): OWASP LLM07 & LLM09: Insecure Plugin Design & Overreliance
*   **Study (1.5 hrs):** Read on vulnerabilities where an LLM agent blindly trusts untrusted client instructions to perform actions.
*   **Lab (1.5 hrs):** Build an application function tool calling script; exploit it by feeding it inputs that bypass localized verification checks.
*   **Deliverable:** API schema enforcement plan for tools.
*   **Domain / CPE:** Domain 8 (Software Development Security) // 3 CPEs

### Week 8 (August 31, 2026): OWASP LLM04, LLM08, & LLM10: Model Denial of Service, Agency, & Theft
*   **Study (1.5 hrs):** Explore resource exhaustion via long padding context attacks and methods used to reverse engineer or extract model weights.
*   **Lab (1.5 hrs):** Execute an intensive context-window inflation test script to monitor token consumption rates and service timeouts.
*   **Deliverable:** Rate limiting and token bounding configuration policy.
*   **Domain / CPE:** Domain 4 (Network/Comm Security) // 3 CPEs

### Week 9 (September 7, 2026): Foundational AWS Bedrock Platform Security
*   **Study (1.5 hrs):** AWS Bedrock Security documentation, concentrating on data encryption, VPC endpoints, and the absolute isolation of inference data.
*   **Lab (1.5 hrs):** Deploy a Bedrock model invocation backend wrapped inside a secure AWS VPC using private VPC endpoints.
*   **Deliverable:** CloudFormation or Terraform snippet demonstrating network isolation.
*   **Domain / CPE:** Domain 4 (Network/Comm Security) // 3 CPEs

### Week 10 (September 14, 2026): Foundational Google Vertex AI Platform Security
*   **Study (1.5 hrs):** Google Cloud Vertex AI Security Architecture guidelines, focusing on Service Perimeters (VPC Service Controls).
*   **Lab (1.5 hrs):** Construct a basic Vertex AI pipeline secured by explicit IAM roles and context-aware access constraints.
*   **Deliverable:** IAM access policy blueprint for model fine-tuning endpoints.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 11 (September 21, 2026): Multi-Tenant Data Perimeters for Core AI Platforms
*   **Study (1.5 hrs):** Read strategies for establishing tenant-level data boundaries within shared inference infrastructure.
*   **Lab (1.5 hrs):** Configure a cross-account IAM policy matrix ensuring tenant A cannot hit tenant B's fine-tuned model endpoints.
*   **Deliverable:** Reference architecture pattern for tenant compute isolation.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 12 (September 28, 2026): Phase 1 Capstone – Comprehensive Threat Model
*   **Study (1.5 hrs):** Synthesize all Phase 1 concepts to evaluate a standard corporate multi-cloud AI design blueprint.
*   **Lab (1.5 hrs):** Complete an end-to-end threat assessment portfolio covering every vector from ingestion to output consumption.
*   **Deliverable:** A comprehensive 5-page threat modeling assessment artifact.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

---

## Phase 2: Cloud AI Infrastructure & Controls (Weeks 13–24)
*Focus: Deep architectural implementations on AWS and Google Cloud, covering perimeters, guardrails, and secure data pipelines.*

### Week 13 (October 5, 2026): Deep Dive: AWS Bedrock Guardrails Architecture
*   **Study (1.5 hrs):** AWS Documentation on Guardrails for Bedrock, focusing on regular expressions, PII masking, and toxicity filtering performance overhead.
*   **Lab (1.5 hrs):** Configure a strict Bedrock Guardrail policy that detects and masks common PII strings (SSNs, API keys) during prompt ingestion.
*   **Deliverable:** Verified Guardrail policy configuration file.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 14 (October 12, 2026): Deep Dive: GCP Vertex AI Safety Settings
*   **Study (1.5 hrs):** Google Vertex AI Safety Attributes and structural configuration knobs across model categories.
*   **Lab (1.5 hrs):** Implement programmatic Vertex AI safety threshold configs via python and track response blocking events under adversarial pressure.
*   **Deliverable:** Safety blocking metrics assessment report.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 15 (October 19, 2026): Securing Retrieval-Augmented Generation (RAG) Architecture
*   **Study (1.5 hrs):** Read about vector injection vectors and document access permission tracking models within RAG architectures.
*   **Lab (1.5 hrs):** Set up an Amazon Bedrock Knowledge Base connected to a locked-down S3 data source, focusing on preserving metadata visibility limits.
*   **Deliverable:** Secure RAG data flow diagram showing access check points.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 16 (October 26, 2026): Vector Database Security (Pinecone, pgvector, OpenSearch)
*   **Study (1.5 hrs):** Investigate network-layer protection, data encryption at rest/in transit, and row-level security for vector tables.
*   **Lab (1.5 hrs):** Deploy an OpenSearch or PostgreSQL vector storage node with explicit row-level access controls enabled.
*   **Deliverable:** SQL DDL / configuration schema showing active access filters.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 17 (November 2, 2026): Advanced IAM for AI Pipelines (AWS Roles / Google Service Accounts)
*   **Study (1.5 hrs):** Principles of least privilege specifically applied to short-lived token handshakes for inference jobs.
*   **Lab (1.5 hrs):** Build an AWS IAM role structure utilizing session policies to dynamically downgrade model access privileges at run time.
*   **Deliverable:** IAM assume-role execution policy template.
*   **Domain / CPE:** Domain 5 (Identity & Access Management) // 3 CPEs

### Week 18 (November 9, 2026): AI Logging, Auditing, and SIEM Integration
*   **Study (1.5 hrs):** Logging patterns for CloudTrail/CloudWatch and GCP Cloud Logging, capturing entire prompt/response transactions safely without logging PII.
*   **Lab (1.5 hrs):** Route Bedrock invocation logs to a secure S3 bucket with Object Lock enabled; build an alert pattern for high-frequency toxicity hits.
*   **Deliverable:** Log pipeline schematic and alerting rule file.
*   **Domain / CPE:** Domain 7 (Security Operations) // 3 CPEs

### Week 19 (November 16, 2026): Cross-Cloud AI Architecture Comparison
*   **Study (1.5 hrs):** Comparative structural analysis of Bedrock’s managed endpoint approach versus Vertex AI’s customized runtime setups.
*   **Lab (1.5 hrs):** Map identical security baseline requirements across an equivalent deployment on both clouds.
*   **Deliverable:** Cross-cloud technical control translation matrix.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 20 (November 23, 2026): Introduction to AI Red Teaming Frameworks
*   **Study (1.5 hrs):** Review the guidelines in the Microsoft AI Red Team documentation and the building blocks of the MITRE ATLAS matrix.
*   **Lab (1.5 hrs):** Outline an operational red team engagement plan focused on exposing data leak vectors in an internal enterprise tool.
*   **Deliverable:** Drafted AI Red Team scoping document.
*   **Domain / CPE:** Domain 6 (Security Assessment/Testing) // 3 CPEs

### Week 21 (November 30, 2026): Executing Adversarial Prompt Engineering Attacks
*   **Study (1.5 hrs):** Research advanced jailbreaking logic (e.g., token smuggling, multi-language obfuscation techniques).
*   **Lab (1.5 hrs):** Conduct safe execution testing of complex jailbreak templates against an isolated sandbox model to gauge structural baseline resistance.
*   **Deliverable:** Attack string behavior and mitigation log.
*   **Domain / CPE:** Domain 6 (Security Assessment/Testing) // 3 CPEs

### Week 22 (December 7, 2026): Model Inversion and Extraction Testing
*   **Study (1.5 hrs):** Read current academic research explaining how repeated systemic queries can reconstruct proprietary training instances or model parameters.
*   **Lab (1.5 hrs):** Write a python automation loop designed to spot information disclosure anomalies via high-frequency subtle variations in prompt structure.
*   **Deliverable:** Anomaly threshold report for API traffic limits.
*   **Domain / CPE:** Domain 6 (Security Assessment/Testing) // 3 CPEs

### Week 23 (December 14, 2026): Continuous Evasion Defense Design
*   **Study (1.5 hrs):** Structural techniques for building an intermediate defensive layer that analyzes and cleans incoming embeddings before they reach a model.
*   **Lab (1.5 hrs):** Build an inline input pre-filtering script that intercept and rejects anomalous data payloads.
*   **Deliverable:** Source code for the pre-inference verification script.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 24 (December 21, 2026): Phase 2 Capstone – Secured Infrastructure Blueprint
*   **Study (1.5 hrs):** Pull together all Phase 2 cloud structural controls into a cohesive architectural model.
*   **Lab (1.5 hrs):** Construct a highly secure enterprise RAG platform template using infrastructure-as-code principles.
*   **Deliverable:** Production-ready IaC infrastructure template with documented network and identity controls.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

---

## Phase 3: Governance, Risk, & Compliance (Weeks 25–36)
*Focus: Implementing governance standards, mapping compliance frameworks, and practicing secure code delivery.*

### Week 25 (December 28, 2026): Implementing the NIST AI Risk Management Framework (RMF)
*   **Study (1.5 hrs):** NIST AI RMF 1.0 core functions: Govern, Map, Measure, and Manage.
*   **Lab (1.5 hrs):** Translate the "Govern" requirements into concrete technical infrastructure checking procedures for a development organization.
*   **Deliverable:** Organizational AI Risk Assessment spreadsheet.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 26 (January 4, 2027): ISO/IEC 42001 Standard Deep Dive
*   **Study (1.5 hrs):** Review the ISO/IEC 42001 requirements for establishing, maintaining, and improving an Artificial Intelligence Management System (AIMS).
*   **Lab (1.5 hrs):** Conduct a gap analysis of an AI deployment scenario against ISO 42001 Annex A objectives.
*   **Deliverable:** ISO 42001 baseline gap statement.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 27 (January 11, 2027): Operationalizing AI Governance & Inventory Controls
*   **Study (1.5 hrs):** Mechanisms for accurately identifying, tracking, and cataloging every active internal model deployment, API endpoint, and customized fine-tuning run.
*   **Lab (1.5 hrs):** Build an automated inventory asset schema explicitly engineered to capture core AI metrics (base model version, training lineage, classification limits).
*   **Deliverable:** Enterprise AI Asset Catalog Schema template.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 28 (January 18, 2027): Secure SDLC Extensions for AI Engineering
*   **Study (1.5 hrs):** Adapting traditional continuous integration pipelines to incorporate automated checks for model weight validation and adversarial evaluations.
*   **Lab (1.5 hrs):** Setup a mock GitHub Actions validation runner that checks model fine-tuning dataset hashes for tampering before deployment.
*   **Deliverable:** CI/CD pipeline configuration code block.
*   **Domain / CPE:** Domain 8 (Software Development Security) // 3 CPEs

### Week 29 (January 25, 2027): Enterprise Security Policy for AI Coding Assistants
*   **Study (1.5 hrs):** Review data retention choices, corporate IP leakage vectors, and contextual scanning vulnerabilities in tools like GitHub Copilot or Amazon Q.
*   **Lab (1.5 hrs):** Draft a practical corporate usage standard defining explicit code boundaries, allowed data parameters, and code review criteria.
*   **Deliverable:** Completed Corporate AI Coding Assistant Policy.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 30 (February 1, 2027): Secrets Prevention & Detection in Prompt Contexts
*   **Study (1.5 hrs):** Analyzing risk maps where developers inadvertently pass live connection tokens, API credentials, or certificates into context paths.
*   **Lab (1.5 hrs):** Implement an automated regex-driven scanner pipeline that flags and drops user messages containing cryptographic shapes before they hit external services.
*   **Deliverable:** Scanning engine code module.
*   **Domain / CPE:** Domain 8 (Software Development Security) // 3 CPEs

### Week 31 (February 8, 2027): AI Supply Chain & Model Provenance (SBOMs for AI)
*   **Study (1.5 hrs):** Investigate emerging Software Bill of Materials (SBOM) expansions for AI, focusing on tracking foundational dataset layers and fine-tuning histories.
*   **Lab (1.5 hrs):** Document a comprehensive structural component bill of materials for an open-weights model platform.
*   **Deliverable:** Formatted AI Software Bill of Materials file.
*   **Domain / CPE:** Domain 8 (Software Development Security) // 3 CPEs

### Week 32 (February 15, 2027): Data Privacy Laws & Machine Learning Realities
*   **Study (1.5 hrs):** Explore tension points between corporate compliance mandates (GDPR/CCPA "Right to be Forgotten") and immutable model training parameters.
*   **Lab (1.5 hrs):** Outline a data ingestion pipeline architecture that maps out automated data scrubbing steps prior to any persistent storage ingestion.
*   **Deliverable:** Data minimization operational blueprint.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 33 (February 22, 2027): Explainability, Bias, and Audit Logging Architecture
*   **Study (1.5 hrs):** Examine the relationship between model interpretability constraints and regulatory verification paths.
*   **Lab (1.5 hrs):** Implement an engineering record-keeping pattern that logs system prompts, temperature values, and random seeds alongside basic output tracking.
*   **Deliverable:** Deterministic logging standard schema.
*   **Domain / CPE:** Domain 7 (Security Operations) // 3 CPEs

### Week 34 (March 1, 2027): Managing Third-Party AI Vendor Risk Assessments
*   **Study (1.5 hrs):** Review vendor evaluation strategies, focusing on zero-data retention clauses, liability profiles, and sub-processor evaluation procedures.
*   **Lab (1.5 hrs):** Create a tailored, highly specific AI SaaS vendor intake assessment template.
*   **Deliverable:** 20-question comprehensive Vendor Risk Assessment questionnaire.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 35 (March 8, 2027): Incident Response Runbooks for AI Exploits
*   **Study (1.5 hrs):** Discover strategies for recognizing, isolating, and containing active AI-specific security incidents (e.g., massive data exfiltration via prompt injection).
*   **Lab (1.5 hrs):** Create a systematic incident containment plan outlining immediate remediation protocols for compromised model endpoints.
*   **Deliverable:** Completed AI Security Incident Response Playbook.
*   **Domain / CPE:** Domain 7 (Security Operations) // 3 CPEs

### Week 36 (March 15, 2027): Phase 3 Capstone – Governance Blueprint & Audit Pack
*   **Study (1.5 hrs):** Assemble all regulatory and compliance artifacts generated during Phase 3.
*   **Lab (1.5 hrs):** Map your existing lab platforms directly to a unified dashboard showing alignment with NIST AI RMF and ISO 42001 frameworks.
*   **Deliverable:** Corporate AI Compliance Audit package document.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

---

## Phase 4: Advanced Agentic Security & Regulated Industries (Weeks 37–48)
*Focus: Securing autonomous multi-agent environments, Model Context Protocol integration, and highly regulated deployment frameworks.*

### Week 37 (March 22, 2027): The Model Context Protocol (MCP) Architecture & Vulnerability Map
*   **Study (1.5 hrs):** Analyze Anthropic's Model Context Protocol (MCP) design specification, highlighting potential client-server security vulnerabilities.
*   **Lab (1.5 hrs):** Build an isolated MCP server wrapper script featuring strict input schema enforcement constraints.
*   **Deliverable:** Hardened MCP server interface schema configuration.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 38 (March 29, 2027): OAuth & Token Delegation for Autonomous AI Agents
*   **Study (1.5 hrs):** Investigate methods for managing secure token authentication and runtime session limits when agents execute API mutations on behalf of human users.
*   **Lab (1.5 hrs):** Construct an OAuth delegation flow that down-scopes an agent's token visibility to specific sub-directories.
*   **Deliverable:** Architecture flow diagram showing token interception boundaries.
*   **Domain / CPE:** Domain 5 (Identity & Access Management) // 3 CPEs

### Week 39 (April 5, 2027): Multi-Agent Communication & System Trust Boundaries
*   **Study (1.5 hrs):** Explore emerging attack patterns in multi-agent environments where an exploitation of a secondary agent compromises a primary coordinator agent.
*   **Lab (1.5 hrs):** Simulate a two-agent scenario using a verification layer that screens data passing between the distinct agent runtime environments.
*   **Deliverable:** Micro-segmented agent communication schema pattern.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 40 (April 12, 2027): Sandbox Isolation for Autonomous Code Execution Engines
*   **Study (1.5 hrs):** Research secure hosting mechanics for dynamic runtimes, focusing on gVisor, Firecracker microVMs, and hardened Docker configurations.
*   **Lab (1.5 hrs):** Create a production-ready microVM or container configuration featuring hard limitations on network access, storage, and CPU lifetimes for running agent-generated code blocks.
*   **Deliverable:** Dockerfile / task definition deployment template.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 41 (April 19, 2027): AI Architecture in Highly Regulated Environments
*   **Study (1.5 hrs):** Review advanced security strategies, focusing on strict air-gapped network structures, completely offline base model configurations, and localized dependency tracking.
*   **Lab (1.5 hrs):** Design an end-to-end logical architecture map demonstrating how an offline enterprise AI solution operates without any public internet dependencies.
*   **Deliverable:** Detailed network topology document for an air-gapped AI deployment.
*   **Domain / CPE:** Domain 4 (Network/Comm Security) // 3 CPEs

### Week 42 (April 26, 2027): FedRAMP High/Moderate Baselines for GenAI Platforms
*   **Study (1.5 hrs):** Read the FedRAMP Joint Authorization Board (JAB) updates regarding the authorization of cloud-delivered generative AI capabilities.
*   **Lab (1.5 hrs):** Translate key FedRAMP access control (AC) and configuration management (CM) requirements into cloud-native control settings.
*   **Deliverable:** FedRAMP control response document snippet.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 43 (May 3, 2027): Advanced Enterprise Guardrails & Context-Aware Real-Time Defenses
*   **Study (1.5 hrs):** Explore how multi-stage classifier configurations can detect sub-string anomalies and semantic drifts in real time.
*   **Lab (1.5 hrs):** Build a high-performance validation proxy function that calculates real-time cosine similarity scores against a database of known exploit profiles.
*   **Deliverable:** Inline inspection proxy source file.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 44 (May 10, 2027): Executive Risk Communication & AI Threat Metrics
*   **Study (1.5 hrs):** Strategies for translating deeply technical AI vulnerabilities into high-level business risks (e.g., estimating financial impacts or quantifying legal liability risks).
*   **Lab (1.5 hrs):** Build an executive dashboard template that highlights crucial performance indicators like cost tracking, policy violation frequencies, and control effectiveness rates.
*   **Deliverable:** Executive briefing slide outline.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 45 (May 17, 2027): High-Throughput Stream Analysis & Pipeline Defenses
*   **Study (1.5 hrs):** Investigate security patterns designed to safely parse and analyze continuous streaming data feeds without adding system delays.
*   **Lab (1.5 hrs):** Set up an inline streaming consumer thread designed to scan, filter, and alert on system tokens on the fly.
*   **Deliverable:** High-performance log parser benchmark report.
*   **Domain / CPE:** Domain 7 (Security Operations) // 3 CPEs

### Week 46 (May 24, 2027): Hardening Open Weights Model Runtimes (vLLM / Ollama)
*   **Study (1.5 hrs):** Analyze the threat vectors of unmanaged hosting engines, focusing on API authentication holes and shared memory vulnerabilities.
*   **Lab (1.5 hrs):** Deploy an isolated instance of vLLM behind an NGINX reverse proxy featuring mutual TLS authentication controls.
*   **Deliverable:** Hardened reverse proxy configuration script.
*   **Domain / CPE:** Domain 4 (Network/Comm Security) // 3 CPEs

### Week 47 (May 31, 2027): Emerging Vulnerabilities & Advanced Cryptographic Protections
*   **Study (1.5 hrs):** Review academic papers covering Homomorphic Encryption and Secure Multi-Party Computation configurations within model pipelines.
*   **Lab (1.5 hrs):** Experiment with a basic Python cryptography library to mock out how datasets can remain encrypted throughout simple analysis workflows.
*   **Deliverable:** Cryptographic verification test code.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 48 (June 7, 2027): Phase 4 Capstone – Hardened Multi-Agent Architecture Blueprint
*   **Study (1.5 hrs):** Combine all autonomous agent security configurations, OAuth boundaries, and sandboxing designs into a comprehensive framework.
*   **Lab (1.5 hrs):** Construct an end-to-end system design specifying identity handshakes and data containment boundaries across a distributed multi-agent architecture.
*   **Deliverable:** An advanced 10-page Multi-Agent Architecture Blueprint.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

---

## Phase 5: Portfolio Finalization & Audit Readiness (Weeks 49–60)
*Focus: Assembling the final enterprise platform design blueprint, consolidating evidence for audit verification, and filling out the CPE ledger.*

### Week 49 (June 14, 2027): Portfolio Project Initialization: Base Architecture Definition
*   **Study (1.5 hrs):** Review all cloud platform templates and system diagrams created throughout the curriculum year.
*   **Lab (1.5 hrs):** Establish the base repository framework for your final portfolio showcase, integrating your cross-cloud infrastructure design assets.
*   **Deliverable:** Core architecture map and infrastructure outline.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 50 (June 21, 2027): Portfolio Enhancement: Deepening the Threat Modeling Suite
*   **Study (1.5 hrs):** Review structural threat patterns, focusing on edge cases like cascading agent loops and advanced prompt injection payloads.
*   **Lab (1.5 hrs):** Expand your threat modeling library into a comprehensive threat matrix that spans from ingestion layers down to analytical output consumption points.
*   **Deliverable:** Complete enterprise threat catalog.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 51 (June 28, 2027): Portfolio Enhancement: Hardening Identity & Perimeter Controls
*   **Study (1.5 hrs):** Identify and patch potential weaknesses in your IAM policies, focusing on eliminating wildcard entries and tightening short-lived token lifetimes.
*   **Lab (1.5 hrs):** Refine your cloud platform deployment templates to implement zero-trust access controls across all model access points.
*   **Deliverable:** Audited and verified IAM configuration codebase.
*   **Domain / CPE:** Domain 5 (Identity & Access Management) // 3 CPEs

### Week 52 (July 5, 2027): Portfolio Enhancement: Validating Compliance Dashboards
*   **Study (1.5 hrs):** Review control mapping practices for tracking structural controls against NIST AI RMF and ISO/IEC 42001 requirements.
*   **Lab (1.5 hrs):** Build an automated control tracking matrix linking your infrastructure components directly to specific regulatory requirements.
*   **Deliverable:** Complete, traceable compliance matrix artifact.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 53 (July 12, 2027): Portfolio Project Final Assembly & Technical Documentation
*   **Study (1.5 hrs):** Review strategies for clear technical writing, focusing on distilling complex cloud security steps into clean, readable implementation documentation.
*   **Lab (1.5 hrs):** Author the comprehensive master guide for your secure enterprise platform deployment blueprint.
*   **Deliverable:** Finalized system implementation documentation guide.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 54 (July 19, 2027): Advanced Cloud Security Research Review
*   **Study (1.5 hrs):** Read newly published cloud platform threat briefs, vulnerabilities, and vendor research notes from the past year.
*   **Lab (1.5 hrs):** Assess how these newly discovered threat behaviors affect your secure reference design blueprint.
*   **Deliverable:** Vulnerability assessment summary report.
*   **Domain / CPE:** Domain 6 (Security Assessment/Testing) // 3 CPEs

### Week 55 (July 26, 2027): Independent Code Security Auditing Practice
*   **Study (1.5 hrs):** Study code auditing methodologies for spot-checking python and infrastructure templates for hidden security issues.
*   **Lab (1.5 hrs):** Perform an end-to-end security review across all custom middleware scripts in your local laboratory repository.
*   **Deliverable:** Cleaned up source code repo and associated audit finding notes.
*   **Domain / CPE:** Domain 8 (Software Development Security) // 3 CPEs

### Week 56 (August 2, 2027): Simulating Security Operations Center (SOC) Alerts
*   **Study (1.5 hrs):** Review effective incident log patterns, focusing on distinguishing normal high-volume workflows from stealthy injection attacks.
*   **Lab (1.5 hrs):** Build simulated log streams that mimic data exfiltration behavior patterns to test the accuracy of your detection alerts.
*   **Deliverable:** Detection alert logic and validation logs.
*   **Domain / CPE:** Domain 7 (Security Operations) // 3 CPEs

### Week 57 (August 9, 2027): Exploring Evolving Industry Threat Trends
*   **Study (1.5 hrs):** Research the latest industry analysis papers regarding autonomous agent security risks and emerging model runtime threat models.
*   **Lab (1.5 hrs):** Draft a technology roadmap assessing the security impact of these upcoming tools on enterprise system architectures.
*   **Deliverable:** Strategic security technology forecast brief.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 58 (August 16, 2027): Comprehensive CISSP CPE Record Consolidation
*   **Study (1.5 hrs):** Review (ISC)² audit guidelines to ensure your activity logs are properly structured and ready for submission.
*   **Lab (1.5 hrs):** Pull together all your time tracking logs, architecture deliverables, and git commit history into a single, audit-ready verification package.
*   **Deliverable:** Audit-ready CPE ledger tracking artifact.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs

### Week 59 (August 23, 2027): Peer Technical Portfolio Verification Simulation
*   **Study (1.5 hrs):** Standardize your presentation assets, ensuring all architecture maps, threat catalogs, and data flow summaries are clear and well-structured.
*   **Lab (1.5 hrs):** Conduct a thorough walkthrough review of your complete repository suite to verify the documentation flow is seamless.
*   **Deliverable:** Completed technical portfolio presentation package.
*   **Domain / CPE:** Domain 3 (Security Architecture) // 3 CPEs

### Week 60 (August 30, 2027): Final Repository Validation & Program Sign-off
*   **Study (1.5 hrs):** Conduct a final sweep across your system repository to polish explanations, update references, and ensure all asset links work correctly.
*   **Lab (1.5 hrs):** Execute your automated code verification and linting tools one last time across the entire repository structure.
*   **Deliverable:** Completed, production-grade AI Security Mastery Repository.
*   **Domain / CPE:** Domain 1 (Security & Risk Management) // 3 CPEs
