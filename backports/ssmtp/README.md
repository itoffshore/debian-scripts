`ssmtp` backport for Debian Jessie
---

This script will build `ssmtp` with the [Red Hat patches](http://pkgs.fedoraproject.org/cgit/rpms/ssmtp.git/tree/) giving the following improvements:

* The SSL Certificate Authority can be verified (but unfortunately not the host yet).
* This builds against `openssl` giving stronger encryption than `gnutls`.

```
## sSMTP for Debian with Red Hat patches for better encryption ##
##-------------------------------------------------------------##
## the normal ciphers:            RSA_AES_128_CBC_SHA1         ##
## this version uses:------ECDHE-RSA-AES256-GCM-SHA384-------- ##
```
It is mandatory that the following is set in `/etc/ssmtp/ssmtp.conf`:

* `TLS_CA_File=/etc/ssl/certs/ca-certificates.crt`

