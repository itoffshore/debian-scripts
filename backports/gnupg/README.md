Build in numerical package order.

Backporting `libgcrypt` is optional (`ed25519` keys will work with the current `libgcrypt 1.6.3` in Debian Jessie). If you do backport `libgcrypt 1.6.4+` & you use `skype` on `64bit` you will need to build both `64 & 32bit` libraries & configure a local repo so `32 & 64bit` libs can be installed simultaneously.
