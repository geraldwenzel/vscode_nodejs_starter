FROM mcr.microsoft.com/devcontainers/base:noble

# Install npm
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
  && apt-get -y install --no-install-recommends npm \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* 

# Install `n` version manager and then use n to install the latest 
# stable node version
RUN npm install -g n diff-so-fancy \
  && n stable

# Install Yarn
RUN npm install -g yarn

USER vscode

# Configure shell
RUN echo 'alias g=git' >> /home/vscode/.bash_aliases
