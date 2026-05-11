# revoked — Docs

API documentation for [revoked](https://revoked.link), built with [Scalar](https://scalar.com) and hosted on GitHub Pages.

## Live Docs

👉 [revokedlink.github.io/docs](https://revokedlink.github.io/docs)

## Structure

```
docs/
├── index.html          # Scalar docs page
├── specs/
│   ├── latest.yaml     # Always the current spec
│   ├── v1.0.0.yaml     # Versioned specs (auto-copied on release)
│   └── ...
└── versions.json       # Auto-generated versions list
```

## How Versioning Works

1. The `api` repo merges a PR into `main`
2. The release workflow bumps the version, tags it, and fires a `repository_dispatch` event
3. This repo's deploy workflow copies `specs/latest.yaml` → `specs/vX.Y.Z.yaml`
4. Scalar renders all versions with a dropdown switcher

## Updating the Spec

Edit `specs/latest.yaml` and push to `main`. The docs redeploy automatically.

## License

[Elastic License 2.0](https://www.elastic.co/licensing/elastic-license)
