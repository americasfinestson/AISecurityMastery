# AI Security Mastery: Interactive Portfolio (July 2026 – August 2027)

**Mission:** Develop a comprehensive, interactive AI security portfolio deployed live on `josh-whipkey.com`. This curriculum translates theoretical GenAI vulnerabilities (OWASP LLM Top 10) into hands-on React/AWS CDK implementations, satisfying 80+ CISSP Group A CPEs.

**Tech Stack:** 
* **Front End**: Typescript React styled with Cloudscape, hosted on Route 53
* **Infrastructure**: Typescript CDK
* **Back End**: API Gateway + Lambda, using a variety of other services as peripherals (e.g. Secrets Manager). Object storage in S3,and database services in DynamoDB and OpenSearch.

Note: When I began this security AI journey, I already had my own personal website running at josh-whipkey.com.
---

## Phase 1: Runtime Defenses & Prompt Integrity (July 2026 – October 2026)
**Focus:** Understanding fundamental LLM vulnerabilities, specifically direct/indirect prompt injection, output handling, and system prompt leakage.
**CISSP Domain:** Software Development Security
**Estimated CPEs:** 20

### The Deliverable: The "Prompt Hijack" Sandbox
Create a new route (`/projects/llm-sandbox`) on your site. Build an interactive UI where users are challenged to extract a "secret flag" hidden in the system prompt or bypass a classification filter. 
* **Backend:** CDK-deployed API Gateway -> Lambda -> Bedrock (Claude or Titan).
* **Security Control:** Implement an inline prompt validator (regex or a smaller secondary LLM) that intercepts and scrubs malicious inputs before they hit the primary model.

### Study Path & Resources
* **Read:** [OWASP Top 10 for LLMs (LLM01 & LLM02)](https://genai.owasp.org/llm-top-10/)
* **Read:** [Anthropic: Mitigating Jailbreaks and Prompt Injections](https://docs.anthropic.com/en/docs/mitigating-jailbreaks)
* **Read:** [AWS Prescriptive Guidance: Securing GenAI](https://docs.aws.amazon.com/prescriptive-guidance/latest/strategy-generative-ai-security/welcome.html)
* **Watch:** [AWS re:Invent: Securing Generative AI Applications (SEC315)](https://www.youtube.com/watch?v=7M7Fq8h_gE4)

---

## Phase 2: RAG Architecture & Data Perimeters (November 2026 – February 2027)
**Focus:** Securing Retrieval-Augmented Generation (RAG) pipelines, managing vector database access controls, and preventing sensitive data disclosure.
**CISSP Domain:** Security Architecture and Engineering & Identity & Access Management
**Estimated CPEs:** 20

### The Deliverable: Secure Document Q&A
Create a route (`/projects/secure-rag`) featuring a document chatbot. 
* **Backend:** Implement Amazon Bedrock Knowledge Bases backed by OpenSearch Serverless or a vector-enabled Postgres RDS.
* **Security Control:** Use Amazon Cognito (or your existing auth provider) to pass user-context tokens to the backend. Enforce row-level security or strict index filtering in the vector DB so the LLM can only retrieve documents the authenticated user is authorized to see. Demonstrate multi-tenant data isolation.

### Study Path & Resources
* **Read:** [OWASP LLM06: Sensitive Information Disclosure](https://genai.owasp.org/llm-top-10/)
* **Read:** [AWS Bedrock Knowledge Bases Security](https://docs.aws.amazon.com/bedrock/latest/userguide/kb-security.html)
* **Read:** [Pinecone: Vector Database Security Best Practices](https://www.pinecone.io/learn/vector-database-security/)
* **Watch:** [Google Cloud: Securing your AI data pipelines](https://www.youtube.com/watch?v=F_fD0N_5_Zg)

---

## Phase 3: AI Observability, Guardrails & Governance (March 2027 – May 2027)
**Focus:** Monitoring model behavior, detecting toxicity/PII in real-time, and aligning with risk management frameworks.
**CISSP Domain:** Security Operations and Security & Risk Management
**Estimated CPEs:** 20

### The Deliverable: Real-Time AI Audit Dashboard
Create a route (`/projects/ai-observability`) that visualizes the telemetry from Phases 1 and 2.
* **Backend:** Use CDK to configure CloudWatch Logs, EventBridge, and AWS Bedrock Guardrails.
* **Security Control:** Implement a Bedrock Guardrail to detect and mask PII (e.g., SSNs, credit cards) in user inputs. Build a React dashboard that polls CloudWatch metrics to display real-time stats on "Blocked Prompts," "PII Masking Events," and "Average Latency."

### Study Path & Resources
* **Read:** [NIST AI Risk Management Framework (AI RMF)](https://www.nist.gov/itl/ai-risk-management-framework)
* **Read:** [Amazon Bedrock Guardrails Documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails.html)
* **Read:** [OWASP LLM09: Overreliance](https://genai.owasp.org/llm-top-10/)
* **Watch:** [AWS re:Invent: Build responsible AI apps with Guardrails for Amazon Bedrock](https://www.youtube.com/watch?v=8XQG9M1l2_c)

---

## Phase 4: Agentic Orchestration & Least Privilege (June 2027 – August 2027)
**Focus:** Securing autonomous multi-agent environments, function calling/tool use, and API delegation.
**CISSP Domain:** Security Architecture & Network/Comm Security
**Estimated CPEs:** 20

### The Deliverable: The "Sandboxed Agent"
Create a route (`/projects/agent-executor`) where users can ask an AI agent to perform basic infrastructure lookups (e.g., "What is the current weather?" or "List the top 3 HackerNews articles").
* **Backend:** Implement a custom tool-calling loop using Claude 3 via Bedrock, utilizing the Model Context Protocol (MCP) or standard OpenAPI schemas.
* **Security Control:** The focus here is strictly on IAM and network boundaries. Define ultra-restrictive CDK IAM execution roles for the Lambda running the agent. Prove that even if the agent is compromised via indirect prompt injection (e.g., reading a malicious headline), its blast radius is completely contained by the AWS permissions boundary.

### Study Path & Resources
* **Read:** [Anthropic: Tool Use & Function Calling](https://docs.anthropic.com/en/docs/tool-use)
* **Read:** [Model Context Protocol (MCP) Specification](https://modelcontextprotocol.io/)
* **Read:** [OWASP LLM08: Excessive Agency](https://genai.owasp.org/llm-top-10/)
* **Watch:** [Black Hat: LLM Agents and the Rise of AI-Driven Exploits](https://www.youtube.com/watch?v=4b3iW4s2FGo) (Placeholder search recommendation for latest BlackHat/DefCon talks on Agent Security)