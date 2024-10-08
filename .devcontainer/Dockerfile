FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

RUN apt-get update && apt-get install -y \
    curl \
    gnupg2 \
    build-essential \
    ruby-full \
    && rm -rf /var/lib/apt/lists/* \
    && gem install bundler jekyll

# Create a non-root user to work in container
RUN useradd -m devuser
USER devuser
