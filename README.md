# renovate-config

🧹 Shared [Renovate](https://docs.renovatebot.com/) preset for my projects.

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>LECOQQ/renovate-config"]
}
```

What it does:

- `chore(deps): …` commits, no body;
- runs between 1:00 and 4:00, Paris time, on releases at least three days old;
- one pull request per ecosystem for non-major updates, one per major update;
- Node.js and pnpm move as one exact version across `.nvmrc`, `engines`, CI and Dockerfiles;
- development dependencies merge themselves, by rebase, once CI passes (0.x excluded); everything else waits for review;
- known vulnerabilities get their own pull requests.

Repositories on GitHub add `github>LECOQQ/renovate-config:github`, which lifts the night-only schedule.

This repository is a read-only copy: changes are made upstream and pull requests are not merged here.
