FROM node:20-alpine

WORKDIR /app

# Install dependencies first (better layer caching)
COPY package*.json ./
RUN npm ci --omit=dev

# Copy source
COPY . .

# Backend commonly runs on 3000 (adjust if your app uses another port)
EXPOSE 3000

CMD ["npm", "start"]
