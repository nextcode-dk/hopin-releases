# HopIn.chat release notes

Static site served by GitHub Pages from the repo root: https://nextcode-dk.github.io/hopin-releases/

## Add a release

1. Open `releases.json` and add a new object at the **top** of the array (newest first):

   ```json
   {
     "version": "1.18.0",
     "date": "2026-11-20",
     "title": "Optional short title",
     "items": [
       { "type": "new", "text": "One short, user-facing sentence." },
       { "type": "improved", "text": "..." },
       { "type": "fixed", "text": "..." }
     ]
   }
   ```

   `type` is `new`, `improved` or `fixed`. Aim for 1 to 6 bullets.
2. Commit and push to `main`. Pages redeploys in a minute.

## Keep it public-safe

This site is public. Write plain English for users. No issue or PR numbers, branch names, file paths, key or variable names, infrastructure details, emails or exploit details. Security fixes are just "Security hardening".

## Preview locally

`python3 -m http.server 8000` and open http://localhost:8000 (the page loads `releases.json` with fetch, so opening the file directly will not work).
