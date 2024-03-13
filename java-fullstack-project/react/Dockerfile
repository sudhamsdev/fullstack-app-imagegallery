FROM node:18-alpine AS build
LABEL maintainer="sudhams reddy duba<sudhams@visualpath.in>"
COPY . /app
WORKDIR /app
RUN npm install
RUN npm run build

FROM nginx:alpine
LABEL maintainer="sudhams reddy duba<sudhams@visualpath.in>"
COPY default.conf /etc/nginx/conf.d
COPY --from=build /app/dist/ /usr/share/nginx/html
