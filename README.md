# Projects Hub

Live, browsable index of every public project — demo links, code, and status badges.

**Live site:** [danieldemoz.github.io/projects-hub](https://danieldemoz.github.io/projects-hub/)

## How to add or update a project

1. Edit **`projects.json`** — one object per project.
2. Commit and push to `main`.
3. The GitHub Pages site updates automatically. **No HTML changes needed.**

### Project object fields

| Field | Description |
|-------|-------------|
| `name` | Repo / project name |
| `category` | Section heading (must match an existing category or add to `CATEGORY_ORDER` in `index.html`) |
| `description` | One-line summary |
| `tech` | Array of tech tags, e.g. `["Python", "FastAPI"]` |
| `status` | `live` · `partial` · `broken` · `none` |
| `demoUrl` | Live demo URL, or `null` if code-only |
| `repoUrl` | GitHub repo URL |

### Status badges

- **live** — demo works end-to-end
- **partial** — UI loads but backend or data incomplete
- **broken** — known issue (see Phase 1 audit notes)
- **none** — no public demo; code/README only

## Local preview

```bash
npx --yes serve .
```

Open the printed URL and load `index.html`.

## Structure

```
projects-hub/
├── index.html      # page shell + JS loader (no hardcoded cards)
├── projects.json   # single source of truth
└── README.md
```

## License

MIT — see [LICENSE](LICENSE).
