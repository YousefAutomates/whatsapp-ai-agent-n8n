# Security Policy

## ⚠️ Important Security Notice

This repository contains n8n workflow files for WhatsApp automation.

## Sensitive Information — Never Commit These!

| Item | Where to Store |
|------|---------------|
| Access Tokens | n8n Credentials (encrypted) |
| App Secrets | Environment variables |
| Phone Number IDs | n8n node configuration |
| WABA IDs | n8n node configuration |
| Verify Tokens | n8n node configuration |

## Reporting Security Issues

If you discover a security vulnerability, please:
1. **Do NOT** open a public GitHub Issue
2. Contact directly via: [yousefautomates.pages.dev](https://yousefautomates.pages.dev/)
3. Include a description of the issue

## Best Practices

- Use System User Tokens (never expire) instead of temporary tokens
- Rotate tokens periodically
- Use n8n's built-in credential encryption
- Never share credentials in workflow exports
- Regularly audit Meta app permissions
