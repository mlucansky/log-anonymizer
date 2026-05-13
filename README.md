# Log Anonymizer

A standalone, single-file HTML tool for anonymizing sensitive data in log files and error messages — **100% local, no data is ever sent anywhere**.

🌐 **Live demo:** [psguy.eu/log-anonymizer](https://psguy.eu/log-anonymizer.html)

---

## Features

- **Auto-detect** — automatically identifies emails, IP addresses, UUIDs, tokens, URLs, file paths and dates
- **Quick presets** — one-click rules for the most common patterns (email, IP, IP:port, path, token, UUID, date, URL)
- **Custom rules** — plain text or regex, with case sensitivity toggle and live regex preview
- **Numbered replacements** — multiple IPs become `[IP_1]`, `[IP_2]` etc. instead of all `[IP]`
- **Rule profiles** — save and reload rule sets via localStorage; export/import as JSON
- **Rule ordering** — move rules up/down to control priority (e.g. IP:PORT before IP)
- **Diff highlighting** — replaced tokens are highlighted green in the output; hover to see the original value
- **Light / Dark theme**
- **Auto language detection** — Slovak for SK browsers, English for everything else (manually switchable)
- **Responsive** — works on desktop, tablet and mobile (iOS/Android)

## Usage

Download `log-anonymizer.html` and open it in any modern browser. No server, no installation, no build step, no dependencies.

```
git clone https://github.com/mlucansky/log-anonymizer
open log-anonymizer.html
```

Or use the hosted version at [psguy.eu](https://psguy.eu/log-anonymizer.html) where you can also download the file directly from the page.

## How it works

All processing happens entirely in your browser using vanilla JavaScript. No frameworks, no build tools, no external APIs.

The only external request is loading IBM Plex fonts from Google Fonts — remove the `@import` line at the top of the `<style>` block for fully offline operation.

Storage used:
- **localStorage** — persists rule profiles between sessions
- **Clipboard API** — paste input / copy output
- **Blob API** — download anonymized text or export rules

## Privacy

No data ever leaves your browser. No analytics, no tracking, no telemetry. The tool works completely offline after the first load (fonts cached by browser).

## Rule profiles

Rules can be saved as named profiles (stored in browser localStorage) or exported/imported as `.json` files — useful for sharing rule sets between browsers or machines.

## License

MIT — see [LICENSE](LICENSE).

---

## About

Prompted and designed by [Martin Lučanský](https://psguy.eu). Code generated using [Claude](https://claude.ai) (Anthropic). All features and iterations were directed through conversation — no manual coding involved.
