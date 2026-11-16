# CVForge

Tailor a CV to a specific job, find what is missing and how to cover it, tune your LinkedIn profile, write a cover letter that sounds like a person, and share a digital CV by link. Runs entirely in the browser. Works with any LLM.

## What you get
| Need | Where |
|---|---|
| a) CV modified for a given role | Master prompt and web page step 4 |
| b) Key expertise highlighted from the existing CV | "Key expertise to lead with" panel plus reordered skills and bullets |
| c) Digital CV shareable via link | "Create share link" (CV is encoded inside the URL, no server), plus HTML and PDF export |
| d) What to do when a key requirement is missing | Gaps tab: severity and 2 to 4 honest ways to cater to each |
| e) LinkedIn edits for the role | Headline, About, skills, experience rewrites, featured ideas |
| f) Unique cover letter, no em dashes, human voice | Cover letter tab. Prompt rules plus automatic dash stripping |

## Repo layout
```
index.html                  the whole web app (no build step)
SKILL.md                    portable skill for Claude, GPT, Gemini and others
prompts/master-prompt.md    one paste prompt that returns structured JSON
docs/use-with-any-llm.md    setup for each LLM tool
examples/sample-output.json sample of the JSON the page reads
.github/workflows/pages.yml auto deploy to GitHub Pages
```

## Deploy on GitHub (2 minutes)
1. Create a new public repo and push these files to `main`.
2. Settings, Pages, Source: **GitHub Actions**.
3. The workflow publishes to `https://<your-user>.github.io/<repo>/`.

(Or choose Source: Deploy from a branch, `main`, `/ (root)`, and skip the workflow.)

## How it works
1. Paste CV and job description. The page shows a quick local keyword match.
2. Copy the generated prompt into any LLM, or paste an API key and run it from the page. The key stays in memory and goes only to the provider you pick.
3. Paste the JSON reply. The page renders the tailored CV, gaps, LinkedIn advice and cover letter.
4. Press Create share link. Anyone opening it sees only the CV (not gaps, LinkedIn tips or the letter).

## Privacy
No backend, no analytics, no storage. The share link contains the CV text itself, so treat the link like the CV. Remove phone or address if you do not want them public.

## Honesty guardrail
The prompt forbids inventing employers, dates, tools or numbers, and tells the model to suggest real ways to close gaps instead of covering them up. Check the result before you send it.

## Customise
Edit the `PROMPT` constant in `index.html` and `prompts/master-prompt.md` together. Change the banned word list or tone there.

MIT licence.
