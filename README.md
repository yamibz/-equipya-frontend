# 🛠️ EquipYa — Frontend

Plataforma marketplace híbrida para alquiler de herramientas y contratación de servicios locales. Pensada para el Gran Buenos Aires con una estética moderna.

## 🌐 Enlaces
- **Frontend (producción):** [EquipYa Vercel](https://equipya-frontend.vercel.app)
- **Backend (producción):** [EquipYa Render](https://equipya-backend.onrender.com)
- **Repositorio Backend:** [GitHub Backend](https://github.com/yamibz/-equipya-backend)

## 🚀 Tecnologías y Stack
- **Core:** React 18 + Vite
- **Estilos:** CSS puro (sin frameworks de UI) + Google Fonts
- **Peticiones:** Fetch nativo
- **Infraestructura:** Vercel (Frontend), Render (Backend), MongoDB Atlas (Base de datos)

## 📂 Estructura del proyecto
```text
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
✨ Funcionalidades principalesAutenticación: Registro con validación, inicio de sesión, sesión persistente (localStorage) y diseño split.Feed / Home: Búsqueda en tiempo real, listado desde /api/articulos, filtros en sidebar y tabs de categorías.Detalle de Producto: Galería con thumbnails, selector de fechas con cálculo de total y perfil del vendedor.⚙️ Instalación y ejecución localClonar el repositorio:Bashgit clone [https://github.com/yamibz/-equipya-frontend.git](https://github.com/yamibz/-equipya-frontend.git)
Ingresar a la carpeta:Bashcd -equipya-frontend
Instalar las dependencias:Bashnpm install
Configurar variables de entorno:
Crear un archivo .env en la raíz del proyecto con la URL del backend local:Fragmento de códigoVITE_API_URL=http://localhost:3000
Iniciar el servidor de desarrollo:Bashnpm run dev
(El frontend estará disponible en http://localhost:5173 y requiere que el backend esté corriendo en http://localhost:3000).🔌 Endpoints consumidosMétodoRutaDescripciónPOST/api/usuarios/registroRegistro de usuarioPOST/api/usuarios/loginInicio de sesiónGET/api/articulosLista de artículosGET/api/articulos/:idDetalle de artículo👥 Autores y DesarrolloProyecto académico — Desarrollo de Software 2026.Equipo: Yamila Báez · Marcos Ruiz Díaz · Leandro Rodriguez · Valentina Ortigoza.Mi contribución directa incluyó la colaboración activa en el desarrollo full stack durante las fases de construcción, implementando componentes en el frontend y configurando la conexión con los endpoints.
