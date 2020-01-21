FROM node:latest
RUN mkdir -p /app
COPY . /app
WORKDIR /app
RUN npm install && npm audit fix
ENV NODE_ENV=${NODE_ENV}
EXPOSE 80
CMD ["node", "server.js"]