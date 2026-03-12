# TextCleanup

A single-file browser app for AI-powered text transformations. Paste any text, type a natural-language instruction, and get back the transformed result instantly.

## Features

- **AI-powered transforms** — describe what you want in plain English (e.g. "sort lines alphabetically", "remove empty lines", "translate to German")
- **Multi-provider** — works with **Google Gemini** (free tier), Anthropic (Claude), and OpenAI (GPT); switch anytime in settings
- **Undo stack** — up to 50 steps back with Cmd+Z / Ctrl+Z
- **Prompt history** — recent instructions stored locally for quick reuse, with per-entry delete
- **Zero dependencies** — single HTML file, no build step, no server required
- **Privacy-first** — API keys stored only in your browser's localStorage, never sent anywhere except the chosen AI provider
- **Mobile-friendly** — responsive layout, 44px touch targets, safe-area support, and icons-only toolbar on small screens (iOS and Android)

## Usage

### Option A — Open locally

Just open `index.html` in any modern browser.

### Option B — GitHub Pages

1. Fork / clone this repo
2. Go to **Settings → Pages** and set source to the `main` branch (root)
3. Access at `https://<your-username>.github.io/<repo-name>/`

## Setup

1. Click the **⚙** gear icon in the top-right
2. Choose your provider: **Google (Gemini)** for a free tier, or Anthropic / OpenAI
3. Paste in your API key
4. Select the model and click **Save**

Keys are saved in `localStorage` — they persist across sessions in the same browser.

**Getting API keys:**

- **Gemini (free):** [Google AI Studio](https://aistudio.google.com) — create an API key at no cost
- **Anthropic:** [console.anthropic.com](https://console.anthropic.com)
- **OpenAI:** [platform.openai.com](https://platform.openai.com)

## Supported Models

| Provider  | Models |
|-----------|--------|
| Google    | Gemini 2.0 Flash (recommended), Gemini 1.5 Flash, Gemini 1.5 Flash 8B, Gemini 1.5 Pro |
| Anthropic | Claude Haiku 4.5 (recommended), Claude 3.5 Haiku, Claude 3 Haiku |
| OpenAI    | GPT-4o Mini (recommended), GPT-3.5 Turbo, o1 Mini |

Lightweight models are listed by default for cost-effective text transformation.

## Security Note

API calls are made directly from your browser to the chosen AI provider. Keys never leave your device except to that provider’s API. **Do not share your API keys.**
