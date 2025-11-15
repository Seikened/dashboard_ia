FROM node:22-alpine

WORKDIR /app

# Instalar dependencias si hubiera package.json en el futuro
COPY package*.json ./
RUN if [ -f package.json ]; then npm install; fi

# Copiar resto del código (cuando exista)
COPY . .

# Puerto típico de front dev (ajústalo si usas otro)
EXPOSE 5173

# Comando por defecto: modo dev genérico (ajustar después)
CMD [ "sh", "-c", "if [ -f package.json ]; then npm run dev -- --host 0.0.0.0; else npm install vite && npx vite --host 0.0.0.0; fi" ]
