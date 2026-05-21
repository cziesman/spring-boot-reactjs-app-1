FROM node:22 AS builder

WORKDIR /app

COPY ./react-app-frontend ./

RUN npm install
RUN npm run build

FROM node:22-slim

WORKDIR /app

RUN npm install -g serve

COPY --from=builder /app/build ./build

RUN chmod -R g=u /app

EXPOSE 3000

CMD ["serve", "-s", "build", "-l", "3000"]