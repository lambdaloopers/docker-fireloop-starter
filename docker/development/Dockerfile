FROM library/node:9.0

ARG USER_ID=1000
ARG GROUP_ID=1000

COPY ./docker/development/entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

RUN npm install -g @mean-expert/fireloop

RUN groupmod -g ${GROUP_ID:-1000} node \
  && usermod -u ${USER_ID:-1000} node

USER node

WORKDIR /home/nodejs

EXPOSE 4200 3000