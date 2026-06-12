FROM mcr.microsoft.com/devcontainers/javascript-node:20

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    curl \
    python3 \
    && rm -rf /var/lib/apt/lists/*

# Install both OpenAI Codex CLI and Firecrawl CLI
RUN npm install -g @openai/codex firecrawl-cli

# Set working directory
WORKDIR /workspaces

# Verify installations
RUN node --version && npm --version
