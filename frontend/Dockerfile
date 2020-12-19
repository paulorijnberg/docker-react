# 1) Build Phase: Install dependencies and run NPM install -> Creates folder /app/build --> we want this for our Run phase
FROM node:alpine
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

# 2) Run phase
FROM nginx:latest

# Here take the build folder and serve that for nginx to host
# Default command starts up nginx, therefor no CMD
COPY --from=0 /app/build /usr/share/nginx/html