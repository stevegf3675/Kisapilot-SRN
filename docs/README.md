# Kisapilot-SRN — Development Branch ![Branch](https://img.shields.io/badge/branch-kisapilot--dev-orange)

**Purpose:** Active development branch — where new code is created and tested before promotion to staging.

**Flow Direction:**
`kisapilot-dev → kisapilot-staging → kisapilot-main`

**Rules:**
- No branch protection (direct commits allowed)
- Optional: enable linear history enforcement if desired
- Safe area for experimentation

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
