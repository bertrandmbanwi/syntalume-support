<!-- Synced from the private Syntalume source repo. Run `npm run docs:sync` before every release. -->

# Getting Started

## Trial and subscription

New users and existing Auralis/Syntalume users receive 30 full days starting when
the in-editor notice is first presented. Closing it does not end that period. No payment details are required. After
that, an annual subscription is required: $9 for 1 activation, $12 for 3, or $20
for 6, plus applicable tax. Checkout charges immediately and renews yearly until
canceled. It does not add a second trial.

An activation is an editor installation; multiple editors or remote hosts may
use separate slots. Theme and Companion share one slot within the same JetBrains
IDE. Activate via **Syntalume: Activate License** in VS Code-compatible editors,
or **Tools → Syntalume License** in JetBrains. Recover keys, deactivate old
installations and cancel renewal in the [customer portal](https://polar.sh/syntalume/portal).

Paid licenses require online activation and periodic validation after consent.
Temporary connection or service failures retain previously verified access for
up to 72 hours, never beyond the known license expiry. When grace ends while
verification is unavailable, interactive and background features pause but the
selected appearance remains. Confirmed expiration or
revocation stops licensed features. Appearance replaced during enforcement is
restored when access returns only if you have not changed it yourself. Browser-only hosts such as
vscode.dev/github.dev are not supported by this paid release. Read the
[licensing details](https://syntalume.dev/legal/licensing) and
[30-day first-purchase refund policy](https://syntalume.dev/legal/refunds).

Native remote hosts connected to the same VS Code UI installation share the
local 30-day period; existing host-specific periods use the earliest known
dates. Paid activation slots remain separate per installation. This is not a
universal account-level trial across different machines or editor products.

## VS Code Marketplace

1. Open VS Code.
2. Open Extensions.
3. Search for `Syntalume — Adaptive Themes & Icons`.
4. Install the extension with ID `auralis-labs.auralis-theme-system`.

Canonical listing:

- https://marketplace.visualstudio.com/items?itemName=auralis-labs.auralis-theme-system

The publisher ID and extension ID are the durable identity. Use them to avoid
confusing Syntalume with similarly named extensions.

## Open VSX and VS Code-compatible editors

Syntalume is also published under the same publisher and extension IDs on Open
VSX:

- https://open-vsx.org/extension/auralis-labs/auralis-theme-system

Use that listing for editors whose built-in extension browser uses Open VSX.
The release workflow verifies the canonical registry version after publishing;
search-engine result pages are not used as release evidence.

## JetBrains IDEs

The public, approved Syntalume Theme listing for JetBrains IDEs is:

- https://plugins.jetbrains.com/plugin/32762-auralis-theme

The standalone theme plugin carries all nine palettes, editor schemes,
Islands-aware surfaces, and Syntalume icon substitutions with its own small licensing runtime. It does not require Companion. Syntalume Companion is a separate optional plugin
for shared profiles, project identity, Rhythm, and Environment Guard; keeping
the two products separate means users who want only a theme install only a
theme. Companion’s shared-profile review can also apply supported comfort, syntax,
bracket, and density choices through a separately owned editor scheme; every
change is previewed first, and unsupported Look and Feel fields are identified
without approximation.

## Local VSIX

```bash
npm run package
code --install-extension auralis-theme-system-*.vsix --force
```

Reload VS Code after installing a local package.

## Installation Is Non-Intrusive

Installing Syntalume does not automatically apply a theme or profile. The first-run notice starts your 30-day period; closing it preserves the remaining time. If access later expires, selected Syntalume appearance can fall back to editor defaults, with your selection retained for safe restoration after reactivation. To apply it, run:

```text
Syntalume: Apply Recommended Experience
```

or use the walkthrough buttons or the Setup Dashboard. Every write is a normal,
visible VS Code setting. Ownership-aware surfaces such as Complete Experience,
tooling, theme/icon commands, Tune, Icon Studio, project/accent customization,
and Syntalume Type restore only their unchanged writes or individually owned
object keys; later manual edits and unrelated additions win.

## First Setup

After Marketplace install, VS Code opens the Syntalume Getting Started walkthrough. Run:

```text
Syntalume: Open Setup Dashboard
```

for the guided first run. The dashboard shows whether the color theme, file icons, product icons, formatter settings, companion extensions, and old settings are in a healthy state.

You can also run:

```text
Syntalume: Apply Recommended Experience
```

for the fastest first run. It applies Syntalume Botanica, file icons, product icons, bracket guides, semantic highlighting, and the balanced infrastructure profile.

To pick a different profile, run:

```text
Syntalume: Apply Complete Experience
```

Choose the profile closest to how you work. Syntalume applies the color theme, file icons, product icons, bracket guides, minimap behavior, semantic highlighting, and optional ambience settings together.

For infrastructure projects, also run:

```text
Syntalume: Setup Terraform Tooling
Syntalume: Setup YAML and Kubernetes Tooling
Syntalume: Run Doctor (Check Setup)
```

These commands write normal VS Code settings and offer companion extensions. They do not bundle Terraform, TFLint, Prettier, ESLint, or the Red Hat YAML language server.
