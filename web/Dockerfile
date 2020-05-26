# # Build environment
# FROM node:lts-alpine as build-stage

# # install simple http server
# RUN npm install -g http-server

# # make the 'app' folder the current working directory
# WORKDIR /app

# # copy both 'package.json' and 'package-lock.json' (if available)
# COPY frontend/package*.json ./app/

# # install project dependencies
# RUN npm install

# # copy project files and folders to the current working directory (i.e. 'app' folder)
# COPY frontend/* /app/

# # build app for production with minification
# # RUN npm run build

# FROM nginx:stable-alpine as production-stage
# COPY --from=build-stage /app/dist /usr/share/nginx/html

# EXPOSE 80

# # CMD ["npm run serve"]
# # CMD [ "http-server", "dist" ]
# CMD ["nginx", "-g", "daemon off;"]

FROM node:lts-alpine  
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
# RUN npm run build
CMD ["npm", "run", "serve"]

# # production stage
# FROM nginx:stable-alpine as production-stage
# COPY --from=build-stage /app/dist /usr/share/nginx/html
# EXPOSE 80
# CMD ["nginx", "-g", "daemon off;"]

# FROM node:10.15.3-alpine AS builder

# WORKDIR /app

# COPY ./package.json ./
# RUN npm install

# COPY . .
# RUN npm run build

# FROM nginx
# EXPOSE 3000

# COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
# COPY --from=builder /app/dist /usr/share/nginx/html


