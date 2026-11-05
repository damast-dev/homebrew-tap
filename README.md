# damast-dev/homebrew-tap

Homebrew formulae for [Damast](https://damast.dev) tools.

```sh
brew install damast-dev/tap/mast
```

| Formula | What it is |
|---------|------------|
| [`mast`](Formula/mast.rb) | [mast](https://github.com/damast-dev/mast), the command line for Damast. A drop-in for `fj` (forgejo-cli): same commands, shared logins. Prebuilt binaries for macOS (Apple silicon, Intel) and Linux (x86_64, aarch64). |

`brew upgrade mast` picks up new releases.

## How it is updated

Don't edit `Formula/mast.rb` by hand. On every final mast release, [`release.yml`](https://github.com/damast-dev/mast/blob/main/.github/workflows/release.yml) in damast-dev/mast generates the formula with [`formula.sh`](https://github.com/damast-dev/mast/blob/main/.github/scripts/formula.sh) (version, URLs, sha256 from the release's `SHA256SUMS`), runs `brew style`, `brew audit --strict`, `brew install` and `brew test` on it, and pushes it here. Release candidates are not published here.
