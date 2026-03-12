# TextCleanup

A single-file browser app for AI-powered text transformations. Paste any text, type a natural-language instruction, and get back the transformed result instantly.

## Features

- **AI-powered transforms** — describe what you want in plain English (e.g. "sort lines alphabetically", "remove empty lines", "translate to German")
- **Multi-provider** — works with Anthropic (Claude) and OpenAI (GPT) — switch anytime in settings
- **Undo stack** — up to 50 steps back with Cmd+Z / Ctrl+Z
- **Prompt history** — recent instructions stored locally for quick reuse
- **Zero dependencies** — single HTML file, no build step, no server required
- **Privacy-first** — API keys stored only in your browser's localStorage, never sent anywhere except the AI provider

## Usage

### Option A — Open locally

Just open `index.html` in any modern browser.

### Option B — GitHub Pages

1. Fork / clone this repo
2. Go to **Settings → Pages** and set source to the `main` branch (root)
3. Access at `https://<your-username>.github.io/<repo-name>/`

## Setup

1. Click the **⚙** gear icon in the top-right
2. Choose your provider (Anthropic or OpenAI)
3. Paste in your API key
4. Select the model and click **Save**

Keys are saved in `localStorage` — they persist across sessions in the same browser.

## Supported Models

| Provider  | Models                                        |
|-----------|-----------------------------------------------|
| Anthropic | Claude 3.5 Haiku, Claude Haiku 4.5, Claude 3 Haiku |
| OpenAI    | GPT-4o Mini, GPT-3.5 Turbo, o1 Mini          |

## Security Note

API calls are made directly from your browser to the AI provider. The Anthropic integration uses the `anthropic-dangerous-direct-browser-access` header which is required for browser-based API access. **Do not share your API keys.**
