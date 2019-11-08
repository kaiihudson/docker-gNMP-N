FROM node:lts as builder

WORKDIR /tmp/app

COPY package*.json ./

RUN npm install

FROM node:lts

WORKDIR /usr/src/app
#
COPY --from=builder /tmp/app/node_modules ./node_modules
#Gives permission to files just coppied
COPY --chown=node:node . ./

EXPOSE 3000

CMD [ "npm", "start" ]

USER node

