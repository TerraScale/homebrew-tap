# TerraScale Homebrew tap

```sh
brew install terrascale/tap/ts
ts --version
```

Each stable `sdk/go/vX.Y.Z` [release of TerraScale/terrascale](https://github.com/TerraScale/terrascale/releases)
generates `ts.rb` from its archives and SHA-256 checksums. The
[sync workflow](.github/workflows/sync.yml) is scheduled every 15 minutes; in its 20 scheduled
runs from 6 to 11 November 2026, GitHub started it every 3.1 to 10.4 hours (median 5.0 hours).
It checks that the formula's URLs and checksums match the latest stable `sdk/go/vX.Y.Z` release, and commits
it to `Formula/ts.rb` when it differs. Each URL must carry the SHA-256 that the release's
`checksums.txt` lists for that exact archive, so a hash that belongs to another archive fails
the sync instead of a user's `brew install`. The tap pulls the formula instead of the release
pushing it, so no workflow outside this repository needs a token that can write here.
See the [CLI release instructions](https://github.com/TerraScale/terrascale/blob/main/sdk/go/docs/cli-releases.md).
