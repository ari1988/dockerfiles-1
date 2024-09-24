mubeng
======

[mubeng][1] has 2 core functionality:

1. Run proxy server as proxy IP rotation
2. Perform proxy checks

## Quick Start

```bash
$ mubeng --version

$ echo "socks5://x.x.x.x:1080" | mubeng -v -a 0.0.0.0:3128 -f -

$ curl localhost:3128/cert > mubeng.der

$ openssl x509 -inform der -outform pem -in mubeng.der -out mubeng.crt

$ curl --cacert mubeng.crt -x localhost:3128 https://ipinfo.io
```

[1]: https://github.com/kitabisa/mubeng