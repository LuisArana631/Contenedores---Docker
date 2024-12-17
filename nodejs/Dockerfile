# Imagen base de Node
FROM node:14

# Directorio de trabajo
WORKDIR /usr/src/app

# Clonar el repositorio e instalación de dependencias
RUN git clone https://github.com/bmorelli25/simple-nodejs-weather-app . && \
  npm install

# Puerto en el que se expone la aplicación
EXPOSE 3000

# Comando para iniciar la aplicación
CMD ["node", "server.js"]
