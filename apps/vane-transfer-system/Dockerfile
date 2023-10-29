FROM --platform=linux/arm64 node:14-alpine AS development
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npx prisma generate --schema ./libs/core/prisma/schema.prisma
RUN npm run build