# Prompt Engineer Pro (Antigravity Skill)

**Prompt Engineer Pro** is a world-class prompt engineering skill for Google Antigravity. It acts as an elite prompt architect, intercepting your vague or general tasks and automatically rewriting them into highly optimized, detailed prompts that yield outstanding results when fed to Large Language Models.

This skill is powered by a comprehensive 4-week Prompt Engineering curriculum knowledge base, natively integrated so the AI can look up and apply advanced frameworks (RACE, RTF, Chain of Thought, Prompt Chaining) on the fly.

## 🚀 Installation

To install this skill, simply clone this repository into your Antigravity global skills directory.

### Windows (PowerShell)
```powershell
cd C:\Users\$env:USERNAME\.gemini\config\skills
git clone https://github.com/Sriram1576/Prompt-Engineering-for-AI.git prompt-engineer-pro
```

### macOS / Linux
```bash
mkdir -p ~/.gemini/config/skills
cd ~/.gemini/config/skills
git clone https://github.com/Sriram1576/Prompt-Engineering-for-AI.git prompt-engineer-pro
```

## 💡 How to Use It

Once installed, Antigravity will automatically detect the skill. You don't need to run any special commands! Just talk to your AI agent and ask it to write or enhance a prompt for you.

**Example Prompts to try with your agent:**
- *"I need to write a Python script for a web scraper, but first, enhance this prompt for me."*
- *"Write a prompt that will help me extract names and emails from a messy text file."*
- *"I want to generate a creative story about a space pirate. Can you draft an optimized prompt using the RTF framework?"*

The agent will analyze your request, consult its internal knowledge base, and output the perfect, ready-to-copy prompt in a markdown code block!

## 🧠 What's Inside the Knowledge Base?

The skill relies on a built-in curriculum located in the `references/` directory:
- **`foundations_of_prompting.md`**: Core Foundations (Anatomy of a Prompt, RACE framework, Role-Task-Format, Zero-Shot vs Few-Shot).
- **`advanced_parameters_and_api.md`**: Advanced Parameters & API Integration (Temperature, Top-P, Error Handling).
- **`creative_writing_and_data_extraction.md`**: Creative Writing & Automating Data Extraction Workflows (JSON/CSV).
- **`code_generation_and_chatbots.md`**: Code Generation, Debugging, & Advanced Chatbot Prompting (Prompt Chaining, RAG, Handling Ambiguity).
- **`image_generation.md`**: AI Image Generation (Midjourney, DALL-E), lighting, styling, textures, character and environment design, negative prompting.

## 🛠️ Architecture

Unlike traditional programmatic skills that rely on hardcoded Python scripts, this skill leverages the AI's native natural language reasoning. When invoked, the AI follows the strict workflow defined in `SKILL.md` to:
1. Analyze the user's core intent.
2. Search and read the relevant `week_X.md` documentation.
3. Select the best framework (e.g. RACE, RTF).
4. Generate the optimized prompt.