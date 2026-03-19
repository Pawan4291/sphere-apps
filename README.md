<p align="center">
  <img src="sphere.svg" width="96" alt="Sphere" />
</p>

# Sphere Apps

Community-curated directory of apps for [Unicity Sphere](https://github.com/unicity-sphere/sphere). Apps listed in `apps.json` appear automatically in the Sphere desktop.

## Adding Your App

1. Fork this repo
2. Add your app to the `apps` array in `apps.json`
3. Open a pull request

### Entry Format

```json
{
  "category": "games",
  "name": "My App",
  "description": "Short description shown on hover",
  "url": "https://example.com",
  "icon": "https://example.com/logo.png"
}
```

| Field | Required | Description |
|-------|----------|-------------|
| `category` | Yes | Category for grouping in the Sphere desktop (see below) |
| `name` | Yes | Display name |
| `description` | No | Short description shown as tooltip on hover |
| `url` | Yes | HTTPS URL of your app |
| `icon` | No | URL to a square icon image (PNG or SVG recommended, min 128x128px) |
| `hidden` | No | Set to `true` to hide the app from the Sphere desktop (default: `false`) |

### Categories

Use an existing category when possible:

- `games` — Games and entertainment
- `dev` — Developer tools, examples, and SDKs
- `defi` — DeFi, exchanges, and financial apps
- `social` — Social and communication apps
- `tools` — Utilities and productivity

Need a new category? Propose it in your PR.

### Guidelines

- App must be accessible over HTTPS
- Icon should be square with a transparent or solid background
- Keep the `apps` array sorted alphabetically by category, then by name
- One app per PR makes review easier
- For Sphere wallet integration, use [`@unicitylabs/sphere-sdk/connect`](https://github.com/unicity-sphere/sphere-sdk)
