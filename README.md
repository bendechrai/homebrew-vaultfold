# homebrew-vaultfold

The Homebrew tap for [vaultfold](https://vaultfold.app/), a team secrets manager that keeps encrypted vaults in git or any dumb blob store.

## Install

```
brew install bendechrai/vaultfold/vaultfold
```

This works on macOS and Linux. It installs the `vaultfold` command and `vaultfold-native-host`, the helper the browser extension talks to. Upgrade with `brew upgrade vaultfold`.

## How this repository is maintained

Do not edit it by hand. Every vaultfold release writes the cask `Casks/vaultfold.rb` here with [GoReleaser](https://goreleaser.com/), from the project's `.goreleaser.yaml`, pointing at that release's archives and their SHA-256 sums. Pre-releases never update the tap. A change made here directly is overwritten by the next release.

Until the first release this repository holds only this README.

## Signing

The binaries are not yet signed by Apple; the cask removes the quarantine attribute after install so macOS does not block them. Every release's `checksums.txt` is signed with the project's minisign key, which is the integrity guarantee. How to verify a release is in the vaultfold repository's `docs/release.md`, "Verifying a release".

## Problems

Report problems with the cask or the install in the [vaultfold repository](https://github.com/bendechrai/vaultfold/issues), not here.
