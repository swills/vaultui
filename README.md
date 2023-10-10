# Compiled Vault UI

Merely compiled committed to git. In vault repo, checkout the tag for the
appropriate release, then run:

```
# ensure npm version 18 is installed
pkg install -y npm-node18 yarn-node18
# ignore errors here
export GOPATH=$(mktemp -d)
export PATH=${PATH}:${GOPATH}/bin
mkdir -p pkg/web_ui
gmake bootstrap
gmake static-dist
gmake dev-ui
```
Note: the static-dist can take 18 minutes or more

Then copy `http/web_ui` to this repo.

See also [Developing
Vault](https://github.com/hashicorp/vault/#developing-vault) and [Ticket on
building UI](https://github.com/hashicorp/vault/issues/4295)
