FROM node:18
WORKDIR /app

COPY package.json package.json
COPY package-lock.json packaage-lock.json

RUN npm install

COPY . .
RUN npm run build

CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]

