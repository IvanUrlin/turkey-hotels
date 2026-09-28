# Project instructions

This repository contains a simple static hotel catalogue website.

## General rules
- Keep the project as a simple static site.
- Do not introduce npm, package.json, build tools, frameworks, bundlers, local servers, or other infrastructure unless explicitly requested.
- Prefer the smallest possible change.
- Do not modify unrelated files.

## Files
- index.html contains the site interface and logic.
- hotels-master.txt is the authoritative hotel data source.
- Do not modify hotels-master.txt unless explicitly requested.
- UI changes should normally affect only index.html.

## Development workflow
- Code, UI, responsive-layout, and application-logic changes are implemented by Codex.
- ChatGPT prepares the task for Codex and then performs an independent review of Codex's pull request.
- ChatGPT should not author code/UI/logic changes directly when Codex is available.
- Codex must run the required validation for its implementation, including Playwright/Chromium for UI work.
- ChatGPT reviews the diff, scope, test evidence, regressions, and compliance with these instructions.
- The user performs the final merge after ChatGPT's review.
- Data-only metadata changes (for example hotels-meta.json) and repository-process documentation may be handled directly by ChatGPT when appropriate, but still through a separate branch and pull request.

## Git workflow
- Do not commit directly to main.
- Work in a separate branch.
- Before publishing, check the diff.
- Create a pull request for review.
- Do not merge the pull request yourself.

## Validation
- Confirm that hotels-master.txt is unchanged unless modification was explicitly requested.
- Check that the site still loads hotels from hotels-master.txt.
- Preserve mobile usability.
- At the end, list all changed files.

## UI validation
For any UI or responsive-layout change:
- use Playwright with Chromium;
- test widths 360, 390, 430, and approximately 1000 px;
- verify there is no horizontal page overflow;
- check for console errors and page errors;
- create screenshots for visual review at all tested widths;
- report the tested widths and results before publishing a pull request.
