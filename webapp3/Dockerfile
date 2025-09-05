FROM node:16-alpine As Firststage
WORKDIR /dada
COPY package*.json .
RUN npm install

FROM Firststage As Finalstage
RUN npm install --production
COPY . .
CMD ["node", "app.js"]
