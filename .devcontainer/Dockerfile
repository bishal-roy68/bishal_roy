FROM mcr.microsoft.com/devcontainers/universal:2-linux

# 1. Install system prerequisites (xz-utils, curl, etc.)
RUN apt-get update && \
    apt-get install -y xz-utils curl gnupg && \
    rm -rf /var/lib/apt/lists/*

# 2. Install Node.js (you need Node to get the Vue CLI)
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - && \
    apt-get install -y nodejs

# 3. Install the Vue CLI globally
RUN npm install -g @vue/cli

# 4. Upgrade pip and install Flask
RUN pip install --upgrade pip && \
    pip install flask
