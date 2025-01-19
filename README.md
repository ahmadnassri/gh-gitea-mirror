# gitea-mirror

bulk GitHub to Gitea mirroring

[![license][license-img]][license-url]
[![release][release-img]][release-url]

## Installation

``` shell
gh extension install ahmadnassri/gh-gitea-mirror
```

### Upgrading

``` shell
gh extension upgrade gitea-mirror
```

## Usage

``` shell
gh gitea-mirror --gitea-url http://gitea.tld --gitea-token XYZ --github-token ABC
```

> mirrors all repositories you own

``` shell
gh gitea-mirror --org myorg --gitea-url http://gitea.tld --gitea-token XYZ --github-token ABC
```

> mirrors all repositories beloning to the \$org

``` shell
gh gitea-mirror --user username --gitea-url http://gitea.tld --gitea-token XYZ --github-token ABC
```

> mirrors all PUBLIC repositories beloning to the \$user

> [!IMPORTANT]
> Make sure you specify a GitHub token with read:repo scope (classic) or contents:read (fine-grained)

### Options

      --user              GitHub username (optional)
      --org               GitHub organization (optional)
      --gitea-url         Gitea instance base URL
      --gitea-token       Gitea token (write:organization, write:repository)
      --github-token      GitHub token (read:repo or contents:read)
      --overwrite         Overwrite existing repositories (useful to replace expired tokens)

> [!WARNING]
> `--overwrite` will **DELETE** then re-create the mirror repository, this is mostly useful to replace an expired token

---

> Author: [Ahmad Nassri](https://www.ahmadnassri.com/) &

[license-url]: LICENSE
[license-img]: https://badgen.net/github/license/ahmadnassri/gh-gitea-mirror
[release-url]: https://github.com/ahmadnassri/gh-gitea-mirror/releases
[release-img]: https://badgen.net/github/release/ahmadnassri/gh-gitea-mirror
