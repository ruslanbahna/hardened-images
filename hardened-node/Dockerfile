FROM photon:latest
LABEL Name=hardened-node-photon
RUN \
    --mount=type=cache,target=/var/cache/tdnf \
    --mount=type=cache,target=/root/.cache/pip \
    tdnf check-update ; \
    tdnf upgrade -y --allowerasing --obsoletes ; \
    tdnf --setopt=tsflags=nodocs --allowerasing --assumeyes install nodejs ; \
    npm install -g yarn ;

