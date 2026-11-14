# API Documentation Security Guidelines (`SECURITY.md`)

**Target:** Public API documentation portfolio (`technical-writing-portfolio`) covering REST APIs, authentication flows, and webhooks.

When reviewing Pull Requests, enforce the following security standards:

## 1. Credential & Token Hygiene in Examples
- **No Real Secrets:** Ensure no live API keys, Bearer tokens, OAuth client secrets, webhook signing secrets, or private keys appear in Markdown files, OpenAPI specs, or HTML outputs.
- **Standardized Placeholders:** Require explicit placeholders in examples (e.g., `Bearer <YOUR_API_TOKEN>`, `whsec_example_secret_key`, `https://example.com`).

## 2. Secure API & Webhook Guidance
- **Webhook Verification Best Practices:** Flag any webhook verification example that encourages insecure practices (such as skipping signature verification, disabling TLS validation, or comparing signatures without constant-time comparison notes where relevant).
- **Sensitive Data in Logs/URLs:** Ensure authentication tokens or personally identifiable information (PII) are never passed in query parameters (`?api_key=...`) in documentation examples.

## 3. GitHub Pages & Workflow Security
- **Minimal Permissions:** Verify that `.github/workflows` files use least-privilege permissions (`permissions: contents: read`) and safe deployment configurations.

## 4. Reporting Security Issues
- If you find an exposed credential or security flaw in this repository, please contact the maintainer (`@ekatmoz88-alt`) directly before public disclosure.
