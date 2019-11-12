# Compiled Vault UI

Merely compiled committed to git. In vault repo, checkout the tag for the
appropriate release, then run:

```
# ensure npm version 10 is installed
pkg install -y npm-node10 yarn-node10
# ignore errors here
env GOPATH=${PWD} PATH=${PWD}/bin:${PATH} gmake bootstrap dev-ui
env GOPATH=${PWD} PATH=${PWD}/bin:${PATH} gmake static-assets static-dist
```

Then copy `http/bindata_assetfs.go` to this repo.

See also [Developing
Vault](https://github.com/hashicorp/vault/#developing-vault) and [Ticket on
building UI](https://github.com/hashicorp/vault/issues/4295)
