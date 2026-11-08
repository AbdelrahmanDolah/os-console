# OS Console

A single static page for issuing commands, approving work, and following agents in a private GitHub repository.

- No build step, no external scripts. One file: `index.html`.
- Data is read and written live through the GitHub REST API with a fine-grained personal access token that the user pastes into the page.
- The token is kept only in the user's browser (localStorage, or sessionStorage if "remember" is off) and is sent only to `https://api.github.com`. A Content-Security-Policy in the page blocks every other host.
- This repository holds code only. No project data lives here.

Recommended token: fine-grained, one repository, Contents / Issues / Pull requests set to Read and write, 90-day expiry.
