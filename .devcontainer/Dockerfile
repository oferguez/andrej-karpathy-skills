FROM mcr.microsoft.com/devcontainers/javascript-node:20

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Install codex-cli and firecrawl-cli globally
RUN npm install -g codex-cli firecrawl-cli

# Set working directory
WORKDIR /workspaces

# Verify installations
RUN node --version && npm --version && codex-cli --version
