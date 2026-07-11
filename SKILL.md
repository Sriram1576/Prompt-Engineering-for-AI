---
name: prompt-engineer-pro
description: Advanced prompt engineering intelligence for LLM task optimization
---

# prompt-engineer-pro

Comprehensive prompt engineering guide and framework repository. Contains advanced strategies for chatbot prompting, code generation, creative writing, and data extraction based on a rigorous 4-week Prompt Engineering curriculum.

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

*If you are already familiar with the frameworks, you may skip reading the files and apply the frameworks directly.*

### Step 3: Select the Appropriate Framework

Based on your analysis, actively apply one of the following frameworks:
- **RACE Framework**: Define the Role, Action, Context, Expectation.
- **Role-Task-Format (RTF)**: Define the Persona, Task, and exact output Format.
- **Chain of Thought (CoT)**: Force the model to "think step-by-step" before outputting the final answer.
- **Prompt Chaining**: For multi-step complex logic, break it down into sequential sub-prompts.

### Step 4: Generate the Prompt

**DO NOT execute the user's actual task.** Your job is to output the optimized prompt for them to use.

---

## Example Workflow

**User request:** "Write a prompt to help me extract names and emails from a messy text file."

### Step 1: Analyze Requirements
- Intent: Data Extraction
- Constraints: Must handle messy text, extract specific entities (names, emails).

### Step 2 & 3: Consult & Select Framework
- Knowledge Base: `creative_writing_and_data_extraction.md` (Automating Data Extraction)
- Framework: RTF (Role, Task, Format) with Few-Shot examples.

### Step 4: Generate Output
**Output:**
```text
You are an expert data extraction algorithm. 
Your task is to scan the following messy text and extract all human names and email addresses.

Format the output strictly as a JSON array of objects, like this:
[
  {"name": "John Doe", "email": "john@example.com"}
]

Do not include any conversational text in your response. Only output the JSON.
Text to parse:
[INSERT TEXT HERE]
```
*This prompt uses the RTF framework and strict negative constraints to ensure the output is pure JSON.*

---

## Output Formats

Always output the final, optimized prompt inside a Markdown code block (` ```text `) so the user can easily copy and paste it. Provide a brief 1-2 sentence explanation below the block explaining which framework you used and why.

---

## Common Rules for Professional Prompts

These are frequently overlooked issues that make prompts weak:

| Rule | Do | Don't |
|------|----|----- |
| **Negative Constraints** | Explicitly say "Do not include conversational filler" | Assume the LLM will just give the data |
| **Role Assignment** | "You are a senior Python engineer..." | "Write a python script..." |
| **Formatting** | Provide a precise mock-up of the JSON/Markdown structure | "Make it look nice" |
| **Edge Cases** | "If no email is found, output null" | Leave error states undefined |
