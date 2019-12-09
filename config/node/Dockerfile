FROM node:lts-alpine as builder
WORKDIR /tmp/app
COPY ./app/package.json .
RUN npm install

FROM node:lts-alpine
WORKDIR /usr/src/app
COPY --from=builder /tmp/app/node_modules ./node_modules
COPY --chown=node:node ./app .
USER node

EXPOSE 3000

CMD [ "npm", "start" ]


