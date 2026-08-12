FROM mcr.microsoft.com/devcontainers/rust:1

# Add useful Rust components
RUN rustup component add rustfmt clippy && \
    cargo install cargo-watch cargo-edit