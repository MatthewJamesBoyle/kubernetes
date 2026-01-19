FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

# Install build dependencies and tools for Kubernetes development
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
        build-essential \
        rsync \
        jq \
        shellcheck \
        protobuf-compiler \
        python3 \
        python3-pip \
        curl \
        wget \
        unzip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Install Snyk CLI
RUN curl -fsSL https://static.snyk.io/cli/latest/snyk-linux -o /usr/local/bin/snyk \
    && chmod +x /usr/local/bin/snyk
