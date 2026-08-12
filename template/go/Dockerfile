FROM mcr.microsoft.com/devcontainers/go:1.22

# Install additional Go tools
RUN go install github.com/go-delve/delve/cmd/dlv@latest && \
    go install honnef.co/go/tools/cmd/staticcheck@latest