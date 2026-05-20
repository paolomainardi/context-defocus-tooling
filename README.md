# defocus.tools

A reference catalogue of open-source tools that address token waste and context degradation in AI coding agents. Organized by failure mode. Filtered and sorted by community metrics.

**Live site:** https://paolomainardi.github.io/context-defocus-tooling/

## Disclaimer

This catalogue is vibe-coded — built with AI assistance, curated by intuition, not rigorously verified. Tool descriptions, observations, and metrics are best-effort and may contain errors. No warranties, no guarantees of accuracy, no endorsements, no affiliation with any listed project. Do your own due diligence before adopting anything here. If something is wrong, open a PR.

## Contributing

### Adding a tool

1. Fork the repo
2. Edit `tools.json` — append a new entry to the array
3. Open a PR

Each tool entry requires these fields:

```json
{
  "id": "unique-kebab-id",
  "name": "Display Name",
  "vendor": "owner/repo",
  "url": "https://github.com/owner/repo",
  "failure": "1",
  "failureLabel": "FAIL MODE 01",
  "tagline": "One-paragraph description of what it does and how.",
  "meta": {
    "License": "MIT",
    "Distribution": "npm · pip",
    "...": "other key-value pairs shown on the card"
  },
  "maintainer": "solo|team|vendor",
  "language": "Rust|Python|TypeScript|Go|Shell|Markdown",
  "license": "MIT|Apache-2.0|BSD|Custom",
  "indepEval": false,
  "compactDesc": "Short one-line description for compact view",
  "observations": [
    "Factual observation with source attribution.",
    "Another observation."
  ],
  "stars": 100,
  "lastRelease": "2026-05"
}
```

**Notes:**

- `stars` and `lastRelease` are seed values — the daily GitHub Action overwrites them with live data once your PR is merged.
- `maintainer`: `"solo"` (single author), `"team"` (multiple substantive contributors), `"vendor"` (commercial entity). This is editorial judgment.
- `failure`: which failure mode the tool targets. Values: `"1"` through `"5"`, `"x"` for cross-cutting. Use `"1+3"` for tools spanning multiple modes.
- `indepEval`: set to `true` only if a third party (not the tool's author) has measured its claims.
- `observations`: must be factual, sourced, written in third person. No recommendations, no opinions.

### Updating an existing tool

Same process — edit the relevant entry in `tools.json` and open a PR.

### What NOT to edit

- `metrics.json` — auto-generated daily by GitHub Actions. Manual edits will be overwritten.
- `index.html` — only for UI/logic changes, not for adding tools.

## License

MIT. See [LICENSE](LICENSE).
