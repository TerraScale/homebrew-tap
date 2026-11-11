# TerraScale Homebrew tap

```sh
brew install terrascale/tap/ts
ts --version
```

Each [ts-go CLI release](https://github.com/TerraScale/ts-go/releases) generates
`ts.rb` from its archives and SHA-256 checksums. The
[sync workflow](.github/workflows/sync.yml) runs every 15 minutes, checks that
the formula's URLs and checksums match the latest stable `sdk/go/vX.Y.Z` release, and commits
it to `Formula/ts.rb` when it differs. Each URL must carry the SHA-256 that the release's
`checksums.txt` lists for that exact archive, so a hash that belongs to another archive fails
the sync instead of a user's `brew install`. The tap pulls the formula instead of the release
pushing it, so no workflow outside this repository needs a token that can write here.
See [CLI release instructions](https://github.com/TerraScale/ts-go/blob/main/docs/cli-releases.md).
