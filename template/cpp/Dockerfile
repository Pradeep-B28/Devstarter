FROM mcr.microsoft.com/devcontainers/cpp:bookworm

# Install additional tools for C++ development
RUN apt-get update && apt-get install -y \
    cmake \
    gdb \
    valgrind \
    clang-format \
    clang-tidy \
    && apt-get clean && rm -rf /var/lib/apt/lists/*