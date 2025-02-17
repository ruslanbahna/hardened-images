FROM photon:latest
LABEL Name=hardened-photon

RUN \
    # Cache the package files on the host instead of the image https://docs.docker.com/build/cache/#use-the-dedicated-run-cache
    --mount=type=cache,target=/var/cache/tdnf \
    # Forcibly check for updates
    tdnf check-update ; \
    # Always upgrade to the latest version of package even it the base image is published regulary.
    tdnf upgrade -y --allowerasing --obsoletes ; \


