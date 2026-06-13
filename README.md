# Examen Final - React + Vite (Consumo API Platzi)

**Código: 192676 - 03578**
**Docente:** Cristian Afanador
**Estudiante:** Jhoan Arengas

## Instalación

```bash
npm install
npm run dev
```

Abrir en el navegador: http://localhost:5173

## Estructura del proyecto

```
src
├── features
│   ├── producto
│   │   ├── pages        -> ProductosPage, DetalleProductoPage
│   │   ├── components   -> ProductoCard, ProductoGrid, GaleriaImagenes
│   │   └── service       -> productoService.js (Axios)
│   └── usuarios
│       ├── pages        -> UsuariosPage
│       ├── components   -> UsuarioCard, UsuarioList
│       └── service       -> usuarioService.js (Axios)
├── routes               -> AppRoutes.jsx
├── layouts              -> MainLayout.jsx (Drawer + Topbar)
├── shared               -> apiClient.js, styles/global.css
└── App.jsx
```

## Funcionalidades implementadas

- **Drawer lateral** con navegación a Productos y Usuarios.
- **Productos**: listado con grid de tarjetas reutilizables (`ProductoCard`), consumo de
  `GET /products` con Axios. Click en una tarjeta navega a `/producto/:id`.
- **Detalle de producto**: consume `GET /products/{id}`, muestra nombre, precio,
  categoría, descripción y galería de imágenes navegable (`GaleriaImagenes`), con diseño
  inspirado en Mercado Libre.
- **Usuarios**: listado con `UsuarioCard` reutilizable, consume `GET /users`.
- **React Router DOM**: rutas `/productos`, `/producto/:id`, `/usuarios`.
- **Axios**: cliente centralizado en `shared/apiClient.js`, usado por ambos servicios.
- Manejo de estados de carga y error en cada vista.

## Endpoints consumidos

- `https://api.escuelajs.co/api/v1/products`
- `https://api.escuelajs.co/api/v1/products/{id}`
- `https://api.escuelajs.co/api/v1/users`
