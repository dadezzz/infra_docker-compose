FROM docker.io/library/busybox:1.37.0-musl@sha256:19b646668802469d968a05342a601e78da4322a414a7c09b1c9ee25165042138

COPY --from=docker.io/dxflrs/garage:v2.2.0@sha256:45a61ce3f7c9c24fc23d9ed2b09b27ed560ab87b34605d175d5c588f539c24e4 /garage /usr/bin/garage

ENTRYPOINT ["/usr/bin/garage", "server"]
