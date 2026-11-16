# Using CVForge in different LLM tools

All routes use the same text: `SKILL.md` (rules and workflow) and `master-prompt.md` (ready to paste prompt with JSON output).

| Tool | How |
|---|---|
| **Claude (claude.ai, Cowork, Claude Code)** | Zip the repo folder as `cvforge.zip` with `SKILL.md` at the top level and upload it under Settings, Capabilities, Skills. Or create a Project and paste `SKILL.md` into the project instructions. In Claude Code, copy the folder to `~/.claude/skills/cvforge/`. |
| **ChatGPT** | Create a Custom GPT. Paste `SKILL.md` into Instructions. Upload `master-prompt.md` as Knowledge. Or just paste the master prompt into a normal chat. |
| **Gemini** | Create a Gem. Paste `SKILL.md` as the instructions. Paste the master prompt for one-off use. |
| **Microsoft Copilot** | Paste the master prompt in chat. In Copilot Studio, put `SKILL.md` in the agent instructions. |
| **Perplexity, Mistral Le Chat, DeepSeek, others** | Paste the master prompt in chat. |
| **API or local models (Ollama, LM Studio)** | Send the master prompt as the user message. Smaller models do better if you split steps: first ask for the gap analysis, then the CV JSON, then the letter. |

## Round trip with the web page
1. Open the CVForge page, paste CV and job description, press Copy prompt.
2. Paste into any LLM above. Ask it to return JSON only if it adds commentary.
3. Paste the reply into step 3C on the page. You get the tailored CV, gaps, LinkedIn edits, cover letter and a share link.

## Tips
- Paste the whole job description, not a summary.
- If the model uses a dash anyway, the page strips it. In a plain chat, reply: "Remove every em dash and en dash."
- Always check numbers and dates against your original CV before sending.
