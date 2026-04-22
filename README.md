# Fix My UI

A developer tool that analyzes UI components and returns structured, actionable feedback — issues found, improved code, UX reasoning, and quick fixes.

Works with Claude, OpenAI, Groq, and Gemini. All free tiers supported. No backend, no account, no cost to run.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Multi-provider](https://img.shields.io/badge/providers-Claude%20%7C%20OpenAI%20%7C%20Grok%20%7C%20Gemini-yellow.svg)]()
[![No backend](https://img.shields.io/badge/backend-none-green.svg)]()

---

## The problem

Developers know when a UI feels wrong. They do not always know why.

There is no tool that takes a component, explains what is broken, and hands back improved code with the reasoning attached. Fix My UI does exactly that.

---

## What it does

Paste any HTML component. Choose your AI provider. Get back:

- **Issues** — problems ranked as critical, warning, or suggestion
- **Improved code** — your component rewritten and ready to use
- **Quick fixes** — specific before/after changes
- **UX reasoning** — the principle behind each recommendation
- **Scores** — overall, hierarchy, copy, and accessibility ratings

---

## Providers

| Provider | Free tier | Get key |
|---|---|---|
| Claude | Yes | [console.anthropic.com](https://platform.claude.com/) |
| OpenAI | Yes | [platform.openai.com](https://platform.openai.com/) |
| Grok | Yes (generous) | [x.ai](https://x.ai/api) |
| Gemini | Yes (generous) | [aistudio.google.com](https://aistudio.google.com/) |

Your API key is held in browser memory only. It is never stored, never logged, never sent anywhere except directly to the provider you choose.

---

## Review modes

| Mode | Description |
|---|---|
| Standard | Balanced, practical review |
| Strict | Direct and unsparing — no softening |
| Senior dev | Explains reasoning as a senior engineer to a junior |
| Accessibility | WCAG, ARIA, contrast, keyboard navigation |

---

## Quick start

No install required. Open the file and use it.

```bash
git clone https://github.com/roynick365/fix-my-ui/
cd fix-my-ui
open index.html
```

Or use it live at **roynick365.github.io/fix-my-ui**

---

## Example

Input:
```html
<div class="card">
  <h2>Welcome</h2>
  <p>Click here</p>
  <button>Go</button>
</div>
```

Output (abbreviated):
- `critical` — CTA label "Go" gives the user no information about the action
- `warning` — No spacing between elements reduces scannability
- `suggestion` — Heading text is too generic for context

Improved code returned with clearer CTA, better copy, and structured spacing.

---

## Upcoming features

- Screenshot input — analyze from a pasted image, no code needed
- Before vs after rendered preview
- CSS analysis alongside HTML
- VS Code extension
- Shareable diagnosis links
- React / JSX support
- Team history and version tracking
- Design token suggestions

---

## Tech

- HTML, CSS, vanilla JavaScript
- No dependencies
- No build step
- No backend
- Calls provider APIs directly from the browser

---

## Contributing

Issues and pull requests are welcome. If you want to add a provider or a new review mode, open an issue first to discuss.

---

## License

MIT
