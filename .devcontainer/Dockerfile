FROM rust:1.70

# Install Rust tooling
ARG RUST_ANALYZER_VERSION=2023-04-10
RUN wget -qO- "https://github.com/rust-analyzer/rust-analyzer/releases/download/${RUST_ANALYZER_VERSION}/rust-analyzer-$(uname -m)-unknown-linux-musl.gz" | \
    gunzip > /usr/local/bin/rust-analyzer && \
    chmod 500 /usr/local/bin/rust-analyzer
RUN rustup component add clippy rustfmt

RUN cargo install cargo-watch
RUN cargo install cargo-audit