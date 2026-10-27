
# CrewCar — Grupo 3

Plataforma web para comprar, vender e intercambiar piezas y recambios de coche de forma técnica, segura y sencilla.

## El problema

Encontrar recambios compatibles en plataformas generalistas puede ser lento y complicado. Además, los usuarios se exponen a estafas, piezas incompatibles y problemas de comunicación durante las transacciones.

**CrewCar** busca resolver estos problemas mediante un catálogo especializado de piezas, filtros técnicos de búsqueda, comunicación entre usuarios y funcionalidades de ubicación. También se contempla la supervisión de mensajes mediante inteligencia artificial para detectar posibles fraudes y avisar a los moderadores.

## Objetivos del proyecto

- Facilitar la publicación y búsqueda de anuncios de recambios de automóvil.
- Mejorar la compatibilidad de las piezas mediante filtros técnicos.
- Permitir la comunicación entre compradores y vendedores mediante un chat.
- Incorporar un mapa para consultar ubicaciones relevantes.
- Facilitar las relaciones entre usuarios mediante un sistema de amigos.
- Mejorar la seguridad mediante autenticación, roles y detección de posibles comportamientos fraudulentos.
- Desarrollar una aplicación mantenible, probada y desplegada en producción.

## Funcionalidades previstas

- **Usuarios y autenticación:** registro, inicio de sesión, perfil y rutas protegidas mediante JWT.
- **Roles:** diferenciación entre usuarios y administradores.
- **Anuncios:** creación, consulta, actualización y eliminación de anuncios de recambios.
- **Búsqueda técnica:** filtros por marca, modelo, año y referencia OEM.
- **Imágenes:** incorporación de fotografías a los anuncios.
- **Mensajería:** conversaciones y envío de mensajes entre usuarios.
- **Mapa:** visualización de ubicaciones mediante Google Maps y acceso al chat desde el mapa.
- **Sistema de amigos:** funcionalidades para conectar usuarios.
- **Privacidad:** opción para ocultar el estado en línea.
- **Seguridad:** medidas de autenticación y evaluación de posibles mensajes fraudulentos.
- **Pruebas y despliegue:** automatización de pruebas y publicación de la aplicación.

Estas funcionalidades se implementarán progresivamente durante los sprints del proyecto.

## Equipo

| Integrante | Rol principal |
|---|---|
| Gonzalo Pérez González | Frontend Lead |
| Óscar García Jaén | Backend Lead |
| Laura Sánchez Manzanares | Database Manager |
| Ismael Íñiguez Toledo | QA y despliegue |

Los roles principales identifican las áreas de responsabilidad de cada integrante. Las funciones de Product Owner, Scrum Master y Developer podrán rotar durante los sprints.

## Stack tecnológico

El proyecto utiliza el stack **MERN**, complementado con herramientas de pruebas, calidad y despliegue.

| Tecnología | Uso |
|---|---|
| React | Interfaz de usuario |
| Vite | Entorno de desarrollo del frontend |
| Node.js | Entorno de ejecución del backend |
| Express | Desarrollo de la API REST |
| MongoDB Atlas | Base de datos en la nube |
| bcrypt | Protección de contraseñas mediante hash |
| JSON Web Tokens (JWT) | Autenticación |
| Google Maps | Mapas y funcionalidades de ubicación |
| ESLint | Análisis estático del código |
| Prettier | Formato consistente del código |
| Jest y Supertest | Pruebas del backend y de la API |
| Maestro | Pruebas automatizadas de flujos de usuario |
| GitHub Actions | Integración continua y automatización del despliegue |
| Vercel | Despliegue previsto del frontend |
| Render | Despliegue previsto del backend |
| Toggl Track | Registro del tiempo de trabajo |

La utilización de servicios externos y sus posibles costes dependerá de la configuración final del proyecto.

## Arquitectura prevista

La aplicación se organizará en dos partes principales:

- **Frontend (`client/`):** interfaz desarrollada con React y Vite.
- **Backend (`server/`):** API desarrollada con Node.js y Express.
- **Base de datos:** MongoDB Atlas para almacenar usuarios, anuncios, conversaciones y demás información necesaria.

El frontend se comunicará con el backend mediante peticiones HTTP a la API. El backend gestionará la lógica de negocio, la autenticación y el acceso a la base de datos.

## Planificación del desarrollo

El proyecto se organiza en seis sprints de una semana.

| Sprint | Fechas | Objetivo principal |
|---|---|---|
| 1. Setup y arquitectura base | 02/11–06/11/2026 | Preparar el entorno, la estructura del proyecto, la base de datos y el despliegue inicial. |
| 2. Autenticación y roles | 09/11–13/11/2026 | Implementar el registro, el login, los roles y las rutas protegidas. |
| 3. Funcionalidades principales (parte 1) | 16/11–20/11/2026 | Desarrollar anuncios, filtros técnicos y mensajería. |
| 4. Funcionalidades principales (parte 2) | 23/11–27/11/2026 | Integrar el mapa, el sistema de amigos y las opciones de privacidad. |
| 5. Testing y optimización | 30/11–04/12/2026 | Ejecutar pruebas, corregir errores y mejorar la accesibilidad. |
| 6. Despliegue y documentación final | 07/12–11/12/2026 | Completar CI/CD, documentación, despliegue e informe final. |

Las fechas y los entregables corresponden a la planificación prevista y podrán ajustarse según el avance real del equipo.

## Gestión del proyecto

La organización y el seguimiento del trabajo se realizarán con GitHub Projects.

Cada tarea contará con un responsable, una prioridad, una estimación de horas, una categoría y un estado. El flujo de trabajo será:

1. Crear o seleccionar un issue.
2. Asignar responsable, sprint y estimación.
3. Crear una rama para desarrollar la tarea.
4. Registrar el tiempo de trabajo en Toggl Track.
5. Abrir una pull request.
6. Solicitar una revisión por otro integrante.
7. Integrar los cambios tras la revisión.
8. Actualizar el estado de la tarea.

La capacidad prevista es de 40 horas semanales para el equipo completo, con un margen aproximado del 15 % para imprevistos y una planificación de 34 horas por sprint.

## Cómo arrancarlo

El proyecto se encuentra en fase de planificación y preparación del desarrollo. Las instrucciones definitivas de instalación y ejecución se añadirán cuando estén implementados el frontend y el backend.

Una vez disponible el código, esta sección incluirá:

- Requisitos previos y versiones necesarias.
- Clonación del repositorio.
- Instalación de dependencias.
- Configuración de variables de entorno.
- Conexión a MongoDB Atlas.
- Arranque del frontend y del backend.
- Ejecución de pruebas.

No se deben añadir credenciales, claves API ni secretos al repositorio. Las variables sensibles se configurarán mediante archivos locales de entorno y la configuración segura de los servicios de despliegue.

## Pruebas y calidad

Se prevé utilizar Jest y Supertest para comprobar el funcionamiento del backend y de las rutas principales de la API. Maestro se utilizará para automatizar flujos de usuario cuando corresponda.

También se aplicarán revisiones de código mediante pull requests y herramientas de análisis y formato para mantener una base de código consistente.

## Seguridad y privacidad

La aplicación contempla las siguientes medidas:

- Almacenamiento de contraseñas mediante hash con bcrypt.
- Autenticación basada en JWT.
- Protección de las rutas que requieren autenticación.
- Control de permisos según los roles de usuario.
- Gestión segura de variables de entorno.
- Medidas de privacidad relacionadas con el estado en línea.
- Evaluación de posibles mensajes fraudulentos y notificación a moderadores, según la implementación final.

La detección mediante inteligencia artificial se considera una funcionalidad prevista y deberá validarse durante el desarrollo antes de presentarse como disponible.

## Enlaces del proyecto

- [Tablero de GitHub Projects](https://github.com/users/oscargarciajaen/projects/7/views/1)
- [Repositorio de CrewCar](https://github.com/oscargarciajaen/CrewCar)
- [Contrato del equipo](https://github.com/oscargarciajaen/CrewCar/blob/develop-proyecto/docs/CONTRATO.md)
- [Propuesta del proyecto](https://github.com/oscargarciajaen/CrewCar/blob/develop-proyecto/docs/propuesta)

## Estado del proyecto

**Estado:** planificación y preparación del desarrollo.

Las funcionalidades descritas representan los objetivos previstos. Se actualizará este README conforme se implementen, prueben y desplieguen los distintos componentes.

## Licencia

La licencia del proyecto se definirá cuando se establezcan las condiciones de distribución y uso del código.
