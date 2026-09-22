# Agent Skills PR preview

This separate GitHub Pages site hosts the latest manually requested, commit-pinned preview of an open [agent-skills pull request](https://github.com/stark-ai-de/agent-skills/pulls).

- [Open the latest preview](https://stark-ai-de.github.io/agent-skills-preview/).
- [Preview source receipt](https://stark-ai-de.github.io/agent-skills-preview/preview.json).
- [Production catalog](https://stark-ai-de.github.io/agent-skills/) remains separate.

The workflow is maintained in [the source repository](https://github.com/stark-ai-de/agent-skills/blob/642fe8f51e1156d2d6d984e4c6e44cb6a459cb31/.github/workflows/pages-preview.yml). Copy reviewed workflow updates here without modification. [Operator instructions](https://github.com/stark-ai-de/agent-skills/blob/642fe8f51e1156d2d6d984e4c6e44cb6a459cb31/docs/github-pages-previews.md) describe manual refresh and validation.

Dispatch `pages-preview.yml` on `main` with `pr` and its exact current `source_sha`. Only open same-repository PRs are accepted. Builds have read-only permissions; a separate job publishes static artifacts through the protected `github-pages` environment. No deployment credentials from the source repository are needed.

One snapshot is retained at a time. Another deployment replaces it; PR pushes and closure do not automatically refresh or remove it. Preview pages identify their PR/commit and request no indexing. This does not merge a PR, promote a skill or publish packages.
