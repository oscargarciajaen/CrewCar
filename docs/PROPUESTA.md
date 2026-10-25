# Propuesta Final
## Idea Final 
### Marketplace de Recambios y Comunidad
Qué es: Es una aplicación web móvil que se utiliza para conectar a particulares, aficionados al motor y profesionales para la compraventa, intercambio o localización de piezas y recambios de coche.

Incluye:
- Mensajería directa entre usuarios, supervisada por una inteligencia artificial que analiza las conversaciones en segundo plano para detectar fraudes, discusiones o lenguaje inapropiado y emitir alertas automáticas a los administradores.
- Catálogo categorizado de piezas con filtros avanzados por marca, modelo y año.
- Sistema de alertas automáticas para piezas difíciles de encontrar.
- Panel de moderación para que los administradores gestionen las incidencias reportadas por la IA.
## Fase 1 · El problema

### Introducción
En esta fase definimos el problema principal que resuelve nuestra plataforma: la dificultad de encontrar recambios de coche compatibles y comprarlos sin riesgo de estafa. Analizamos a quién afecta, su impacto, los usuarios objetivo, los casos de uso, la competencia y la propuesta de valor.

### El Problema
* **Problema:** El mercado de recambios entre particulares y profesionales sufre fragmentación, ausencia de filtros técnicos adecuados y alto riesgo de estafas. Nuestra plataforma centraliza la oferta y demanda bajo un catálogo estructurado y un entorno seguro supervisado por inteligencia artificial.
* **¿A quién afecta?** 
  * *Restauradores y aficionados al motor:* Buscan piezas clásicas o descatalogadas con compatibilidad exacta.
  * *Propietarios particulares:* Conductores con presupuesto ajustado que temen ser estafados o comprar piezas erróneas.
  * *Mecánicos y talleres independientes:* Necesitan localizar repuestos rápidos y fiables con trazabilidad técnica.
  * *Vendedores y despiezadores:* Particulares que gestionan excedentes y sufren regateos o tratos conflictivos.
* **Frecuencia e impacto:** El problema es ocasional o continuado según la avería o proyecto, y diario en talleres. Causa vehículos parados semanas, pérdida de tiempo en portales generalistas, estafas en pagos adelantados y sobrecostes en concesionarios.
* **Evidencias:** Casos reales de compradores engañados con pagos por Bizum adelantados o envíos de piezas no compatibles sin soporte de las plataformas generalistas.

### ¿A quién le pasa?
* **Persona 1 (El restaurador / aficionado al motor):** Busca piezas muy específicas por compatibilidad técnica (marca, modelo, año, OEM) y alertas de stock. Le frustran los anuncios ambiguos y el miedo a componentes falsificados.
* **Persona 2 (El conductor con avería y presupuesto limitado):** Busca un recambio funcional al mejor precio para reparar su coche sin depender de concesionarios. Le frena su desconocimiento técnico y el riesgo de fraude.

### Casos de Uso
* Búsqueda técnica avanzada con filtros por vehículo y referencia OEM.
* Creación de alertas de stock personalizadas para piezas difíciles de encontrar.
* Negociación mediante chat integrado, supervisado en segundo plano por una IA que detecta fraudes y avisa a moderación.
* Consulta de perfiles de fiabilidad, valoraciones e historial de transacciones.
* Panel de moderación activo para que los administradores intervengan ante incidencias graves.

### Competidores
1. *Wallapop / Milanuncios:* Gran volumen de usuarios, pero sin filtros técnicos mecánicos ni moderación activa contra fraudes en chats.
2. *Oscaro / Autodoc:* Buen catálogo estructurado, pero limitado a piezas nuevas de consumo masivo, sin mercado de segunda mano ni particulares.
3. *RecambioVerde / EcoOpArts:* Especializados en desguaces (CAT), pero excluyen el trato, compraventa o intercambio directo entre particulares y restauradores.
* **Valor diferencial:** Marketplace vertical especializado con catálogo técnico y supervisión inteligente de conversaciones mediante IA para garantizar tratos seguros.

### Propuesta de valor
Plataforma web móvil que conecta a particulares, aficionados y profesionales para la búsqueda, compraventa e intercambio de recambios de coche con precisión técnica y un entorno protegido por IA frente a fraudes y disputas.

## Fase 4 · ¿Con qué y con quién?

Esta fase define **quién hace qué**, con qué tecnologías se construirá el proyecto y cómo se gestionará el trabajo. Se reparten los roles técnicos y los módulos del MVP, se concreta el stack y las herramientas, y se establece el funcionamiento del tablero, las ramas y la estructura del repositorio para comenzar a programar en la UD1. Tener claro desde el principio quién lidera cada parte evita problemas con las tareas y permite saber a quién acudir en cada apartado.

### 1. Las personas

El equipo se organiza en cuatro roles técnicos. Cada responsable coordina su área y revisa los Pull Requests relacionados con ella, aunque no tiene por qué programar todo.

| Persona | Rol | Responsabilidad |
|---|---|---|
| Gonzalo | Frontend Lead | Coordinar y revisar el desarrollo de la interfaz de usuario. |
| Oscar | Backend Lead | Coordinar y revisar la lógica del servidor y la API. |
| Laura | Database Manager | Diseñar y mantener la estructura de la base de datos y revisar su integración. |
| Ismael | QA y despliegue | Coordinar las pruebas y comprobar el correcto funcionamiento de la aplicación desplegada. |

#### Responsables por módulo

Cada módulo tiene una persona responsable y otra de apoyo. El responsable lleva el desarrollo completo —desde la base de datos hasta la pantalla— y comprueba que funciona correctamente.

| Módulo | Requisitos (RF) | Responsable | Apoyo |
|---|---|---|---|
| Usuarios y perfiles | Registro, inicio de sesión y perfiles de usuario. | Oscar | Ismael |
| Catálogo y anuncios | Publicación, consulta y búsqueda de recambios con filtros técnicos. | Gonzalo | Laura |
| Mensajería | Comunicación privada entre compradores y vendedores. | Gonzalo | Oscar |
| Moderación con IA | Análisis de las conversaciones y registro de avisos de posible fraude. | Oscar | Laura |
| Base de datos | Almacenamiento y organización de usuarios, anuncios, conversaciones y avisos. | Laura | Ismael |
| Pruebas y despliegue | Comprobación del MVP y publicación de la aplicación. | Ismael | Gonzalo |

#### Comunicación

El equipo sigue las normas de comunicación y colaboración establecidas en el [contrato del equipo](../CONTRATO.md). Los canales son **WhatsApp** y un **servidor de Discord**.

Las tareas se organizan mediante el tablero del proyecto, y los cambios de código se gestionan mediante **issues** y **Pull Requests**, que deben ser revisadas por otro compañero.

### 2. La tecnología

La aplicación utiliza la arquitectura **MERN**:

- **React + Vite**: frontend basado en componentes reutilizables y desarrollo rápido.
- **React Router**: navegación entre páginas sin recargar la aplicación.
- **Node.js + Express**: backend y API REST, usando el mismo lenguaje que el frontend.
- **MongoDB Atlas + Mongoose**: base de datos documental flexible para almacenar las características de cada pieza.
- **bcrypt + JWT**: protección de contraseñas y control de acceso a funciones privadas.
- **Vercel**: despliegue del frontend.
- **Render**: despliegue del backend.

El detalle de cada tecnología, los servicios externos y sus limitaciones está en el documento de [viabilidad técnica](02-viabilidad-tecnica.md).

### Herramientas de desarrollo

| Área | Herramientas |
|---|---|
| Pruebas del backend | Jest y Supertest |

### 3. La gestión

#### Tablero

Las tareas se organizan en el [tablero del proyecto](https://github.com/users/oscargarciajaen/projects/4/views/1). Cada tarea es una **issue** que se mueve por las columnas del tablero según su estado.

#### Ramas

- `main`: versión estable. Solo recibe un PR desde `develop` al cerrar cada sprint.
- `develop`: rama de integración. Las ramas de tarea salen de ella y vuelven a ella.
- Ramas de tarea: una por issue, con su PR hacia `develop`.

El flujo de trabajo es: **issue → rama → PR → review de un compañero → merge**. Nadie puede fusionar su propio PR; la revisión debe aprobarse antes del merge.

Las ramas `main` y `develop` están protegidas: exigen un Pull Request obligatorio con al menos una aprobación.

#### Estructura de carpetas

```text
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
