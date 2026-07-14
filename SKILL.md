---
name: prompt-engineer-pro
description: Advanced prompt engineering intelligence for LLM task optimization
---

# prompt-engineer-pro

Comprehensive prompt engineering guide and framework repository. Contains advanced strategies for chatbot prompting, code generation, creative writing, and data extraction based on a rigorous 7-week Prompt Engineering curriculum.

## How to Use This Skill

When a user requests to create, fix, enhance, or optimize a prompt (or asks you to do a vague task that would benefit from a strict prompt), follow this workflow:

### Step 1: Analyze User Requirements

Extract key information from the user's request:
- **Core Intent**: What is the ultimate goal? (e.g., code generation, creative writing, data extraction, chatbot setup)
- **Target Audience/Tone**: Who is this for? Is it formal, playful, technical?
- **Constraints**: Are there negative constraints (what NOT to do) or format requirements (JSON, Markdown)?

### Step 2: Consult the Knowledge Base (REQUIRED)

Depending on the Core Intent, use the `view_file` tool to search the relevant week's curriculum in the `references/` directory.

- **`references/foundations_of_prompting.md`**: Core Foundations, Anatomy of a Prompt (RACE framework, Role-Task-Format), Zero-Shot vs Few-Shot. Use for **basic task structuring**.
- **`references/advanced_parameters_and_api.md`**: API Integration, Advanced Parameters (Temperature, Top-P), Error Handling. Use for **system prompts and API interactions**.
- **`references/creative_writing_and_data_extraction.md`**: Creative Writing, Persona Adoption, Automating Data Extraction Workflows (JSON/CSV). Use for **creative tasks or data parsing**.
- **`references/code_generation_and_chatbots.md`**: Code Generation, Debugging, Advanced Chatbot Prompting (Prompt Chaining, RAG, Handling Ambiguity). Use for **coding tasks and conversational AI**.
- **`references/image_generation.md`**: AI Image Generation (Midjourney, DALL-E), lighting, styling, textures, character and environment design, negative prompting. Use for **visual and artistic tasks**.
- **`references/data_interpretation_and_insights.md`**: Data Analysis, Descriptive Statistics, Trend Identification, Hypothesis Generation, and Bias Detection. Use for **analytical tasks and data interpretation**.
- **`references/generating_prompts_for_data_visualization.md`**: Chart Types (Bar, Line, Scatter), Axes, Labels, Color Schemes, BI Tools (Tableau, Power BI), and Python Libraries (Matplotlib, Seaborn). Use for **data visualization tasks**.
- **`references/integrating_ai_with_data_analysis.md`**: AI-driven Script Generation, Automated Report Generation, Data Cleaning, and Interpreting Insights. Use for **end-to-end data analysis workflows**.
- **`references/prompt_chaining_and_meta_prompting.md`**: Prompt Chaining, Managing State and Context, Meta-Prompting. Use for **complex AI tasks requiring sequential steps**.
- **`references/optimizing_prompts_for_performance_and_cost.md`**: Prompt Length Optimization, Few-Shot Efficiency, Tokenization, Inference Speed, Benchmarking. Use for **optimizing prompt cost and performance**.
- **`references/robustness_reliability_and_ethics.md`**: Handling Ambiguity, Adversarial Prompts, AI Hallucinations, Bias Detection, Responsible AI Usage. Use for **building trustworthy and ethical AI interactions**.
- **`references/project_ideation_and_scoping.md`**: Identifying AI Opportunities, SMART Goals, Feasibility Assessment, Tool Selection, Project Planning. Use for **planning and scoping real-world AI projects**.
- **`references/building_a_prototype_bot.md`**: Designing FAQ Prompts, Conversation History Management, UI Integration, Handling Escalations. Use for **building functional AI chatbot prototypes**.
- **`references/content_generation_pipeline.md`**: Prompt Chaining, AI-Assisted Research, CMS Integration, Quality Metrics, Workflow Optimization. Use for **building scalable automated content pipelines**.
- **`references/healthcare_prompting.md`**: Medical Terminology, Patient Record Summarization, Diagnostic Assistance, HIPAA Compliance. Use for **healthcare and medical use cases**.
- **`references/finance_prompting.md`**: Market Analysis, Trend Prediction, Financial Reports, Fraud Detection, Regulatory Compliance. Use for **financial and quantitative use cases**.
- **`references/legal_prompting.md`**: Legal Terminology, Case Law Analysis, Document Summarization, Contract Clause Generation. Use for **legal and compliance use cases**.

*If you are already familiar with the frameworks, you may skip reading the files and apply the frameworks directly.*

### Step 3: Select the Appropriate Framework

Based on your analysis, actively apply one of the following frameworks:
- **RACE Framework**: Define the Role, Action, Context, Expectation.
- **Role-Task-Format (RTF)**: Define the Persona, Task, and exact output Format.
- **Chain of Thought (CoT)**: Force the model to "think step-by-step" before outputting the final answer.
- **Prompt Chaining**: For multi-step complex logic, break it down into sequential sub-prompts.

### Step 4: Execute the Enhanced Prompt

**DO NOT just output the optimized prompt for the user.** 
Instead, you must **internally apply** the enhanced prompt and execute the user's actual task yourself. 
Act as the persona defined in your framework (e.g., Senior Python Engineer, Expert Data Analyst) and deliver the final result directly to the user.

---

## Output Formats

1. Briefly state (1-2 sentences) which prompt engineering framework and knowledge base you applied to their request.
2. Deliver the final, high-quality result (the code, the writing, the analysis) that is generated by following your enhanced prompt.

---

## Common Rules for Professional Prompts

These are frequently overlooked issues that make prompts weak:

| Rule | Do | Don't |
|------|----|----- |
| **Negative Constraints** | Explicitly say "Do not include conversational filler" | Assume the LLM will just give the data |
| **Role Assignment** | "You are a senior Python engineer..." | "Write a python script..." |
| **Formatting** | Provide a precise mock-up of the JSON/Markdown structure | "Make it look nice" |
| **Edge Cases** | "If no email is found, output null" | Leave error states undefined |
