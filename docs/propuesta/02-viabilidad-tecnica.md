# Fase 2 · Viabilidad técnica · Grupo 3

## Introducción
En esta fase comprobamos que el proyecto que planteamos en la fase 1 se puede construir con nuestro equipo y nuestro tiempo. Definimos los requisitos funcionales y su prioridad (MoSCoW), el MVP, las tecnologías de frontend, backend y base de datos, las capacidades del equipo, lo que tendremos que aprender y los riesgos técnicos con su forma de mitigarlos.

## 1. Requisitos funcionales
- El usuario puede realizar una búsqueda técnica avanzada, filtrando por marca, modelo, año, categoría o referencia.
- El usuario puede añadir alertas de stock personalizadas para que le avisen cuando la pieza que busca esté disponible.
- El usuario puede utilizar la mensajería directa integrada para comunicarse con otros usuarios.
- La IA analiza en segundo plano las conversaciones entre usuarios para detectar casos de estafa, comportamientos sospechosos o lenguaje agresivo.
- El sistema emite alertas automáticas al equipo de moderación cuando la IA detecta un riesgo o una anomalía en las conversaciones.
- El usuario puede consultar el perfil de vendedores o compradores, revisando su historial, valoraciones y comentarios.
- El administrador puede acceder a un panel de moderación activo para gestionar los avisos prioritarios generados por la IA, interviniendo o mediando en las incidencias.

## 2. Priorización MoSCoW

### Must Have
- El usuario puede crear una cuenta nueva y acceder con ella.
- El usuario puede publicar un anuncio de una pieza con sus detalles básicos.
- El usuario puede buscar recambios aplicando filtros técnicos.
- El usuario puede crear una conversación privada para negociar la compra.
- La IA puede auditar las conversaciones en segundo plano para detectar fraudes y avisar a moderación.

### Should Have
- El usuario puede activar una alerta de stock para piezas difíciles de encontrar.
- El usuario puede consultar el perfil y las valoraciones de fiabilidad de otros usuarios.
- El administrador puede acceder al panel de moderación activo para gestionar incidencias.

### Could Have
- El usuario puede editar o eliminar sus anuncios publicados.
- El usuario puede marcar transacciones como finalizadas y dejar valoraciones detalladas.

### Won't Have
- Sistema integrado de pasarela de pago en línea con depósito retenido.
- Aplicación móvil nativa independiente para iOS y Android.

## 3. MVP
El MVP es el recorrido mínimo para que un usuario pueda encontrar y comprar la pieza exacta que necesita sin riesgo de estafa:

1. El usuario crea una cuenta y accede con ella.
2. Filtra el catálogo por los datos técnicos de su coche. El vendedor, por su parte, ha publicado el anuncio de la pieza.
3. Abre un chat interno con el vendedor para negociar la compra.
4. La IA supervisa el chat en segundo plano y, si detecta intentos de estafa o comportamientos no permitidos, guarda un aviso para moderación.

El panel de moderación para gestionar esos avisos queda fuera del MVP (es Should Have).

## 4. Requisitos técnicos: frontend e infraestructura

### Frontend
Vamos a utilizar **React** para crear una interfaz sencilla que se adapte tanto a móviles como a ordenadores, organizada a través de componentes reutilizables.

| **Tecnología** | **Función** |
|---|---|
| React | Construir la interfaz de usuario. |
| Vite | Facilitar el desarrollo y la compilación. |
| React Router | Manejar la navegación entre páginas. |
| Fetch API | Conectar el frontend con el backend. |
| CSS adaptable | Ajustar la interfaz a diferentes dispositivos. |

La interfaz permitirá a los usuarios buscar recambios, aplicar filtros, consultar anuncios, acceder a perfiles y utilizar la mensajería.

### Arquitectura e infraestructura
La aplicación seguirá una arquitectura cliente-servidor basada en MERN. El frontend se comunicará con el backend a través de una API REST.

| **Componente** | **Tecnología** | **Función** |
|---|---|---|
| Frontend | React | Presentar la interfaz. |
| Backend | Node.js y Express | Manejar las peticiones y la lógica. |
| Base de datos | MongoDB Atlas | Almacenar la información. |
| Repositorio | GitHub | Gestionar el código y las revisiones. |
| Despliegue | Vercel y Render | Publicar el frontend y el backend. |

### Limitaciones y seguridad
- Los planes gratuitos pueden tener restricciones en recursos, almacenamiento y disponibilidad.
- La aplicación dependerá de la conexión a Internet y de los servicios utilizados.
- La interfaz deberá ser probada en diferentes dispositivos y navegadores.
- Las credenciales se almacenarán en variables de entorno y las operaciones sensibles se validarán en el servidor.
- Los cambios en el código se revisarán mediante Pull Requests antes de ser integrados.

### Viabilidad del frontend y la infraestructura
La arquitectura propuesta permite desarrollar el MVP utilizando tecnologías compatibles y servicios en la nube a bajo coste. Esta elección es adecuada para una primera versión, aunque será necesario verificar los recursos disponibles y las limitaciones de los servicios durante el desarrollo.

**Documentación oficial**
- [Vite](https://vite.dev/guide/)
- [Vercel](https://vercel.com/docs/plans/hobby)
- [Render](https://render.com/docs/free)
- [MongoDB Atlas](https://www.mongodb.com/docs/atlas/reference/limits/)

## 5. Requisitos técnicos: backend y base de datos

### Backend (Node.js y Express)
El backend se encargará de gestionar las peticiones de los usuarios, los anuncios, las conversaciones y la comunicación con la base de datos. Para desarrollarlo utilizaremos Node.js y Express, ya que permiten crear un servidor y una API para conectar con el frontend.

Para facilitar el desarrollo utilizaremos algunas bibliotecas adicionales:

- **Mongoose:** para conectar con MongoDB y organizar los datos.
- **bcrypt:** para proteger las contraseñas de los usuarios.
- **JWT:** para gestionar la autenticación y controlar el acceso a las funciones privadas.

**Autenticación y roles**

La plataforma necesitará un sistema de registro e inicio de sesión para proteger las cuentas y las conversaciones. Habrá dos roles principales:

- **Usuarios:** podrán publicar anuncios, buscar piezas y contactar con vendedores.
- **Administradores:** podrán revisar las alertas de posibles fraudes y gestionar incidencias.

**API REST**

La API permitirá comunicar el frontend con el backend y realizar las operaciones principales de la aplicación. Algunas de las rutas previstas serán:

- `POST /api/auth/register`: registrar nuevos usuarios.
- `POST /api/auth/login`: iniciar sesión.
- `GET /api/listings`: buscar y filtrar recambios.
- `POST /api/listings`: publicar anuncios.
- `GET /api/conversations`: consultar las conversaciones.
- `POST /api/conversations/:id/messages`: enviar mensajes.
- `POST /api/alerts`: crear alertas de stock.
- `GET /api/moderation/alerts`: consultar alertas de moderación.

**Servicios externos**

Una de las características principales de la plataforma será la inteligencia artificial para detectar posibles estafas o comportamientos sospechosos en los chats. Para ello, se podría integrar una API de IA que analice los mensajes y genere avisos para los moderadores.

Todavía habría que elegir el servicio y comprobar su límite gratuito. Si su uso no resulta viable, se podría comenzar con reglas básicas para detectar mensajes sospechosos.

### Base de datos (MongoDB Atlas)
Utilizaremos MongoDB Atlas para almacenar los usuarios, anuncios, conversaciones y demás información de la aplicación. Al ser una base de datos documental, permite guardar las características de los recambios de forma flexible.

Se proponen las siguientes colecciones principales:

- **users:** datos de los usuarios, como nombre, correo electrónico, contraseña protegida, rol y fecha de registro.
- **listings:** anuncios, con título, descripción, vendedor, marca, modelo, año, referencia OEM, precio y estado de la pieza.
- **conversations:** conversaciones entre compradores y vendedores, con los participantes y el anuncio relacionado.
- **messages:** contenido de los mensajes, su autor, la conversación a la que pertenecen y la fecha de envío.
- **stockAlerts:** alertas de búsqueda configuradas por los usuarios, con los datos de la pieza que desean encontrar.
- **moderationAlerts:** avisos generados cuando se detectan posibles fraudes o comportamientos sospechosos.
- **reviews:** valoraciones y comentarios que los usuarios hacen sobre otros usuarios.

Las colecciones se relacionarán mediante identificadores. Por ejemplo, cada anuncio estará asociado a su vendedor y cada mensaje a una conversación. De esta forma podremos consultar la información relacionada sin duplicar todos los datos.

También será necesario validar la información introducida, proteger las contraseñas y comprobar los permisos para evitar que los usuarios accedan a conversaciones o anuncios que no les corresponden.

### Viabilidad del backend y la base de datos
Consideramos que el backend y la base de datos son viables con las tecnologías elegidas. Para reducir la complejidad, desarrollaremos primero el registro de usuarios, la publicación de anuncios y las búsquedas. Después incorporaremos la mensajería y, por último, la moderación mediante inteligencia artificial.

Así podremos disponer de una primera versión funcional sin depender desde el principio de las funcionalidades más complejas.

## 6. Evaluación de las capacidades del equipo

### Inventario de capacidades técnicas personales

| Tecnología | Gonzalo | Ismael | Óscar | Laura |
| :--- | :---: | :---: | :---: | :---: |
| **Kotlin / Python / SQL** | ✅ | ✅ | ✅ | ✅ |
| **HTML / CSS** | ✅ | ✅ | ✅ | ✅ |
| **Java** | ✅ | Básico | Básico | Básico |
| **JavaScript** | Básico | ❌ | ✅ | ❌ |
| **Spring Boot / Laravel / PHP** | ✅ | ❌ | ❌ | ❌ |
| **Android Studio** | ✅ | ❌ | ❌ | ❌ |
| **MongoDB** | ❌ | ❌ | ✅ | ❌ |
| **Testing (Kotlin)** | ❌ | ❌ | ✅ | ❌ |
| **Figma** | ✅ | ❌ | ✅ | ❌ |

### Lagunas de conocimiento (qué toca aprender)
- **JavaScript y Node.js:** solo Óscar sabe JavaScript en cliente y nadie tiene experiencia en **Node.js**. Tocará aprender desde cero el entorno de ejecución en servidor, la gestión de paquetes (`npm`) y la programación asíncrona.
- **Trabajo con APIs (REST):** necesitaremos aprender a diseñar endpoints, manejar peticiones y respuestas en formato JSON, códigos de estado HTTP y el consumo desde el frontend (`fetch`).
- **Docker y contenedorización:** ningún miembro domina la creación de contenedores (`Dockerfile`, `docker-compose`) para estandarizar el entorno de desarrollo y la base de datos entre los cuatro.
- **Despliegue de la aplicación:** falta experiencia en pasar el proyecto de local a producción (configuración de servidores, variables de entorno, hosting en la nube y CI/CD básico).
- **Frameworks de backend y testing:** hay dependencia de un solo miembro (Gonzalo en Spring y Laravel, Óscar en testing y MongoDB). El resto deberá aprender las bases si se incluyen en el stack final, para evitar cuellos de botella.

### Valoración del MVP
Sí, consideramos que el MVP es viable. Contamos con un equipo de 4 personas con conocimientos variados y óptimos, lo que nos permite avanzar rápido en el núcleo del proyecto mientras asumimos la curva de aprendizaje de las nuevas tecnologías sin bloquear el desarrollo.

## 7. Identificación y mitigación de riesgos técnicos

| # | Riesgo potencial | Estrategia de mitigación (sencilla y temporal) |
| :--- | :--- | :--- |
| **1** | **Bloqueo en frameworks / Node.js:** que el equipo se atasque aprendiendo el entorno de servidor nuevo. | **Plantilla base ("copiar y pegar"):** Gonzalo y Óscar crean un único controlador y ruta de ejemplo funcional el primer día. El resto solo tiene que duplicar ese archivo y cambiar los nombres para sus tareas. |
| **2** | **Retraso conectando frontend y API:** que el backend tarde en estar listo y frene a los que hacen las vistas. | **Datos falsos (JSON local):** mientras la API no esté lista, el frontend trabajará leyendo un archivo `.json` estático con datos de prueba para no detener la maquetación. |
| **3** | **Fallos con Docker o base de datos local:** perder días porque a alguien no le arranca el contenedor o el gestor SQL. | **BD en la nube compartida o SQLite temporal:** si Docker da problemas el primer día, usaremos una base de datos gratuita en la nube (o un archivo local simple) para programar rápido y dejaremos Docker para el final. |
| **4** | **Caída o fallo del despliegue a última hora:** no saber subir la web a un servidor real el día antes de la entrega. | **PaaS automático desde la semana 2:** conectar el repositorio a un servicio gratuito de despliegue en 1 clic (como Render o Vercel) al principio. Si el servidor falla el día de la presentación, tener preparado un túnel local (Ngrok) o un vídeo de respaldo. |
| **5** | **Conflictos graves en Git:** pisar el código de los compañeros al tocar los mismos archivos a la vez. | **Un archivo por persona y copias diarias:** dividir el trabajo en carpetas y archivos separados (cada uno su pantalla) y hacer `merge` todos juntos en clase 10 minutos antes de irnos. |
| **6** | **Falta de tiempo por bugs complejos:** quedarse atascado días en un error (por ejemplo, login complejo o subida de fotos). | **Regla de las 2 horas:** si algo lleva más de 2 horas dando error, se solicita la ayuda de un compañero. |
