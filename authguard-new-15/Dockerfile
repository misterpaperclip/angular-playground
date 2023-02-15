#stage 1
FROM node:latest as node
WORKDIR /authguard-new-15
COPY . .
RUN npm install
RUN npm run build --prod
#stage 2
FROM nginx:alpine
COPY --from=node /authguard-new-15/dist/authguard-new-15 /usr/share/nginx/html