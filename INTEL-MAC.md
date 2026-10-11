# Automatic Intel Mac builds

This public fork checks HakanSeven12/OpenCADStudio main daily at 04:23 UTC
and builds the latest commit when its source or this build configuration changes.
Manual builds are available in Actions → Intel Mac — clean upstream → Run workflow.

Download the DMG and SHA-256 checksum from this fork's Releases page.
The standard macos-15-intel runner is free for public repositories; no paid
larger runner or Apple Developer subscription is used.

The fork's main branch holds the build configuration. Every build checks out
the current upstream commit separately and builds x86_64-apple-darwin without
any source or icon modifications. An external packaging driver creates the
Intel app bundle and DMG. Release notes identify the upstream and configuration
commits. The previous successful release remains available if a new build fails.

Lumen assets and its patch are preserved but NOT applied. The former Lumen
workflow is archived at intel-ci/upstream-workflows/intel-lumen.yml and does
not run. Clean releases have tags starting with upstream-intel-.

The app includes its launcher, Python plugin, QuickLook extension and document
icons. It is ad-hoc signed, not Apple-notarized. macOS may require approval in
Privacy & Security on first launch. Never disable Gatekeeper globally.
Build and MCP handshake are checked on macOS 15 Intel. Deployment target is
macOS 11, but compatibility with older systems is not established by this CI.

Only the Intel workflow is active in this fork. Original upstream workflows
are preserved under intel-ci/upstream-workflows for reference.

GitHub may delay scheduled jobs and disables scheduled workflows after 60 days
of repository inactivity. If that happens, re-enable this workflow in Actions.
Publishing releases is not relied upon to prevent this inactivity rule.
