FROM ghcr.io/philips-software/amp-devcontainer-cpp:8.4.0

RUN apt-get update \
    && apt-get install -y --no-install-recommends libsdl2-dev \
    && rm -rf /var/lib/apt/lists/*

HEALTHCHECK NONE