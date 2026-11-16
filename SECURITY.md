# 🛡️ Security and responsible data use

## 🔐 Secrets and local data
- Never commit API keys, access tokens, passwords, browser cookies, private URLs, or personal information.
- Keep local environment files private. Use `.env.example` only for non-secret variable names and safe placeholders.
- Treat notebooks, outputs, downloaded images, and logs as potentially sensitive.
- Keep generated downloads and model artifacts outside the repository unless their inclusion is necessary and permitted.

## 🚦 Competition integrity
The challenge prohibits external price lookup. Do not use this repository to scrape product prices, call pricing APIs, query external price databases, or evade authentication, throttling, CAPTCHAs, or access controls. Image access must comply with challenge rules and source terms.

## 🐛 Reporting a vulnerability
Report suspected credential exposure, unsafe data handling, or exploitable code privately through the repository owner's GitHub profile: [@Brajesh31](https://github.com/Brajesh31). Include a concise description, affected file, reproduction steps, and impact. Do not publish exploit details or attach secrets in a public issue.

## 🧹 If a secret is committed
Revoke or rotate it immediately. Removing it from the latest commit is not sufficient because Git history may retain it. Review logs and connected services for misuse.
