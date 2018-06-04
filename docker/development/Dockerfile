FROM library/node:9.0

ARG USER_ID=1000
ARG GROUP_ID=1000

RUN npm install -g angular-cli loopback-cli @mean-expert/fireloop

RUN groupmod -g ${GROUP_ID:-1000} node \
  && usermod -u ${USER_ID:-1000} node

USER node

WORKDIR /home/nodejs

EXPOSE 4200 3000