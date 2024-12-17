# Usar la imagen oficial de Rust como base
FROM rust:latest

# Instalar git para poder clonar el repositorio
RUN apt-get update && apt-get install -y git

# Establecer el directorio de trabajo
WORKDIR /usr/src/myapp

# Clonar el repositorio
RUN git clone https://github.com/khalidabuhakmeh/rocketapp.git .

# Actualizar las dependencias del proyecto
RUN cargo update

# Compilar el proyecto, esto también descarga las dependencias necesarias
RUN cargo build --release

# Exponer el puerto en el que Rocket se ejecutará
EXPOSE 8000

# Comando para ejecutar la aplicación
CMD ["cargo", "run", "--release"]
