
FROM node:lts-alpine
WORKDIR /var/www/html/

COPY --chown=node:node ./app .
USER node
RUN npm install

EXPOSE 3000

CMD [ "npm", "start" ]


