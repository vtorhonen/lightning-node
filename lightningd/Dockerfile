FROM debian:stretch-slim as builder
ENV LIGHTNINGD_VERSION=tags/v0.7.1

RUN set -x && \
    apt-get update -qq && \
    apt-get install -qq -y --no-install-recommends --allow-unauthenticated \
        python \
        python3 \
        git \
        make \
        automake \
        autoconf \
        libtool \
        build-essential \
        libprotobuf-c-dev \
        libsodium-dev \
        libbase58-dev \
        libsqlite3-dev \
        libgmp-dev \
        ca-certificates \
        zlib1g-dev && \
    rm -rf /var/lib/apt/lists/*

RUN set -x && \
    git clone https://github.com/ElementsProject/lightning.git /opt/lightningd && \
    cd /opt/lightningd && \
    git checkout $LIGHTNINGD_VERSION && \
    ./configure && \
    make && \
    mkdir -p\
        /usr/local/bin \
        /usr/local/libexec/c-lightning && \
    cp \
        lightningd/lightningd \
        cli/lightning-cli \
        /usr/local/bin/ && \
    cp \
        lightningd/lightning_channeld \
        lightningd/lightning_closingd \
        lightningd/lightning_gossipd \
        lightningd/lightning_hsmd \
        lightningd/lightning_onchaind \
        lightningd/lightning_openingd \
        lightningd/lightning_connectd \
        /usr/local/libexec/c-lightning && \
    rm -rf /opt/lightningd

FROM vtorhonen/bitcoind:0.16.3-1

COPY --from=builder /usr/local/bin /usr/local/bin
COPY --from=builder /usr/local/libexec /usr/local/libexec

RUN set -x && \
    apt-get update -qq && \
    apt-get install -qq -y --no-install-recommends \
        libgcc1 \
        libgmp10 \
        libsodium-dev \
        libsqlite3-dev && \
    rm -rf /var/lib/apt/lists/*

CMD []
ENTRYPOINT []
