FROM node:8.6 as node

WORKDIR /app

COPY . /app/

COPY package.json /app/

RUN cd /app && npm init -y

ARG env=prod

RUN npm run build -- --prod --environment $env

EXPOSE 4200


CMD ["npm", "start"]