# EquipYa — Frontend

Plataforma marketplace híbrida para alquiler de herramientas y contratación de servicios locales. Estética estilo Instagram, pensada para el Gran Buenos Aires.

## 🌐 Links

- **Frontend (producción):** https://equipya-frontend.vercel.app
- **Backend (producción):** https://equipya-backend.onrender.com
- **Repositorio backend:** https://github.com/yamibz/-equipya-backend

## Stack

- **React 18** + **Vite**
- CSS puro (sin frameworks de UI)
- Fetch nativo para llamadas al backend
- Google Fonts (Montserrat + Inter + Syne)
- Deploy: **Vercel** (frontend) + **Render** (backend) + **MongoDB Atlas** (base de datos)

## Estructura del proyecto

```
src/
├── pages/
│   ├── auth/
│   │   ├── Login.jsx        # Pantalla de inicio de sesión
│   │   ├── Register.jsx     # Pantalla de registro
│   │   ├── AuthPage.jsx     # Router entre login y registro
│   │   └── Auth.css         # Estilos compartidos de auth
│   ├── Home.jsx             # Feed principal con filtros y búsqueda
│   ├── Home.css             # Estilos del feed
│   └── ProductDetail.jsx    # Detalle de artículo/herramienta
├── App.jsx                  # Navegación principal
├── App.css
├── main.jsx
└── index.css
```

## Funcionalidades

### Autenticación
- Registro con validación de campos
- Inicio de sesión con manejo de errores
- Toggle mostrar/ocultar contraseña
- Sesión guardada en `localStorage`
- Diseño split: panel de marca + formulario

### Home / Feed
- Feed fetcheado desde `GET /api/articulos`
- Búsqueda en tiempo real por nombre, categoría y ubicación
- Tabs: Todo, Productos, Servicios, Cámaras, Herramientas, Electricidad, Plomería
- Sidebar con filtros de fecha, zona (km) y precio
- Cards con imagen, precio, ubicación, rating, like y guardar
- Modal asistente IA
- Burbuja de chat directo
- Modal para subir publicación

### Detalle de producto
- Galería de imágenes con thumbnails
- Selector de fechas con cálculo de total
- Card del vendedor con rating y verificación
- Tabs de descripción, especificaciones y reseñas

### Navegación
```
Login / Registro → Home → ProductDetail
```

## Configuración local

### Variables de entorno

Crear `.env` en la raíz del proyecto:

```
VITE_API_URL=http://localhost:3000
```

### Instalación y ejecución

```bash
npm install
npm run dev
```

Frontend disponible en `http://localhost:5173`

> El backend debe estar corriendo en `http://localhost:3000`

## Endpoints utilizados

| Método | Ruta | Descripción |
|--------|------|-------------|
| POST | `/api/usuarios/registro` | Registro de usuario |
| POST | `/api/usuarios/login` | Inicio de sesión |
| GET | `/api/articulos` | Lista de artículos |
| GET | `/api/articulos/:id` | Detalle de artículo |

## Pendiente

- [ ] Asistente IA funcional (requiere API key server-side)
- [ ] Conectar modal "Subir publicación" al backend
- [ ] Filtros de fecha y zona funcionales
- [ ] Pantalla de perfil de usuario
- [ ] Imágenes reales subidas por usuarios

## Autores

Proyecto académico — Desarrollo de Software 2026  
Yamila Báez · Marcos Ruiz Díaz · Leandro Rodriguez· Valentina Ortigoza
