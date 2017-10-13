# libcurl

As of version 7.56 this build supports OpenSSL and WinSSL. This allows us to use
native Windows Schannel on Windows 7+, but fall back on OpenSSL on Legacy windows
which do not support TLS 1.1 and 1.2 (Vista/2008).

__Update:__ backported [upstream patch](https://github.com/curl/curl/commit/5f9e2ca09b57d82baf239039835b3b06dc41bbc5) 
to [largebuf.patch](largebuf.patch) 

Configuration:

```
    --enable-static \
    --disable-shared \
    --with-ssl \
    --with-winssl \
    --with-winidn \
    --enable-sspi \
    --without-gnutls \
    --without-nghttp2 \
    --without-random \
    --without-libssh2 \
    --without-librtmp \
    --without-libidn2 \
    --without-ca-bundle \
    --without-ca-path
```
