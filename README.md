# Berkshire Hathaway CMIS — bilingual website

This is a static, responsive website. Russian is the default language; use the EN/RU control in the top bar to switch languages.

## Publish online for free (Cloudflare Pages)
1. Create a GitHub account and a new repository, for example `berkshire-cmis`.
2. Upload `index.html` from this folder to the repository root and commit.
3. Sign in to Cloudflare and open **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
4. Select the repository. Choose **None** as the framework preset; leave the build command empty; set the build output directory to `/` (or `.` if requested).
5. Deploy. Cloudflare will provide a public `*.pages.dev` address. A custom domain can be connected later.

Alternative: GitHub Pages. Put `index.html` in a repository, then open **Settings → Pages**, choose deploy from branch `main` and folder `/root`.

## Important: static site vs. server application
The current version is hosted on a web server/CDN when published, but it is a static front end: it has no application backend or central database. The decision register exists only in the current browser session and is not shared between users/devices. For logins, shared records, persistent data, permissions and audit history, add a backend (for example Supabase Auth + Postgres, or a server API). Do not put confidential business data into this demo.

Financial figures are historical reference values and should be checked against the latest Berkshire Hathaway filings. Proposed workflows and roles are a CMIS design concept, not claims about Berkshire's internal processes.
