FROM node:14

# locale & timezone (Asia/Tokyo)
# https://github.com/moby/moby/issues/12084
ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

# system update
RUN apt-get update && \
    apt-get install -y vim less

WORKDIR /root

# install yarn command.
# - https://yarnpkg.com/lang/ja/docs/install/#alternatives-stable
# - https://github.com/yarnpkg/yarn/releases
ARG CMD_YARN_VERSION=1.22.5
RUN npm update && \
    npm install --global --no-bin-link yarn@$CMD_YARN_VERSION && \
    chmod +x /usr/local/bin/yarn

WORKDIR /app/src

# copy application code from host.
# COPY ./src/package.json ./

# update and install node_modules
# RUN npm update && npm install && \
#     npm install --global @vue/cli @vue/cli-init
