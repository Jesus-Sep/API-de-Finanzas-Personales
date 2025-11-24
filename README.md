# API de Finanzas Personales

Estructura base para una API de finanzas personales usando:
- Node.js + TypeScript
- Express
- Prisma (Postgres)
- JWT para autenticación
- Docker Compose para base de datos

Características incluidas:
- Registro / Login (JWT)
- CRUD básico de transacciones
- Estructura de carpetas por dominios (routes/controllers/services/middleware)
- Prisma schema para modelos principales

Siguientes pasos recomendados:
- Añadir validación de input (Zod/Joi)
- Implementar tests (Jest/Supertest)
- Añadir endpoints para cuentas, presupuestos y reportes
- Implementar paginación y filtros en endpoints de listado
- Añadir políticas de autorización (roles)

Estructura propuesta:
- src/
  - controllers/
  - routes/
  - services/
  - middleware/
  - prisma/
  - utils/
  - index.ts (arranque)

Variables de entorno (ver .env.example)

Para arrancar:
1. Copiar .env.example a .env y configurar
2. Ejecutar `docker compose up -d` para levantar Postgres (opcional)
3. `npm install`
4. `npx prisma migrate dev --name init`
5. `npm run dev`
