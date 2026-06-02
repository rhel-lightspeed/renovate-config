# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) configuration inherited by all repos in the `rhel-lightspeed` GitHub organization.

## Usage

Repos inherit this config automatically via Renovate's [org-level inherited config](https://docs.renovatebot.com/config-presets/#organization-level-presets). No per-repo `renovate.json` needed unless overriding specific rules.

## What's configured

**Base:** `config:best-practices` (includes `config:recommended`, Docker/GitHub Actions digest pinning, lockfile maintenance, semantic commits, and more).

**Schedule:** Weekends only (America/Chicago).

**Rules:**

- 7-day minimum release age on all updates (cooldown period)
- Auto-merge disabled globally (including GitHub-native `platformAutomerge`)
- `Signed-off-by` trailer on all Renovate commits (`:gitSignOff`)
- Python dependency updates grouped into a single PR, labeled `python`
- Git submodule references updated automatically
