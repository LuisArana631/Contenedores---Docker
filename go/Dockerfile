# Imagen base de Go
FROM golang:1.17-alpine

# Instalamos git
RUN apk add --no-cache git

# Establecer el directorio de trabajo
WORKDIR /app

# Instalar git y clonar el repositorio
RUN git clone https://github.com/iam-veeramalla/go-web-app.git .

# Corregir la versión de Go en go.mod
RUN sed -i 's/go 1.22.5/go 1.17/g' go.mod

# Descargar las dependencias del proyecto
RUN go mod download


# Puerto de la aplicación
EXPOSE 8080

# Comando para ejecutar la aplicación
CMD ["go", "run", "main.go"]
