# CVForge (flat layout)

Tailor a CV to a job, find gaps and how to cover them, fix LinkedIn, write a human cover letter, and share a digital CV link. Runs in the browser, works with any LLM.

All files sit in the repo root so they upload cleanly through the GitHub web page.

| File | Purpose |
|---|---|
| index.html | the web app (no build step) |
| SKILL.md | portable skill for Claude, GPT, Gemini and others |
| master-prompt.md | one paste prompt that returns structured JSON |
| use-with-any-llm.md | setup for each LLM tool |
| sample-output.json | sample of the JSON the page reads |

## Deploy
1. Upload all files to a new repo (Add file, Upload files, select all, Commit).
2. Settings, Pages, Source: Deploy from a branch, branch `main`, folder `/ (root)`, Save.
3. Open `https://<your-user>.github.io/<repo>/` after a minute.

## Use
Paste CV and job description, copy the prompt into any LLM (or run it with your API key), paste the JSON reply back, then create the share link. The link holds the CV inside the URL, so treat it like the CV itself.

MIT licence.
