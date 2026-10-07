## Welcome to DI 502

This repository holds the markdown templates for your project documentation. 

1. Go to https://id.atlassian.com/manage-profile/security/api-tokens and choose Create API token (the classic kind, not "with scopes"). Copy it; Atlassian shows it only once.
2. In Github, go to Settings → Secrets and variables → Actions. On the Secrets tab, add: CONFLUENCE_EMAIL and CONFLUENCE_API_TOKEN
Secrets are encrypted, can't be read back, and are masked as *** if they ever appear in a log.
3. On the Variables tab, add: 
    * `CONFLUENCE_BASE_URL`: https://<site>.atlassian.net
    * `CONFLUENCE_SPACE_KEY`: the key from the space URL, /wiki/spaces/<KEY>/…
Variables are for settings that aren't secret, and you can see and edit them later.
