FROM ubuntu:22.04

# Update Ubuntu repositories.
RUN apt update

# Install system dependencies.
RUN apt install -y \
    unzip \
    wget \
    git


# Install Aptos CLI tool.
RUN wget https://github.com/aptos-labs/aptos-core/releases/download/aptos-cli-v2.1.0/aptos-cli-2.1.0-Ubuntu-22.04-x86_64.zip \
    && unzip aptos-cli-2.1.0-Ubuntu-22.04-x86_64.zip \
    && mv aptos /usr/local/bin \
    && rm -rf aptos-cli-2.1.0-Ubuntu-22.04-x86_64.zip