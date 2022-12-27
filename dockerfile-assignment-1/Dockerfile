# use this empty Dockerfile to build your assignment
FROM node:6-alpine

RUN apk add --no-cache tini \
    && npm install \
    && npm cache clean --force

WORKDIR /usr/src/app
COPY package.json /the/workdir/path -p /usr/src/app/

EXPOSE 3000

CMD [ "/sbin/tini -- node ./bin/www" ]

# NOTE: The instructions are now in the README.md file in this directory.
