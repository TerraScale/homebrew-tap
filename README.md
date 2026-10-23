# TerraScale Homebrew tap

```sh
brew install terrascale/tap/ts
ts --version
```

Each [ts-go CLI release](https://github.com/TerraScale/ts-go/releases) generates
`ts.rb` from its archives and SHA-256 checksums. The
[sync workflow](.github/workflows/sync.yml) runs every 15 minutes, checks that
the formula's URLs and checksums match the latest `v0.0.X` release, and commits
it to `Formula/ts.rb`. It needs no token beyond this repository's own.
See [CLI release instructions](https://github.com/TerraScale/ts-go/blob/main/docs/cli-releases.md).
