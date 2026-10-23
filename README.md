# TerraScale Homebrew tap

The first `ts` formula is pending an authorized CLI release. Once published:

```sh
brew install terrascale/tap/ts
ts --version
```

The [CLI release workflow](https://github.com/TerraScale/ts-go/blob/main/.github/workflows/release.yml)
generates the formula from the release archives and their SHA-256 checksums,
then commits it to `Formula/ts.rb` after the GitHub release succeeds.

The repository owner installs a token limited to writing this tap from the
following command's hidden prompt:

```sh
gh secret set HOMEBREW_TAP_TOKEN --repo TerraScale/ts-go
```

Do not pass the token in command arguments, pipe it, or share it in chat.
The next authorized `v0.0.X` tag in `ts-go` publishes the formula automatically.
See [CLI release instructions](https://github.com/TerraScale/ts-go/blob/main/docs/cli-releases.md).
