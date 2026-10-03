<!-- Synced from the private Syntalume source repo. Run `npm run docs:sync` before every release. -->

# Security Policy

## Supported Versions

Security fixes are handled for the current Marketplace release of Syntalume.

## Reporting A Vulnerability

Do not open a public issue for suspected vulnerabilities. Contact `support@syntalume.dev` privately. Syntalume is operated by Mbanwi Ventures LLC.

Please include:

- Affected Syntalume version.
- VS Code version and operating system.
- Steps to reproduce.
- Whether a Syntalume optional ambience feature was enabled.
- Any relevant logs that do not contain secrets.

## Security Model

Syntalume is designed to keep the default theme path low risk:

- Color themes, file icons, and product icons are declarative VS Code contributions.
- The small runtime activates only after the workbench finishes starting
  (`onStartupFinished`); declarative themes and icons do not wait for it, and
  bounded performance checks gate every release.
- The extension does not include telemetry.
- The paid release uses Polar for license activation and periodic background
  validation after the user consents during activation. Requests send the
  license key, organization identifier, random installation label and, where
  applicable, activation identifier. They never include workspace contents,
  paths, filenames, editor settings or diagnostics. See [Privacy](PRIVACY.md).
- Optional ambience features run only after a Syntalume command/profile enables them.
- Optional usage counters store only fixed aggregate counts in VS Code local
  extension storage. Users can disable and clear them; they are never sent.
- Diagnostics and feedback are user-initiated, sanitized previews. Syntalume
  never submits a report or opens a review prompt automatically.
- The paid release supports native desktop and supported remote extension
  hosts. Browser-only hosts such as vscode.dev/github.dev are not supported.
- `Syntalume: Toggle Blame Ghosts` is disabled in untrusted or virtual workspaces and uses local `git blame` through `execFile`, never through shell string execution.
- New and existing users receive a locally recorded 30-day period from the
  first presentation of the in-editor notice, with no payment details or
  network request required. Closing the notice does not end that period.
- Temporary provider or connection failures do not mean revocation. Previously
  verified paid access has a bounded 72-hour grace period, never beyond the
  known license expiry. After grace ends, unavailable verification pauses
  licensed operations without replacing the selected appearance. Confirmed
  revocation is enforced without that grace.
- License keys and cached verification records use editor secret storage.
  This does not make downloaded themes copy-proof or prevent deliberate
  tampering with local trial records.

## User Guidance

- Use the official `auralis-labs.auralis-theme-system` listing on Visual Studio
  Marketplace or Open VSX, or the Syntalume Theme/Companion listings on
  JetBrains Marketplace linked from https://syntalume.dev.
- Keep VS Code and Syntalume updated.
- Use the public support hub for non-sensitive bugs and docs issues: `https://github.com/syntalume/syntalume-support`.
- Review any extension claiming to be a Syntalume fork or modified build carefully.
