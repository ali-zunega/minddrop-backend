# MindDrop Backend

Repositorio BackEnd para la aplicacion web MindDrop. Proporciona autenticación segura y almacenamiento de datos mediante API REST.

## 🚀 Tecnologías

- **Runtime:** Node.js
- **Framework:** Express
- **Base de datos:** MongoDB + Mongoose
- **Autenticación:** JWT + bcryptjs
- **Variables de entorno:** dotenv

## 📋 Prerrequisitos

- Node.js >= 18
- MongoDB (local o Atlas)
- npm

## 🔧 Instalación

```bash
git clone https://github.com/ali-zunega/minddrop-backend.git
cd minddrop-backend
npm install
```

## ⚙️ Variables de Entorno

Crear un archivo `.env` en la raíz con:

```env
PORT=3000
MONGODB_URI=tu_string_de_conexion
JWT_SECRET=tu_secreto_jwt
```

## 📁 Estructura del Proyecto

```bash
minddrop-backend/
├── src/
│   ├── config/             # Configuración de base de datos, etc.
│   │   └── db.js
│   ├── controllers/        # La lógica de qué hace cada ruta (las funciones)
│   │   ├── authController.js
│   │   └── notesController.js
│   ├── middlewares/        # Capas de seguridad (ej: verificar si el usuario está logueado)
│   │   └── authMiddleware.js
│   ├── models/             # El "molde" o esquema de tus datos (User, Note, Category)
│   │   ├── User.js
│   │   └── Note.js
│   ├── routes/             # Definición de los endpoints (URLs)
│   │   ├── authRoutes.js
│   │   └── notesRoutes.js
│   └── app.js              # Configuración central de Express (CORS, middlewares globales)
├── .env                    # Variables secretas (NUNCA se sube a GitHub)
├── .gitignore              # Para excluir node_modules y el archivo .env
├── index.js                # Punto de entrada que arranca el servidor
└── package.json
```

## 🛠️ Scripts

- `npm start` — Inicia el servidor en producción
- `npm run dev` — Inicia con nodemon (desarrollo)

## 📄 [Licencia](./LICENSE)
