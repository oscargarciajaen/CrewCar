# Viabilidad Técnica

## Requisitos Funcionales 

- El usuario puede realizar una búsqueda técnica avanzada, filtrando por marcas, modelo, año, categoría o referencia.

- El usuario puede añadir alerta de stock personalozadas para que el avisen cuando la pieza que esté buscando esté disponible.

- El usuario puede utilizar las mensajería directa integrada para comunicarse de forma directa con otros usarios.

- La IA analiza en segundo plano las conversaciones entre usuarios para detectar casos de estafas, comportaminetos sospechosos o lenguaje agresivo.

- El sistema emite alertas automáticas al equipo de moderación cuando la IA detecta un riesgo o anomalía en las conversaciones

- El usuario puede consultar el perfil de vendedores o compradores, revisando su historial, valoraciones y comnetarios.

- El administrador puede acceder a un panel de moderación activo para gestionar los avisos prioritarios generado por la IA, interviniendo o mediando en las incidencias.

## Priorización MoSCoW

### Must Have

- El usuario puede crear una cuenta nueva y puede acceder

- El usuario puede publicar un anuncio de un apieza con sus detalles básicos

- El usuario puede buscar recambios aplicando filtros técnicos

- El usuario puede creac una conversación privada para negociar la compra

- La IA puede auditar las conversaciones en segundo plano para detectar fraudes y avisar a moderación

### Should Have

- El usuario puede activar una alerta de stock para piezas difíciles de encontrar

- El usuario puede consultar el perfil y las valoraciones de fiabilidad de otros usuarios

- El administrador puede acceder al panel de moderación activo para gestionar incidencias

### Could Have

- El usuario puede editar o eliminar sus anuncios publicados

- El usuario puede marcar transacciones como finalizadas y dejar valoraciones detalladas

### Won´t Have

- Sistema integrado de pasarela de pago en línea con depósito retenido

- Aplicación móvil nativa independiente para iOS y Android

## MVP

El MVP de nuestra aplicación es el recorrido mínimo para que un usuario pueda encontrar y comprar la pieza exacta wue necesita sin riesgo de estafa: el usuario entra, filtra el catálogo por los datos técnicos de su coche, abre un chat interno con el vendedor para negociar la compra y la IA supervisa el chat en segundo plano por si aparecen intentos de estafa o comportamientos no permitidos.

## Requisitos técnicos: frontend e infraestructura

### 1. Frontend

Vamos a utilizar **React** para crear una interfaz sencilla que se adapte tanto a móviles como a ordenadores, organizada a través de componentes reutilizables.

| **Tecnología** | **Función** |
|---|---|
| React | Construir la interfaz de usuario. |
| Vite | Facilitar el desarrollo y la compilación. |
| React Router | Manejar la navegación entre páginas. |
| Fetch API | Conectar el frontend con el backend. |
| CSS adaptable | Ajustar la interfaz a diferentes dispositivos. |

La interfaz permitirá a los usuarios buscar recambios, aplicar filtros, consultar anuncios, acceder a perfiles y utilizar la mensajería.

### 2. Arquitectura e infraestructura

La aplicación seguirá una arquitectura cliente-servidor basada en MERN. El frontend se comunicará con el backend a través de una API REST.

| **Componente** | **Tecnología** | **Función** |
|---|---|---|
| Frontend | React | Presentar la interfaz. |
| Backend | Node.js y Express | Manejar las peticiones y la lógica. |
| Base de datos | MongoDB Atlas | Almacenar la información. |
| Repositorio | GitHub | Gestionar el código y las revisiones. |
| Despliegue | Vercel y Render | Publicar el frontend y el backend. |

### 3. Limitaciones y seguridad

- Los planes gratuitos pueden tener restricciones en recursos, almacenamiento y disponibilidad.
- La aplicación dependerá de la conexión a Internet y de los servicios utilizados.
- La interfaz deberá ser probada en diferentes dispositivos y navegadores.
- Las credenciales se almacenarán en variables de entorno y las operaciones sensibles se validarán en el servidor.
- Los cambios en el código se revisarán mediante Pull Requests antes de ser integrados.

### 4. Viabilidad técnica

La arquitectura propuesta permite desarrollar el MVP utilizando tecnologías compatibles y servicios en la nube a bajo coste. Esta elección es adecuada para una primera versión, aunque será necesario verificar los recursos disponibles y las limitaciones de los servicios durante el desarrollo.

**Documentación oficial:**
- Vite: https://vite.dev/guide/
- Vercel: https://vercel.com/docs/plans/hobby
- Render: https://render.com/docs/free
- MongoDB Atlas: https://www.mongodb.com/docs/atlas/reference/limits/

## Evaluación de las capacidades del equipo

### 1. Inventario de capacidades técnicas personales

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

### 2. Lagunas de Conocimiento (Qué toca aprender)

* **JavaScript y Node.js:** Solo Óscar sabe JS en cliente y nadie tiene experiencia en **Node.js**. Tocará aprender desde cero el entorno de ejecución en servidor, gestión de paquetes (`npm`) y programación asíncrona.
* **Trabajo con APIs (REST):** Necesitaremos aprender a diseñar endpoints, manejar peticiones/respuestas en formato JSON, códigos de estado HTTP y consumo desde el frontend (`fetch`).
* **Docker y Contenedorización:** Ningún miembro domina la creación de contenedores (`Dockerfile`, `docker-compose`) para estandarizar el entorno de desarrollo y la base de datos entre los cuatro.
* **Despliegue de la Aplicación:** Falta experiencia en pasar el proyecto de local a producción (configuración de servidores, variables de entorno, hosting cloud y CI/CD básico).
* **Frameworks Backend y Testing:** Dependencia en un solo miembro (Gonzalo en Spring/Laravel y Óscar en Testing/MongoDB). El resto deberá aprender las bases si se incluyen en el stack final para evitar cuellos de botella.

### 3. Valoración del MVP

Sí, consideramos que el MVP es viable. Contamos con un equipo de 4 personas con unos conocimientos variados y optimos, lo que nos permite avanzar rápido en el núcleo del proyecto mientras asumimos la curva de aprendizaje de las nuevas tecnologías sin bloquear el desarrollo.


## 4. Identificación y Mitigación de Riesgos Técnicos

| # | Riesgo Potencial | Estrategia de Mitigación (Sencilla y Temporal) |
| :--- | :--- | :--- |
| **1** | **Bloqueo en Frameworks / Node.js:** Que el equipo se atasque aprendiendo el entorno de servidor nuevo. | **Plantilla base ("Copiar y pegar"):** Gonzalo y Óscar crean un único controlador y ruta de ejemplo funcional el primer día. El resto solo tiene que duplicar ese archivo y cambiar los nombres para sus tareas. |
| **2** | **Retraso conectando Frontend y API:** Que el Backend tarde en estar listo y frene a los que hacen las vistas. | **Datos falsos (JSON local):** Mientras la API no esté lista, el Frontend trabajará leyendo un archivo `.json` estático con datos de prueba para no detener la maquetación. |
| **3** | **Fallos con Docker o Base de Datos local:** Perder días porque a alguien no le arranca el contenedor o el gestor SQL. | **BD en la nube compartida o SQLite temporal:** Si Docker da problemas el primer día, usaremos una base de datos gratuita en la nube (o un archivo local simple) para programar rápido y dejaremos Docker para el final. |
| **4** | **Caída o fallo del despliegue a última hora:** No saber subir la web a un servidor real el día antes de la entrega. | **PaaS automático desde la Semana 2:** Conectar el repositorio a un servicio gratuito de despliegue en 1 clic (como Render o Vercel) al principio. Si el servidor falla el día de la presentación, tener preparado un túnel local (Ngrok) o vídeo de respaldo. |
| **5** | **Conflictos graves en Git:** Pisar el código de los compañeros al tocar los mismos archivos a la vez. | **Un archivo por persona y copias diarias:** Dividir el trabajo en carpetas/archivos separados (cada uno su pantalla) y hacer `merge` todos juntos en clase 10 minutos antes de irnos. |
| **6** | **Falta de tiempo por bugs complejos:** Quedarse atascado días en un error (ej. login complejo o subida de fotos). | **Regla de las 2 horas:** Si algo lleva más de 2 horas dando error, se solicita la ayuda de un compañero. |

