# Security Policy

## Supported Versions

We actively maintain and support the latest version of this daily.dev DevCard project.

| Version | Supported          |
| ------- | ------------------ |
| 2.x.x   | :white_check_mark: |
| 1.x.x   | :x:                |

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please report it responsibly:

1. **Do not** create a public GitHub issue for security vulnerabilities
2. **Do** send an email to the repository maintainer
3. Include a detailed description of the vulnerability
4. Provide steps to reproduce the issue
5. Include any relevant technical details

## Security Considerations

This project uses:

- GitHub Actions with appropriate permissions
- GitHub Secrets for sensitive data (USER_ID)
- daily.dev official API endpoints
- Automated dependency updates via Dependabot

## Best Practices

When contributing to this project:

- Never commit secrets or API keys
- Use GitHub Secrets for sensitive configuration
- Keep dependencies up to date
- Follow the principle of least privilege for GitHub Actions permissions

## Response Timeline

We will respond to security reports within:

- **24 hours**: Initial acknowledgment
- **7 days**: Detailed assessment and fix plan
- **30 days**: Security fix implementation and release
