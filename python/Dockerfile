# Usamos una imagen base de Python
FROM python:3.9-slim

# Varibles de entorno para ejecutar el proyecto
ENV FLASK_APP=flaskr
ENV FLASK_ENV=development

# Instalamos git
RUN apt-get update && \
    apt-get install -y git && \
    rm -rf /var/lib/apt/lists/*

# Clonamos el repositorio de Flask
RUN git clone https://github.com/codefresh-contrib/python-flask-sample-app /app

# Establecemos el directorio de trabajo
WORKDIR /app

# Extraer los archivos necesarios
COPY . /app

# Instalamos Flask y las dependencias necesarias para el proyecto
RUN pip install --editable .
RUN flask init-db

# Exponemos el puerto en el que se ejecutará la aplicación
EXPOSE 5000

# Comando para ejecutar la aplicación (ejemplo básico)
CMD ["flask", "run", "--host=0.0.0.0"]
