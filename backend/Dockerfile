FROM python:3.12-slim

WORKDIR /app

# Evitar bytecode y asegurar logs inmediatos
ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

# Dependencias del sistema mínimas
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
 && rm -rf /var/lib/apt/lists/*

# Copiar archivos de proyecto
COPY main.py ./

# Comando por defecto (ajusta a tu entrypoint real)
CMD ["python", "main.py"]
