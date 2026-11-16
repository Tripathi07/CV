# CVForge (flat layout)

Tailor a CV to a job (pasted text, or one job/company link), find gaps and how to cover them, fix LinkedIn, write a human cover letter, and share a digital CV link. Runs in the browser, works with any LLM.

Files: index.html (app), SKILL.md (portable skill), master-prompt.md (paste prompt), use-with-any-llm.md (setup per tool), sample-output.json (sample).

Deploy: upload all files to a repo root, then Settings, Pages, Deploy from a branch, main, / (root).

CV input: paste text or upload PDF, Word, txt or md (read in your browser). Job input: paste text or one link. Details load automatically and the match runs. Link fetching uses the r.jina.ai reader; LinkedIn may block it, then paste the text. MIT licence.
