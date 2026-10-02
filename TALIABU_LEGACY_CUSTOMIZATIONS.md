# Taliabu TV3 Legacy customization layer

Base: q215613905/TVBoxOS at `ab11d289e09963a9daf65ca7f6b7a9a8cbe184e1`.

This branch is the old-device edition. Its compatibility baseline must remain intact.

## Required Taliabu customizations

- App name: `塔岛电视3`
- Dedicated application ID: `com.taliabu.tv3.legacy`
- Default API / live API on first launch: `https://tvsource.taliabu.kdns.fr`
- Taliabu launcher icon and TV banner
- Pure black application background
- `REQUEST_INSTALL_PACKAGES` permission removed
- No Taliabu self-update mechanism is added; q215 upstream currently has no built-in self-updater

## Compatibility rules

- Keep q215's Android 4.4 / API 19 Java flavors.
- Keep the API 21 minimum only where q215 already requires it for 64-bit flavors.
- Do not migrate this branch to FongMi libraries, Java 21, or modern SDK requirements.
- Do not replace the q215 player stack merely to match the main Taliabu edition.

## Upstream sync rule

Keep `main` as a clean q215 upstream mirror. Rebase or recreate `taliabu-legacy` from the newest clean `main`, then reapply only the Taliabu commits and run the legacy GitHub Actions build.
