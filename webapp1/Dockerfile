FROM node:16-alpine As firststage
WORKDIR /sujji
COPY package*.json .
RUN npm install

FROM firststage As finalstage
RUN npm install --production
COPY . .
CMD ["node", "app.js"]
