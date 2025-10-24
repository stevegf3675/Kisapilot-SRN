# Kisapilot-SRN — Staging Branch ![Branch](https://img.shields.io/badge/branch-kisapilot--staging-yellow)

**Purpose:** Burn-in / validation branch — used to test builds before they are promoted to production.

**Flow Direction:**
`kisapilot-dev → kisapilot-staging → kisapilot-main`

**Rules:**
- Protected branch
- No direct pushes
- PRs required before merge
- Used for final validation before production

See `/docs/BRANCH_RULES.md` for full policy details.


# openpilot docs

This is the source for [docs.comma.ai](https://docs.comma.ai).
The site is updated on pushes to master by this [workflow](../.github/workflows/docs.yaml).

## Development
NOTE: Those commands must be run in the root directory of openpilot, **not /docs**

**1. Install the docs dependencies**
``` bash
pip install .[docs]
```

**2. Build the new site**
``` bash
mkdocs build
```

**3. Run the new site locally**
``` bash
mkdocs serve
```

References:
* https://www.mkdocs.org/getting-started/
* https://github.com/ntno/mkdocs-terminal
