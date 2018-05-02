FROM node:8.9 AS build
WORKDIR /app
ADD . /app
RUN yarn run build

FROM bitnami/nginx
COPY --from=build /app/build /app
