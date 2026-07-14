# Week 7 Outline: Domain-Specific Prompt Engineering

This document outlines the logical structure and key components for the three Week 7 modules covering prompt engineering in specialized industries.

---

## 1. Healthcare Prompting

### Introduction
*   Overview of AI and Large Language Models (LLMs) in the healthcare sector.
*   The critical need for precision, empathy, and reliability in medical prompts.

### Key Challenges & Constraints
*   **Data Privacy & Compliance:** Navigating HIPAA, GDPR, and safeguarding Patient Health Information (PHI).
*   **The Hallucination Risk:** Why factual inaccuracy is uniquely dangerous in medicine.
*   **Ethical Considerations:** Maintaining the "human in the loop" and avoiding unauthorized medical advice.

### Core Prompting Techniques for Healthcare
*   **Persona Prompting:** Instructing the AI to act as a specialized medical professional or empathetic listener.
*   **Grounding & Context Injection:** Providing the model with specific, verified medical literature or patient history (anonymized) to base its answers on.
*   **Chain-of-Thought (CoT):** Encouraging step-by-step clinical reasoning.

### High-Impact Use Cases & Example Prompts
*   **Clinical Documentation:** Summarizing anonymized doctor-patient transcripts into standard SOAP notes.
*   **Medical Literature Review:** Extracting key findings from dense research papers.
*   **Patient Communication:** Translating complex medical jargon into plain, patient-friendly language.

### Best Practices for Safety
*   Implementing strict output constraints and fallback mechanisms.
*   Adding disclaimers (e.g., "This is not medical advice").

---

## 2. Finance Prompting

### Introduction
*   The role of Generative AI in the financial industry (banking, investment, accounting).
*   The emphasis on quantitative accuracy, speed, and strict regulatory adherence.

### Key Challenges & Constraints
*   **Regulatory Compliance:** Adhering to SEC guidelines, FINRA rules, and avoiding market manipulation.
*   **Data Security:** Protecting sensitive financial data and PII.
*   **Numerical Accuracy:** Mitigating the LLM weakness in pure mathematical computation.

### Core Prompting Techniques for Finance
*   **Data-Driven Prompting:** Formatting tabular data (CSV, JSON) for optimal LLM parsing and analysis.
*   **Few-Shot Prompting:** Providing examples of desired financial reports or formatting.
*   **Instructional Constraints:** Forcing the model to show its work or cite specific sections of a financial document.

### High-Impact Use Cases & Example Prompts
*   **Financial Statement Analysis:** Summarizing 10-K/10-Q reports and extracting key risk factors.
*   **Market Sentiment Analysis:** Analyzing news articles and earnings call transcripts for positive/negative indicators.
*   **Automated Reporting:** Generating routine financial summaries or compliance reports.

### Best Practices for Reliability
*   Using LLMs for text analysis and extraction while relying on specialized tools (e.g., Python scripts via agents) for calculations.
*   Ensuring auditability of AI-generated insights.

---

## 3. Legal Prompting

### Introduction
*   The transformation of legal practice through AI.
*   The balance between efficiency gains and the absolute necessity of accuracy.

### Key Challenges & Constraints
*   **Attorney-Client Privilege:** Ensuring confidentiality and data security when using third-party models.
*   **Fictitious Citations (Hallucinations):** The severe consequences of citing non-existent case law.
*   **Unauthorized Practice of Law (UPL):** Delineating between legal information generation and providing legal counsel.

### Core Prompting Techniques for Legal
*   **Retrieval-Augmented Generation (RAG):** Connecting the prompt to a closed database of verified case law and statutes.
*   **Strict Output Formatting:** Prompting the model to follow specific legal document templates (e.g., standard contract clauses).
*   **Negative Prompting:** Explicitly telling the model *not* to invent cases or give legal advice.

### High-Impact Use Cases & Example Prompts
*   **Contract Review & Extraction:** Identifying specific clauses, obligations, and liabilities within lengthy agreements.
*   **Legal Research Summarization:** Distilling lengthy court opinions into concise IRAC (Issue, Rule, Analysis, Conclusion) summaries.
*   **Drafting Correspondence:** Creating initial drafts of demand letters or client updates.

### Best Practices for Accuracy and Ethics
*   Mandatory verification: Every citation and claim must be verified by a human attorney.
*   Designing prompts that highlight ambiguities in texts rather than attempting to resolve them definitively.
