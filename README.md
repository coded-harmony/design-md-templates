# DESIGN.md templates for coding agents

Four [DESIGN.md](https://github.com/google-labs-code/design.md) files you can drop into a repo so Claude Code, Cursor, Codex or Gemini CLI stop guessing what your product looks like. Each one passes Google's linter with 0 errors and 0 warnings (`@google/design.md` 0.4.0), and each was tested by handing it to a fresh Claude Code agent with a single sentence.

| Template | For | What an agent built from it |
|---|---|---|
| [`saas-dashboard/`](saas-dashboard/DESIGN.md) | Dense B2B dashboards: graphite on warm paper, one green, tabular figures | [Screenshot](https://floo.design/images/blog/design-md-templates/demo-dashboard.webp) · [page](https://floo.design/experiments/design-md-templates/dashboard.html) |
| [`mobile-app/`](mobile-app/DESIGN.md) | Friendly consumer apps: big targets, one accent per screen, a voice that never guilts | [Screenshot](https://floo.design/images/blog/design-md-templates/mobile.webp) · [screen](https://floo.design/experiments/design-md-templates/mobile.html) |
| [`landing-page/`](landing-page/DESIGN.md) | Calm, editorial B2B landing pages with the product as the hero | [Screenshot](https://floo.design/images/blog/claude-code-landing-page-experiment/fold-b.webp) |
| [`docs-site/`](docs-site/DESIGN.md) | Developer docs built for reading and copying code | [Screenshot](https://floo.design/images/blog/design-md-templates/demo-docs.webp) · [page](https://floo.design/experiments/design-md-templates/docs.html) |

The full write-up, with every screenshot and what each file's rules changed: **[DESIGN.md templates for Claude Code, Cursor and Codex](https://floo.design/blog/design-md-templates)**.

## Use one

1. Copy the closest `DESIGN.md` to the root of your repo, then rename the colours, fonts and the Overview paragraph to fit your product. The Overview does more work than the hex codes.
2. Agents don't load `DESIGN.md` on their own, so point at it from `CLAUDE.md` or `AGENTS.md`:

   ```md
   ## Design
   Before any UI work, read DESIGN.md and follow it. If a request conflicts
   with it, say so instead of improvising.
   ```

3. Lint it before you commit:

   ```bash
   npx @google/design.md lint DESIGN.md
   ```

## Write your own

Make six decisions: who it's for and how it should feel (name a place, not adjectives); five or six colours, each with one job; two typefaces and a size ceiling; what the hero or main screen shows; which sections or screens to build; four don'ts. Why those six: [we gave Claude Code the same landing page brief four ways](https://floo.design/blog/claude-code-landing-page-experiment).

---

Made by [Floo](https://floo.design), a shared design canvas where people and coding agents design together. MIT licensed.
