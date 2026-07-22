# KAIRÓS - Plataforma de gestión integral del riesgo

Prototipo profesional, responsivo y navegable basado en el proyecto KAIRÓS. Incluye experiencia pública, biblioteca, protocolos, cursos, noticias, alertas, mapas, comunidad, recuperación ambiental, formularios, autenticación simulada y panel administrativo.

## Inicio rápido

```bash
npm install
npm run dev
```

Luego abre la dirección local que muestra Vite.

Para crear una versión optimizada:

```bash
npm run build
npm run preview
```

## Funciones del prototipo

- Navegación SPA con rutas por hash.
- Modo claro y oscuro persistente.
- Buscador global con `Ctrl + K`.
- Protocolos por amenaza y fase: antes, durante y después.
- Biblioteca con búsqueda, filtros, favoritos y descarga simulada.
- Cursos con módulos, progreso, inscripción y certificados simulados.
- Noticias, boletín y categorías.
- Centro de alertas con niveles de severidad y mapa demostrativo.
- Mapa con capas activables para riesgo, refugios, hospitales y puntos seguros.
- Foro comunitario con publicaciones persistidas en `localStorage`.
- Formularios de contacto y voluntariado.
- Panel administrativo visual con módulos, tablas y creación de borradores.
- Base de datos PostgreSQL/Supabase preparada en `database/schema.sql`.
- Diseño adaptable a escritorio, tableta y móvil.

## Datos y backend

La interfaz funciona como prototipo front-end. Las acciones de contenido se simulan y algunas se guardan en `localStorage`. Para producción se debe conectar:

1. Autenticación real y control de roles.
2. PostgreSQL/Supabase usando `database/schema.sql`.
3. Almacenamiento de archivos y videos.
4. API de alertas oficiales.
5. Proveedor GIS como Mapbox, Google Maps o Leaflet.
6. Servicio de correo y notificaciones push.
7. Pasarela de pago si se activa la suscripción premium.

## Estructura

```text
src/
  components/     Navegación, UI, iconos y modales
  data/           Datos demostrativos
  hooks/          Persistencia local
  pages/          Páginas públicas y panel administrativo
  App.tsx         Router y composición principal
  styles.css      Sistema visual completo y responsivo
database/
  schema.sql      Modelo relacional preparado para PostgreSQL
public/
  kairos-mark.svg Identidad visual de demostración
```

## Seguridad para producción

Aplicar políticas de seguridad por fila, validación del servidor, sanitización de contenido, antivirus para archivos, control de tamaños, rate limiting, registros de auditoría y copias de seguridad. Las alertas reales deben mostrar fuente, hora, vigencia y autoridad responsable.
