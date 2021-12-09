# build image
FROM node:14 AS builder
WORKDIR /app
COPY . .
RUN npm install && npm run build

# prod image
FROM nginx:1.19-alpine
COPY --from=builder /app/build /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80