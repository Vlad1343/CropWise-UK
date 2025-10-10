# syntax=docker/dockerfile:1
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json* pnpm-lock.yaml* yarn.lock* ./
RUN npm ci || npm install
COPY . .
ENV BACKEND_URL=
EXPOSE 5173
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
