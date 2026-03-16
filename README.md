# Copilots & Creators – Build with AI 🤖

Presentation slides for the **"Copilots & Creators: Build with AI"** workshop held on 17 March 2026 at Centric.

This workshop covers how developers can use AI tooling (GitHub Copilot, CLI agents, generative AI) to build faster, think bolder, and integrate AI into their daily workflow.

## Agenda

| Block | Topic | Time |
|-------|-------|------|
| Intro | Setting the Stage | 0:00 – 0:15 |
| Block 1 | Smarter Building with AI (prompt basics, code gen, mini-challenge) | 0:15 – 1:00 |
| Break | | 1:00 – 1:15 |
| Block 2 | Integration & Best Practices (workflow, pitfalls, mindset) | 1:15 – 1:45 |
| Wrap-up | Showcase & Takeaways | 1:45 – 2:00 |

## Running the Presentation

This project uses [Slidev](https://sli.dev) — a Markdown-based presentation framework for developers.

**Prerequisites:** [Node.js](https://nodejs.org) and [pnpm](https://pnpm.io)

```bash
pnpm install
pnpm dev
```

Then open [http://localhost:3030](http://localhost:3030) in your browser.

### Other commands

```bash
pnpm build    # Build as a static SPA
pnpm export   # Export to PDF / PPTX
```

## Project Structure

```
slides.md          # Main presentation content
pages/             # Optional imported slide pages
components/        # Custom Vue components
snippets/          # Code snippets used in slides
patches/           # Dependency patches
package.json
```

## Resources

- [Slidev documentation](https://sli.dev)
- [GitHub Copilot docs](https://docs.github.com/copilot)
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [OWASP AI Security](https://owaspai.org/)

