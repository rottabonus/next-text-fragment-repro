FROM node:24-alpine AS builder

WORKDIR /app

COPY package.json package-lock.json* ./

RUN npm install

COPY . .

RUN npm run build

FROM node:24-alpine

WORKDIR /app

COPY --from=builder /app/out ./out
COPY package.json ./

RUN npm install serve

EXPOSE 3000

CMD ["npx", "serve", "out", "-l", "3000"]
