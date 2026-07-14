# Week 7 Summary: Domain-Specific Prompt Engineering Cheat Sheet

This guide serves as a quick reference for interacting with the Prompt Engineer Pro skill across three specialized and highly regulated industries: **Healthcare**, **Finance**, and **Legal**. 

## 1. Healthcare & Medicine (`healthcare_prompting.md`)
*   **Core Focus:** Precision, empathy, and adherence to medical frameworks (e.g., SOAP notes).
*   **Key Constraints:** HIPAA compliance (do not prompt with PHI/PII); hallucinations can be life-threatening.
*   **Best Practices (CRAFT-GT Framework):**
    *   *Context & Grounding:* Always inject specific, verified medical guidelines or anonymized history.
    *   *Role:* Explicitly state the persona (e.g., "Act as an empathetic primary care physician").
    *   *Chain-of-Thought:* Force step-by-step clinical reasoning to improve diagnostic accuracy.
    *   *Human-in-the-Loop:* Always require clinician review before applying AI outputs.

## 2. Finance & Banking (`finance_prompting.md`)
*   **Core Focus:** Quantitative accuracy, structured data analysis, and regulatory reporting (e.g., GAAP).
*   **Key Constraints:** Strict adherence to SEC/FINRA regulations; mitigating AI's weakness in pure math.
*   **Best Practices:**
    *   *Data-Driven Prompting:* Provide well-formatted tabular data (CSV, JSON) for analysis.
    *   *Task Decomposition:* Separate extraction from calculation (e.g., extract metrics first, calculate via script).
    *   *Instructional Constraints:* Force the model to cite specific sections of financial documents (like 10-K filings).

## 3. Legal Profession (`legal_prompting.md`)
*   **Core Focus:** Precision in legalese, identifying ambiguities, and strict adherence to client confidentiality.
*   **Key Constraints:** Attorney-client privilege; severe consequences for fictitious citations (fake case law); avoiding the Unauthorized Practice of Law (UPL).
*   **Best Practices:**
    *   *Retrieval-Augmented Generation (RAG):* Connect prompts to verified case law databases rather than relying on the LLM's general knowledge.
    *   *Negative Prompting:* Explicitly state "Do not invent cases" and "State if the agreement is silent on a matter rather than guessing."
    *   *Verification:* Demand sources for all legal claims and ensure mandatory review by a licensed attorney.
