<!-- Synced from the private Syntalume source repo. Run `npm run docs:sync` before every release. -->

# Troubleshooting

## License verification is temporarily unavailable

Run **Syntalume: Show License Status** to distinguish a temporary verification
problem from an expired or revoked license. Check connectivity and the system
clock. Do not delete local state or repeatedly activate the same key to repair
a connection problem; an interrupted activation may need portal reconciliation.

A previously verified paid license can keep working for up to 72 hours from
its last successful check during temporary failures, never beyond the known
license expiry. Reconnect before that deadline. An unverified key cannot use
this grace. Confirmed revocation is enforced without it.

Closing the first-run notice does not cancel the 30-day editor period. Storage
contention or clock problems should be reported as unavailable verification,
not as proof that the trial ended. Retry after fixing the clock or storage
problem. Do not reset the system clock to extend access.

If license enforcement replaced Syntalume appearance, access recovery restores
those saved selections only while the fallback remains unchanged. Any manual
appearance choice you made afterward takes precedence. Recover your key or
manage activations in the [customer portal](https://polar.sh/syntalume/portal).
Never include license keys in a public support issue.

## I installed Syntalume but do not see the themes

Run:

```text
Preferences: Color Theme
```

Search for `Syntalume`.

## Icons did not change

Run:

```text
Syntalume: Sync Icons With Active Theme
```

Then reload VS Code if the Extensions view asks for it.

If you used desktop Icon Studio, confirm `Syntalume Icons – Studio (Desktop)` is
the active file-icon theme. Apply switches through a shipped Syntalume theme and
back automatically so Explorer reloads the generated manifest. If Apply reports
that the installation is read-only, reinstall Syntalume in your normal User
extensions location; no settings are changed by the failed attempt.

Browser-only hosts such as vscode.dev are not supported by this paid release;
use a native desktop editor for the trial and activation. In older browser
builds, choose Balanced, Minimal, Outline, or
Pictorial. Arbitrary slider values and custom folder/root/language maps remain
read-only preset previews there because browser extensions cannot update their
packaged contribution files.

## Accessibility Lab cannot read the active theme

Run `Preferences: Color Theme`, select the theme again, and retry:

```text
Syntalume: Open Accessibility Lab
```

Some installed themes do not expose a readable JSON contribution to other
extensions. Syntalume shows a warning and makes no changes when the active theme
cannot be inspected.

## I want one place to check my setup

Run:

```text
Syntalume: Open Setup Dashboard
```

It reports the active theme, icon themes, git decoration visibility (the M/A/U letters and colors next to changed files), formatter settings, companion extensions, and optional ambience settings.

## The git letters (M, A, U) next to changed files are missing

Those letters and file colors come from VS Code's explorer decorations, and Syntalume themes color them in every variant. If they are missing, a past setting turned them off. Run `Syntalume: Run Doctor (Check Setup)` to confirm, or set these back to true:

```json
{
  "explorer.decorations.badges": true,
  "explorer.decorations.colors": true,
  "git.decorations.enabled": true
}
```

Applying any Syntalume Complete Experience profile also restores them.

## Blame Ghosts does not show anything

Check that:

- The workspace is trusted.
- The file is saved and not dirty.
- The file is inside a local git repository.
- `git` is available on your PATH.
- `auralis.blameGhosts.enabled` is true.

## A profile changed too many editor settings

Profiles write normal VS Code settings. Open Settings JSON and adjust the settings you do not want. To stop profiles from toggling ambience:

```json
{
  "auralis.profiles.includeAmbience": false
}
```

## General Reset says its reset history is damaged

Syntalume preserves every current editor setting and clears only its local reset
metadata, so the next Syntalume apply starts from the setup you can see. If that
metadata cleanup fails, retry General Reset before applying more Syntalume
changes.

## Images are broken on Marketplace

Marketplace images must be public HTTPS URLs. Syntalume uses a public asset repository for screenshots while keeping the source repository private.

Public support issues live at:

```text
https://github.com/syntalume/syntalume-support/issues
```

For a shareable support payload that excludes file paths, project names, source
code, and environment context names, run:

```text
Syntalume: Copy Support Diagnostics
```
