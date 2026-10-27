# Code Review for Vibe Coders v2

Built for non-professional developers, this skill reviews code and explains every finding in plain English. It works best on small projects such as single-file web apps, personal scripts, and simple backends.

## Four-Pass Review

Every review runs four passes in the same order:

- **Bugs:** The first pass finds common bugs and logic errors.
- **Security:** The second pass finds security weaknesses, focusing on the risks that apply to where the code runs: a static site, a server, or a local script.
- **Secrets and personal data:** The third pass finds exposed secrets, personal data, local and network paths, and files that should not be in a public repository.
- **Links and scripts:** The fourth pass reviews every link and external script in the code for warning signs, such as insecure connections, URL shorteners, look-alike domains, and unpinned script versions. It judges each link from the code alone and does not open it.

After the four passes, the skill checks whether multiple less severe findings combine into a more severe risk and reports back.

## Findings

Each finding receives one of three labels:

- **Critical — Fix before you ship:** The issue can cause real harm and should be fixed before anyone uses the code.
- **Important — Fix when you have time:** The issue is a real weakness worth fixing soon.
- **Optional polish — Nice to have:** The change is a minor improvement rather than a necessary fix.

## Limits

The skill reads code but does not run it or open the links in it. It is designed for interactive reviews in a chat, not for automated or agentic workflows. When code appears to handle a high-risk feature, such as payments, logins, sensitive data, public file uploads, or access to other users' data, the skill will warn you to have a security professional review it or have an established service handle that feature.

This skill helps catch common issues, but it does not guarantee that code is secure or free of bugs. Its findings and severity labels are the AI's best judgment and can be incomplete or wrong. Treat each review as a strong first check, not a final sign-off. The skill is provided as-is, with no warranty. See the LICENSE file for the full legal disclaimer.

## Install

Upload the `SKILL.md` file directly, or a `.skill` package that contains it, into your AI assistant's Skills section.
