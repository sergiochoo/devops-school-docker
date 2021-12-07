# build image
FROM node:lts-alpine AS builder
WORKDIR /app
COPY . .
RUN npm install && npm run build

# prod image
FROM nginx:1.19-alpine
COPY --from=builder /app/build /usr/share/nginx/html
EXPOSE 80