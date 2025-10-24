# Kisapilot Branch Protection Rules

This document defines the protection rules and branch flow for the **Kisapilot-SRN** repository.

---

## 🔁 Branch Flow
```
dev → kisapilot-staging → kisapilot-main
```

- **dev** — Development sandbox (direct commits allowed)
- **kisapilot-staging** — Test/Burn-in branch before production
- **kisapilot-main** — Production / release branch

---

## 🛡️ Branch Rules

### kisapilot-main
- Require Pull Request before merging (approvals = 0)
- Require conversation resolution before merging
- Require linear history
- Restrict deletions
- Block force pushes
- Direct pushes not allowed
- No status checks required (yet)
- CI checks can be added later under “Required status checks”

### kisapilot-staging
- Require Pull Request before merging (approvals = 0)
- Require linear history
- Restrict deletions
- Block force pushes
- Direct pushes not allowed

### dev
- No protection (direct push allowed)
- Optional: enable “require linear history” if desired

---

## ⚙️ Notes
- These rules are defined as **Rulesets** in GitHub → Settings → Rules.
- GitHub only enforces them for **Team/Enterprise accounts**; on personal repos, they serve as documentation and can be recreated instantly if you upgrade.
- Future addition: Enable `Required status checks` when CI/testing is configured.

---

_Last updated: 2025-10-24_
