FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

RUN apt-get update && apt-get install -y \
    curl \
    gnupg2 \
    build-essential \
    ruby-full \
    && rm -rf /var/lib/apt/lists/*

# Install bundler and Jekyll locally for devuser
USER devuser
RUN gem install --user-install bundler jekyll

# Add Ruby and Bundler to PATH
ENV PATH="/home/devuser/.gem/ruby/3.0.0/bin:$PATH"
