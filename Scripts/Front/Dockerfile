FROM node:16.10-alpine AS build

WORKDIR /app

EXPOSE 4200

COPY package.json package-lock.json ./

#COPY --from=build dist/DevOpsFront /usr/share/nginx/html

RUN npm install -g npm@8.11.0 -g @angular/cli 

RUN npm install

COPY ./AosoFront .

#RUN npm run build

RUN ng build --prod
