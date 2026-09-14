# Blip Social

White-labeled build of **OpenPost** for the Blip Media newsroom, served at
https://social.gdgt.link.

- **License:** AGPL-3.0 (see `LICENSE`) — copyright of the original project
  remains with its authors; this repository is a branded derivative.
- **Upstream:** https://github.com/getopenpost/openpost (pinned at tag `v4.31.0`
  for this branding pass).
- **Changes vs upstream:** brand assets in `assets/brand/` (Blip Social logo,
  lockups, PWA icons), product name in `apps/web/src/lib/pwa/manifest.ts`,
  `apps/web/src/routes/+layout.svelte`, `apps/web/src/lib/components/`,
  and the app copy in `apps/web/messages/*.json`. No functional changes.

## Source availability (AGPL §13)

This modified source is published here for anyone using the instance at
https://social.gdgt.link. Rebuild image tag: `blip-social:v4.31.0-gp1`.

## Rebranding an upgrade

When upstream ships a new tag: merge/pull upstream, then re-apply branding —
the touch list above is stable and small. Commits are prefixed `brand:` to
make them easy to cherry-pick.