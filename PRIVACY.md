<!-- Synced from the private Syntalume source repo. Run `npm run docs:sync` before every release. -->

# Privacy

Syntalume is local-first. Themes and icons load as editor assets, and the
optional runtime does not collect or transmit telemetry.

## Operator and data practices

Syntalume is a DBA of Mbanwi Ventures LLC. Contact support@syntalume.dev for
privacy questions, access, correction or deletion requests. Do not send license
keys or payment-card details in support messages.

No source code, filenames, workspace paths, repository names, environment labels,
editor settings or diagnostics are uploaded for licensing. There is no analytics
SDK, advertising tracker, automatic crash reporter or passive feedback submission.

## License verification

New and existing users receive 30 days from the first presentation of the in-editor
notice. The trial is local and requires no payment details or network request.
Paid licenses require activation and periodic online validation with Polar at
`https://api.polar.sh/v1/customer-portal/license-keys/`.

Activation sends your license key, Syntalume's Polar organization identifier and
a random installation label. Validation and deactivation also use Polar's
activation identifier. Polar receives ordinary connection information such as
an IP address. Validation occurs in the background while a paid key is stored. A secure local
record of successful verification permits up to 72 hours of access during
temporary connection or service failures, never beyond the known license
expiry. Confirmed expiration or revocation stops licensed features. Appearance
selections replaced during enforcement are retained for safe restoration when
access returns; later manual changes take precedence. Source files are not modified.

Keys and activation records use VS Code SecretStorage or the JetBrains password
store. Protection depends on the editor, operating system and selected backend.
A local trial record and secure-store backup retain the start, expiry and last
observed time. Cached paid verification retains the verified license and
activation identity, verification time and expiry; it contains no project data. Local lock/intent files contain random coordination identifiers,
not keys. Remote native VS Code hosts use a durable random installation scope.
Theme and Companion share one license within the same JetBrains IDE.

Polar hosts checkout, authentication, receipts, license delivery and the customer
portal. Mbanwi Ventures LLC can access customer, order, subscription and license
information needed for fulfillment and support. See [Polar's Privacy Policy](https://polar.sh/legal/privacy-policy).
Financial records may need to be retained for legal and accounting obligations.
Syntalume's static website does not collect card details, login codes or keys.
Local records remain until removed through editor/storage controls. Uninstalling
is not cancellation; manage renewal and activations in the [customer portal](https://polar.sh/syntalume/portal).

Native remote hosts connected to the same VS Code UI installation share the
local 30-day period; existing host-specific periods use the earliest known
dates. Paid activation slots remain separate per installation. This is not a
universal account-level trial across different machines or editor products.

## Local data

Syntalume may keep the following data in the editor's extension storage, within
the editor installation and its configured storage:

- Settings and exact-reset ownership records for features you explicitly
  apply, including a local sequence of Syntalume setting changes used only to
  unwind interleaved features during General Reset.
- Draft Icon Studio presets and saved Tune/profile choices.
- Your license and trial records described above. Older signed keys are verified locally.
- Two optional aggregate counters: Tune applies and shared-profile applies.
- The optional JetBrains Companion stores its local choices and exact-reset
  ownership in JetBrains application/project metadata. It does not edit source
  files or transmit that metadata.

The counters contain no timestamps, project or workspace identifiers, paths,
labels, or setting values. They are never transmitted. You can disable and
clear them from the Setup Dashboard, and `Syntalume: Reset Syntalume Settings`
clears Syntalume-owned runtime state.

Edit Heatmap data stays in memory for the current session. Environment Guard
derives a severity locally from the active Git branch, Kubernetes context, and
Terraform workspace marker in `.terraform/environment`, but stores only bounded
configuration and a short-lived hash
for a signal-specific snooze—not the raw label.

## Local tools and files

- Blame Ghosts invokes local `git blame` only when enabled, in a trusted local
  workspace, after cursor movement settles.
- Doctor checks only whether documented optional command-line tools are
  available; it does not run them against source files.
- Export, profile, accessibility, and port commands write only to a location
  you choose or to Syntalume-owned editor settings.
- On desktop, applying arbitrary Icon Studio controls regenerates only the
  packaged `auralis-icons-studio` manifest and its extension-owned SVG copies;
  it never writes into a project. Native hosts use their own writable extension storage.
- Browser-only extension hosts such as vscode.dev/github.dev are outside the paid release. Native remote hosts require persistent writable storage.

## User-initiated links and feedback

Syntalume never submits feedback or opens a review prompt automatically. When you
choose a support, review, font, Marketplace, or companion-extension action, it
shows the relevant destination or payload first and then asks the editor to
open that link in your browser. Any information you submit is governed by the
destination's privacy terms.

## Questions

For privacy questions that do not contain sensitive information, use the
[public Syntalume support hub](https://github.com/syntalume/syntalume-support).
Report suspected security vulnerabilities through the private publisher
contact path described in [SECURITY.md](SECURITY.md).
