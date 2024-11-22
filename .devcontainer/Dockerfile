FROM python:3.11-slim

# Instalar dependencias necesarias
RUN apt-get update && apt-get install -y \
    git \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Instalar Poetry
RUN curl -sSL https://install.python-poetry.org | python3 -

# Agregar Poetry al PATH
ENV PATH="/root/.local/bin:$PATH"

# Configurar Poetry para que no cree entornos virtuales dentro del contenedor
RUN poetry config virtualenvs.create false

# Establecer el directorio de trabajo
WORKDIR /workspace

# Mantener el contenedor corriendo
CMD ["sleep", "infinity"]
