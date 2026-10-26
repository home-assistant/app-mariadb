# Base image updated by Renovate, update versionCompatibility on Alpine base bump
ARG BUILD_FROM=ghcr.io/home-assistant/base:3.23-2026.10.1@sha256:9fd5d40f0682f0dee626cd0d2ea07b96ffef345dac1c6f025d4b4ce30ad362b4
FROM $BUILD_FROM

# Setup base
RUN apk add --no-cache \
    mariadb \
    mariadb-client \
    mariadb-server-utils \
    pwgen

ENV \
    LD_PRELOAD="/usr/local/lib/libjemalloc.so.2"

# Copy data
COPY rootfs /

WORKDIR /

LABEL \
    org.opencontainers.image.title="Home Assistant App: MariaDB" \
    org.opencontainers.image.description="A SQL database server" \
    org.opencontainers.image.source="https://github.com/home-assistant/app-mariadb" \
    org.opencontainers.image.licenses="Apache License 2.0"
