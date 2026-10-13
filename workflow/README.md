# n8n workflow

Put the exported workflow here as `causal-audit.json`.

## Exporting safely

n8n does not include credential secrets in exports, but check the file before committing:

- No API keys pasted into Code nodes or HTTP headers
- No personal email addresses or internal URLs
- Credential references are fine (they are names and IDs, not secrets)

## Importing

1. In n8n: **Workflows → Import from file** and choose `causal-audit.json`.
2. Create two credentials: **OpenAI** and **Tavily**.
3. Open each node that shows a credential warning and select the new credential.
4. Activate the workflow. The production webhook path must match the one the front end calls.
