# Fase 4 · Recursos · <estudio>
## Introducción

Introduciremos los diferentes roles que habrá y quienes lo llevarán a cabo esto es importante debido a que la planeación y organización de dichos roles ayudará a no tener problemas futuros con las tareas y quien es el líder de cada apartado

## 1. Las personas

Cada miembro del equipo ocupará un rol designado siendo Frontend Lead,Backend Lead,Database Manager y QA y despliegue

### Roles técnicos

El equipo se organizará mediante roles técnicos para repartir las responsabilidades y facilitar la revisión del código. Cada responsable coordinará su área y revisará los Pull Requests relacionados con ella.

| Persona | Rol | De qué responde |
|---|---|---|
| Persona 1 | Frontend Lead | Coordinar y revisar el desarrollo de la interfaz de usuario. |
| Persona 2 | Backend Lead | Coordinar y revisar la lógica del servidor y la API. |
| Persona 3 | Database Manager | Diseñar y mantener la estructura de la base de datos y revisar su integración. |
| Persona 4 | QA y despliegue | Coordinar las pruebas y comprobar el correcto funcionamiento de la aplicación desplegada. |

### Responsables por módulo
Cada módulo tendrá una persona responsable y otra de apoyo. El responsable coordinará su desarrollo completo y comprobará que funciona correctamente.

| Módulo | Requisitos (RF) | Responsable | Apoyo |
|---|---|---|---|
| Usuarios y perfiles | Registro, inicio de sesión y perfiles de usuario. | Persona 2 | Persona 3 |
| Catálogo y anuncios | Publicación, consulta y búsqueda de recambios. | Persona 1 | Persona 3 |
| Mensajería | Comunicación entre compradores y vendedores. | Persona 2 | Persona 1 |
| Base de datos | Almacenamiento y organización de usuarios, anuncios y conversaciones. | Persona 3 | Persona 2 |
| Pruebas y despliegue | Comprobación del MVP y publicación de la aplicación. | Persona 4 | Persona 1 |

### Comunicación     (enlace al contrato)

El equipo seguirá las normas de comunicación y colaboración establecidas en el [contrato del equipo](../CONTRATO.md). Las tareas se organizarán mediante el tablero del proyecto y los cambios de código se gestionarán mediante Issues y Pull Requests revisadas por otro compañero.

## 2. La tecnología
### Stack, servicios y APIs   (enlace a la fase 2)

La aplicación utilizará la arquitectura MERN, con React para el frontend, Node.js y Express para el backend y MongoDB para la base de datos. El despliegue y las herramientas seleccionadas se detallan en el documento de [viabilidad técnica](02-viabilidad-tecnica.md).

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
### Ramas
### Estructura de carpetas
