FROM ghcr.io/adamijak/typst:main

ENV PUPPETEER_SKIP_CHROMIUM_DOWNLOAD=true \
    PUPPETEER_EXECUTABLE_PATH=/usr/bin/chromium-browser \
    ENV="/root/.shrc"

RUN apk add --update git nodejs chromium \
    && wget -qO- https://get.pnpm.io/install.sh | ENV="$HOME/.shrc" SHELL="$(which sh)" sh - \
    && source /root/.shrc \
    && pnpm install -g @mermaid-js/mermaid-cli
