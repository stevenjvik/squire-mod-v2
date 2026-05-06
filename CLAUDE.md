# squire-mod-v2 — Claude memory

## What this repo is

A Minecolonies-addon companion mod for Minecraft NeoForge 1.21.1. The mod adds an FSM-driven "squire" entity that fights, mines, chops, farms, and manages its own inventory.

**Off-brand for SJVIK Labs.** This is a personal hobby project on the `stevenjvik` account. Steve's most-released repo (22+ tags). Strong solo-dev portfolio signal.

## Stack

- **Game:** Minecraft 1.21.1
- **Mod loader:** NeoForge
- **Language:** Java
- **Build:** Gradle (with NeoForge MDK)
- **Animations:** Geckolib
- **Compatibility target:** Minecolonies addon contract

## Common commands

```bash
./gradlew build              # Compile + package the mod
./gradlew runClient          # Launch Minecraft with the mod loaded (testing)
./gradlew runServer          # Launch a dedicated server with the mod
./gradlew runData            # Generate datapack assets
./gradlew clean              # Clear build artifacts
```

The `deploy.sh` script in the repo root handles release packaging.

## Conventions

- **Branch:** `main`
- **Versioning:** semver, tagged `v<major>.<minor>.<patch>`
- **Releases:** tagged + GitHub Release with the built `.jar` attached
- **FSM state machines** for the squire's behavior — keep state transitions explicit
- **Conventional Commits** (`feat:`, `fix:`, `docs:`, `chore:`)
- **Lite REPO-STANDARD tier** per §7.8 (personal account, hobbyist signal is fine)

## Conventions specific to mod dev

- Don't bump the Minecraft version target without a planned compatibility branch
- NeoForge mappings change between minor versions — pin in `gradle.properties`
- Geckolib animation files live under `src/main/resources/assets/<modid>/animations/`

## Cross-repo

- Personal MineColonies KubeJS work: `stevenjvik/mc-toolkit`
- Personal profile: `stevenjvik/stevenjvik`

## Standard

Per [SJVIK Labs Repo Standard](https://github.com/sjviklabs/.github) §7.8 (lite tier for personal account):
- **Status:** Stable
- License: MIT
- Branch protection on `main` (no force-push, no deletion)
- Dependabot + secret scanning + push protection enabled
