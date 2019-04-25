# Compiled Vault UI

Merely compiled committed to git. In vault repo, checkout the tag for the
appropriate release, then run:

```
env GOPATH=${PWD} PATH=${PWD}/bin:${PATH} gmake bootstrap static-assets static-dist
```

Then copy `http/bindata_assetfs.go` to this repo.

See also [Developing
Vault](https://github.com/hashicorp/vault/#developing-vault) and [Ticket on
building UI](https://github.com/hashicorp/vault/issues/4295)
