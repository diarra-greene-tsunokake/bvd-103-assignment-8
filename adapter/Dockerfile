# adapter/Dockerfile
FROM node:18-alpine

WORKDIR /app

# Copy package files first to leverage Docker cache for npm install
COPY ../package.json ../package-lock.json ./ 

RUN npm install

# Copy only adapter source files
COPY . .

# Build or start your app (adjust this command to your actual build/start script)
CMD ["npx", "tsx", "index.ts"]
