FROM docker.io/library/busybox:1.37.0-musl@sha256:254e6134b1bf813b34e920bc4235864a54079057d51ae6db9a4f2328f261c2ad

COPY --from=docker.io/dxflrs/garage:v2.2.0@sha256:45a61ce3f7c9c24fc23d9ed2b09b27ed560ab87b34605d175d5c588f539c24e4 /garage /usr/bin/garage

ENTRYPOINT ["/usr/bin/garage", "server"]
