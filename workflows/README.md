# Workflow exports

**No actual n8n workflow export is included.** An export will be added **only if the author supplies one**.

When an export is supplied, sanitize it **before publication**:

- Replace all credentials, API keys, tokens, password values, authorization headers, and embedded connection secrets with clearly marked placeholders.
- Replace webhook endpoints and callback URLs with `YOUR_WEBHOOK_URL` or an equivalent clearly labeled placeholder.
- Replace workspace, project, instance, workflow, account, credential, and tenant identifiers with marked placeholders such as `YOUR_ACCOUNT_ID`.
- Remove or replace customer and client names, company names, real phone numbers, email addresses, personally identifying notes, transcripts, and other real data.
- Inspect node parameters, expressions, URLs, headers, sample/pinned data, notes, code nodes, and embedded JSON; secrets can appear outside a credentials section.
- Verify the sanitized file contains no sensitive information or identifying screenshots before committing it.

[TODO: Author to provide a workflow export and confirm that its contents may be shared publicly.]
