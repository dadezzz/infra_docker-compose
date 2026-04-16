FROM docker.io/library/caddy:2.11.2-builder-alpine@sha256:8a3cbe563c368525df245ec5bbb68e1edd441ae5fe7fc400223380c6aa0427f3 AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.11.2-alpine@sha256:24d58e24e4231c6667677a39469a3d843a3222eadbf640f22933f24bed0939ec

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
