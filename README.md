# Fix My UI

A browser tool that reviews HTML components and returns structured feedback — what is broken, why it matters, and what to change.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## What it does

Paste an HTML component. Get back four things:

- **Issues** — problems ranked as critical, warning, or suggestion
- **Improved code** — your component rewritten with the fixes applied
- **Quick fixes** — specific before/after changes
- **UX reasoning** — the principle behind each recommendation

The tool focuses on identifying problems, not generating new UI.

---

## Features

- **Severity filter** — show or hide issues by critical, warning, or suggestion level
- **Session history** — last 5 reviewed components stored in session, click any to reload
- **Export as Markdown** — download the full review as a `.md` file, ready to paste into a PR or ticket
- **Export as JSON** — download the full structured review including scores and metadata
- **Dark and light mode** — toggle between themes using the button in the top-right corner
- **Complexity indicator** — live readout of line count and complexity level as you type, with a hint if the component is too large for reliable output
- Four review modes: Standard, Strict, Senior dev, Accessibility
- Focus area toggles: Hierarchy, UX copy, Spacing, Accessibility, Mobile, Performance
- Works with Claude, OpenAI, Grok, and Gemini via your own API key

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

Issues found:

- `critical` — CTA label "Go" gives no information about the action
- `warning` — "Click here" is not descriptive; unclear what will happen
- `suggestion` — No visual hierarchy between heading and body text

Improved output:

```html
<div class="card">
  <h2>Get started with your account</h2>
  <p>Complete your profile to unlock all features.</p>
  <button class="btn-primary">Set up my account</button>
</div>
```

Tested with common UI patterns such as cards, forms, and simple dashboards.

---

## Usage

No install required.

```bash
git clone https://github.com/roynick365/fix-my-ui
cd fix-my-ui
open docs/index.html
```

Or use it live at [roynick365.github.io/fix-my-ui](https://roynick365.github.io/fix-my-ui)

---

## API keys

The tool runs directly in the browser using your own API key. Keys are held in browser memory only — never stored, never sent anywhere except to the provider you choose.

| Provider | Free tier | Get key |
|----------|-----------|---------| 
| Claude   | Yes | [console.anthropic.com](https://console.anthropic.com) |
| OpenAI   | Yes | [platform.openai.com](https://platform.openai.com) |
| Grok     | Yes (generous) | [x.ai](https://x.ai/api) |
| Gemini   | Yes (generous) | [aistudio.google.com](https://aistudio.google.com) |

Note: Gemini requires the tool to be served over https. It works at the live demo URL. It will not work if you open the file directly from your filesystem. Claude, OpenAI, and Grok work from any origin.

---

## Review modes

| Mode | What it does |
|------|-------------|
| Standard | Balanced, practical review |
| Strict | Direct feedback without softening |
| Senior dev | Explains reasoning as a senior engineer would to a junior |
| Accessibility | WCAG, ARIA, contrast, keyboard navigation |

---

## Limitations

- Works best on small to medium components — full page reviews lose accuracy
- Output quality depends on input quality; vague or incomplete HTML gets vague feedback
- Does not replace a design system or a human design review
- Suggestions still require manual judgment before applying

---

## Tech

- HTML, CSS, vanilla JavaScript
- No dependencies, no build step, no backend or setup required
- Calls provider APIs directly from the browser

---

## Roadmap

- Before / after rendered preview
- CSS analysis alongside HTML
- Screenshot / image input

---

## Contributing

Issues and pull requests are welcome. If you want to add a provider or a new review mode, open an issue first.

---

## License

MIT
