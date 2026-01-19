FROM node:20-alpine

WORKDIR /app

# Instalar dependencias del sistema necesarias para Expo
RUN apk add --no-cache git python3 make g++

# Instalar Expo CLI globalmente
RUN npm install -g expo-cli @expo/ngrok

# Copiar archivos de dependencias
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Copiar código fuente
COPY . .

# Exponer puertos de Expo
EXPOSE 8081

# Comando por defecto
CMD ["npx", "expo", "start", "--tunnel"]
