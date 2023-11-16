FROM node:latest

WORKDIR /app
COPY . .
RUN npm -f install
RUN cd ./backend
EXPOSE 5000
CMD ["npm", "start"]
