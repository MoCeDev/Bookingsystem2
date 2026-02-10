<<<<<<< HEAD
# ---- Base image ----
FROM node:20-alpine

# ---- Create app directory ----
WORKDIR /usr/src/app

# ---- Copy package files first (better caching) ----
COPY package*.json ./

# ---- Install production dependencies ----
RUN npm install --omit=dev

# ---- Copy the rest of the project ----
COPY . .

# ---- Default command ----
CMD ["node", "index.js"]
=======
FROM nginx:alpine
RUN rm -rf /usr/share/nginx/html/*
COPY ./app /usr/share/nginx/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
>>>>>>> ba7a9eb6fe8d04382e907cb27fa58af5a1f0588b
