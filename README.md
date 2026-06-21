# Maxlo Launcher — update feed

Sparkle appcast + DMG releases for **Maxlo Launcher** (`io.maxlo.maxlolauncher`).

- The shipped app polls `appcast.xml` (raw) for new versions.
- DMGs are attached to GitHub Releases here (tagged `vX.Y.Z`).
- Releases are cut by `release_dmg.sh` in the `AvidLauncher` repo, which signs
  each DMG with Maxlo's Sparkle EdDSA key, uploads it, and inserts a new
  `<item>` at the top of `appcast.xml`.

Public so `raw.githubusercontent.com` serves the appcast unauthenticated.
