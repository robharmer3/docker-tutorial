FROM node:12-stretch AS builder
WORKDIR /app
COPY . .
RUN npm install
RUN npm run bulid

FROM nginx:1.29.6
COPY --from=builder /app/build /usr/share/nginx/html