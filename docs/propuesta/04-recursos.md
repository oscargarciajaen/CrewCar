# Fase 4 · Recursos · Grupo 3

## Introducción
Esta fase define quién hace qué y con qué herramientas vamos a construir el proyecto que planteamos en las fases anteriores. Aquí se reparten los roles técnicos y los módulos del MVP, se concreta el stack y las herramientas de desarrollo, y se explica cómo gestionamos el tablero, las ramas y la estructura del repositorio para empezar a programar en la UD1. Tener claro desde el principio quién lidera cada parte nos ayudará a evitar problemas con las tareas y a saber a quién acudir en cada apartado.

## 1. Las personas

### Roles técnicos
Cada miembro del equipo tiene un rol técnico: Frontend Lead, Backend Lead, Database Manager y QA y despliegue. Cada responsable coordina su área y revisa los Pull Requests relacionados con ella, pero no tiene por qué programarlo todo.

| Persona | Rol | De qué responde |
|---|---|---|
| Gonzalo | Frontend Lead | Coordinar y revisar el desarrollo de la interfaz de usuario. |
| Oscar | Backend Lead | Coordinar y revisar la lógica del servidor y la API. |
| Laura | Database Manager | Diseñar y mantener la estructura de la base de datos y revisar su integración. |
| Ismael | QA y despliegue | Coordinar las pruebas y comprobar el correcto funcionamiento de la aplicación desplegada. |

### Responsables por módulo
Cada módulo tiene una persona responsable y otra de apoyo. El responsable lo lleva de la base de datos a la pantalla y comprueba que funciona correctamente.

| Módulo | Requisitos (RF) | Responsable | Apoyo |
|---|---|---|---|
| Usuarios y perfiles | Registro, inicio de sesión y perfiles de usuario. | Oscar | Ismael |
| Catálogo y anuncios | Publicación, consulta y búsqueda de recambios con filtros técnicos. | Gonzalo | Laura |
| Mensajería | Comunicación privada entre compradores y vendedores. | Gonzalo | Oscar |
| Moderación con IA | Análisis de las conversaciones y registro de avisos de posible fraude. | Oscar | Laura |
| Base de datos | Almacenamiento y organización de usuarios, anuncios, conversaciones y avisos. | Laura | Ismael |
| Pruebas y despliegue | Comprobación del MVP y publicación de la aplicación. | Ismael | Gonzalo |

### Comunicación
El equipo sigue las normas de comunicación y colaboración establecidas en el [contrato del equipo](../CONTRATO.md). Los canales son WhatsApp y un servidor de Discord. Las tareas se organizan mediante el tablero del proyecto y los cambios de código se gestionan mediante issues y Pull Requests revisadas por otro compañero.

## 2. La tecnología

### Stack, servicios y APIs
La aplicación utiliza la arquitectura MERN: React para el frontend, Node.js y Express para el backend y MongoDB Atlas para la base de datos. El despliegue se hará en Vercel (frontend) y Render (backend). El detalle de cada tecnología, los servicios y sus limitaciones está en el documento de [viabilidad técnica](02-viabilidad-tecnica.md).

Motivo de cada elección:

- **React y Vite:** interfaz basada en componentes reutilizables y desarrollo rápido.
- **React Router:** navegación entre páginas sin recargar la aplicación.
- **Node.js y Express:** permiten crear la API REST con el mismo lenguaje que el frontend.
- **MongoDB Atlas y Mongoose:** base de datos documental flexible para guardar las características de cada pieza.
- **bcrypt y JWT:** protegen las contraseñas y controlan el acceso a las funciones privadas.
- **Vercel y Render:** despliegue gratuito y sencillo desde el repositorio.

### Herramientas de desarrollo

| Para qué | Herramienta |
|---|---|
| Editor de código | Visual Studio Code |
| Revisión de calidad y formato | ESLint y Prettier |
| Entorno de ejecución | Node.js, utilizando la misma versión en todo el equipo |
| Pruebas de la API | Postman, Thunder Client o Bruno (se elegirá una) |
| Pruebas del frontend | Vitest |
| Pruebas del backend | Jest y Supertest |

## 3. La gestión

### Tablero
Las tareas se organizan en el [tablero del proyecto](https://github.com/users/oscargarciajaen/projects/4/views/1). Cada tarea es una issue que se mueve por las columnas del tablero según su estado.

### Ramas
- `main`: versión estable. Solo recibe un PR desde `develop` al cerrar cada sprint.
- `develop`: rama de integración. Las ramas de tarea salen de ella y vuelven a ella.
- Ramas de tarea: una por issue, con su PR hacia `develop`.

El flujo es: issue → rama → PR → review de un compañero → merge. Nadie mergea su propio PR y la review se aprueba antes del merge.

Las ramas `main` y `develop` están protegidas: PR obligatorio con una aprobación.

### Estructura de carpetas
```
.
├── client/            # Frontend (React)
│   └── README.md
├── server/            # Backend (Node + Express)
│   └── README.md
├── docs/
│   ├── CONTRATO.md
│   └── propuesta/     # Fases 0 a 4
├── .gitignore
└── README.md
```
