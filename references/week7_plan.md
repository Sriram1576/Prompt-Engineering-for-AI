# Week 7 Content Processing Plan: Specialized Domains (Healthcare, Finance, Legal)

## 1. Overview
This plan outlines the steps required to process the Week 7 knowledge base files—`healthcare_prompting.md`, `finance_prompting.md`, and `legal_prompting.md`. The objective is to transform these foundational documents into actionable learning modules, robust prompt templates, and integrated capabilities for the **Prompt Engineer Pro** skill.

## 2. Domain Objectives & Core Themes
Before executing the plan, the team must understand the unique constraints and requirements for each sector:

### Healthcare Prompting
*   **Core Focus:** Mastering medical terminology (e.g., anatomy, ICD-10), acronyms, and patient-friendly content generation.
*   **Key Applications:** Summarizing patient records, assisting in diagnosis, and creating educational materials.
*   **Critical Constraints:** Strict adherence to HIPAA compliance, patient privacy, and ethical boundaries in medical AI applications.

### Finance Prompting
*   **Core Focus:** Utilizing financial jargon, reporting standards, and market analysis techniques.
*   **Key Applications:** Trend prediction, financial report generation, and conceptual fraud detection.
*   **Critical Constraints:** Regulatory compliance (e.g., SEC guidelines), accuracy, and financial risk management.

### Legal Prompting
*   **Core Focus:** Precision in legal terminology ("legalese"), navigating case law, and accurate interpretation.
*   **Key Applications:** Summarizing complex legal documents, legal research assistance, and drafting contract clauses.
*   **Critical Constraints:** Upholding attorney-client privilege, confidentiality, and understanding the liability of AI-assisted legal work.

---

## 3. Actionable Steps for the Team

### Phase 1: Content Extraction & Template Design (Prompt Engineers)
*   **Action 1:** Extract standard definitions, constraints, and best practices from the Week 7 documentation.
*   **Action 2:** Develop 3-5 foundational prompt templates for each domain using standard frameworks (e.g., RACE, RTF).
    *   *Healthcare Example:* A prompt template for patient record summarization that assumes all PII (Personally Identifiable Information) has been redacted prior to input.
    *   *Finance Example:* A template for market trend analysis that references specific reporting standards.
    *   *Legal Example:* A prompt for drafting a legal clause that includes necessary caveats regarding professional legal review.

### Phase 2: Knowledge Base Integration (Development Team)
*   **Action 1:** Ensure `healthcare_prompting.md`, `finance_prompting.md`, and `legal_prompting.md` are properly indexed by the skill's natural language reasoning system.
*   **Action 2:** Implement guardrails in the system prompt to automatically trigger compliance checks (HIPAA, SEC, Legal Confidentiality) when a user request falls into one of these three domains.

### Phase 3: Stress Testing & Refinement (AI Testers)
*   **Action 1:** Run simulated user prompts across all three domains to evaluate the AI's ability to pull from the correct Week 7 documents.
*   **Action 2:** Conduct "red-teaming" tests focused on constraints:
    *   Attempt to bypass healthcare privacy filters.
    *   Test for hallucinations in financial trend predictions.
    *   Check if the AI correctly applies legal caveats rather than offering definitive legal advice.
*   **Action 3:** Document failure points and iterate on the prompt templates and knowledge base structure.

### Phase 4: Final Review & Publishing (Project Leads)
*   **Action 1:** Review the test results and finalize the domain-specific prompt templates.
*   **Action 2:** Publish a summary guide or "cheat sheet" for users on how to best interact with the Prompt Engineer Pro skill for specialized domains.

---

## 4. Timeline & Milestones
*   **Day 1-2:** Complete Phase 1 (Content Extraction & Template Design).
*   **Day 3:** Complete Phase 2 (Knowledge Base Integration).
*   **Day 4-5:** Complete Phase 3 (Stress Testing & Refinement).
*   **Day 6:** Complete Phase 4 (Final Review & Publishing).
