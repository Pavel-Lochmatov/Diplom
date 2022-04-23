FROM node:latest
WORKDIR /gate-simulator/app
COPY package.json .
RUN npm install
COPY . ./
EXPOSE 9999
CMD ["npm", "start"]