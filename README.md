# agent-scaffold-templates

This repository stores versioned project templates consumed by the [`agent-scaffold`](../agent-scaffold) CLI. Templates are plain files with small JSON manifests, so they can be reviewed and released independently from the npm package.

## Repository layout

```text
.
├── templates.json
├── schemas/
│   ├── template.schema.json
│   └── templates.schema.json
└── templates/
    ├── general/
    │   ├── template.json
    │   ├── AGENTS.md
    │   ├── README.md
    │   └── docs/
    └── game/
        ├── template.json
        ├── AGENTS.md
        ├── README.md
        └── docs/
```

## Available templates

- `general`: a general-purpose, documentation-first agent project.
- `game`: an engine-agnostic game project with gameplay, content, playtest, performance, save compatibility, and release guidance.

`templates.json` is the public index. Each entry points to a template manifest. A manifest lists every file the CLI may download; unlisted files are never scaffolded.

## Template variables

V1 supports one token in text files:

```text
{{PROJECT_NAME}}
```

The CLI replaces it with the destination directory name.

## Adding a template

1. Create `templates/<name>/template.json` and the template files.
2. Add the template to `templates.json`.
3. Validate JSON and run the CLI repository's smoke tests.
4. Release the repository with a semantic tag such as `v1.1.0`.

Paths in manifests must use forward slashes, be relative, and must not contain `.` or `..` segments. Every scaffolded file must be listed explicitly.

## Versioning

- Use `main` for the latest development version.
- Create immutable semantic tags for stable releases.
- Treat removing a template, removing a file, or changing an established file contract as a breaking change.

Consumers can pin a release:

```bash
npx @huylaez/agent-scaffold my-project --template general --template-version v1.0.0
```

## Local verification

From the sibling `agent-scaffold` project:

```bash
npm install
npm run verify
```

The smoke test serves this repository locally and runs the built CLI end to end.
