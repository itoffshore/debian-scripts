`gnupg2` backports for Debian Jessie
---

These scripts will allow you to use `ed25519 Eliptic Curve Cryptography` keys in `gnupg`.

* Build in numerical package order.

Backporting `libgcrypt` is optional (`ed25519` keys will work with the current `libgcrypt 1.6.3` in Debian Jessie). If you do backport `libgcrypt 1.6.4+` & you use `skype` on `64bit` you will need to build both `64 & 32bit libgcrypt` libraries & configure a local repo so `32 & 64bit` libs can be installed simultaneously.

* Generate an `ed25519` key with:

`gpg2 --expert --full-gen-key`

* & select

`A`
`Q`
`1`
`Y`
