FROM node:22-alpine

# RUN addgroup app && adduser -S -G app app

# USER app

WORKDIR /app

COPY package.json pnpm-lock.yaml ./

# USER root

RUN npm install -g pnpm

# RUN chown -R app:app .

# USER root

# USER app

RUN pnpm install

COPY . .

EXPOSE 5173

CMD ["pnpm", "dev"]