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
* Negociación mediante chat integrado.
* Consulta de perfiles de fiabilidad, valoraciones e historial de transacciones.
* Panel de moderación activo para que los administradores intervengan ante incidencias graves.
* Posibilidad de realizar amigos
* Mapa con usuarios online
* Filtrado de mapa mediante amistades y poder ocultar tu estado en linea a los demás usuarios

### Competidores
1. *Wallapop / Milanuncios:* Gran volumen de usuarios, pero sin filtros técnicos mecánicos ni moderación activa contra fraudes en chats.
2. *Oscaro / Autodoc:* Buen catálogo estructurado, pero limitado a piezas nuevas de consumo masivo, sin mercado de segunda mano ni particulares.
3. *RecambioVerde / EcoOpArts:* Especializados en desguaces (CAT), pero excluyen el trato, compraventa o intercambio directo entre particulares y restauradores.
* **Valor diferencial:** Marketplace vertical especializado con catálogo técnico y supervisión inteligente de conversaciones mediante IA para garantizar tratos seguros.

### Propuesta de valor
Plataforma web móvil que conecta a particulares, aficionados y profesionales para la búsqueda, compraventa e intercambio de recambios de coche con precisión técnica y un entorno protegido por IA frente a fraudes y disputas.

## Fase 2 · Viabilidad técnica

### Introducción
En esta fase estudiamos la viabilidad técnica del proyecto, definiendo sus funcionalidades principales, las tecnologías que utilizaremos, las capacidades del equipo y los riesgos que pueden surgir durante el desarrollo.

### Requisitos técnicos y MVP
El proyecto se desarrollará como una aplicación web móvil basada en una arquitectura cliente-servidor. Utilizaremos **React** para el frontend, **Node.js y Express** para el backend y **MongoDB Atlas** como base de datos, siguiendo una arquitectura MERN.

El **MVP (Producto Mínimo Viable)** se centrará en ofrecer las funcionalidades esenciales para que los usuarios puedan encontrar recambios compatibles y contactar con vendedores de forma más segura. Incluirá:

- Registro e inicio de sesión de usuarios.
- Publicación de anuncios de recambios con sus características técnicas.
- Búsqueda de piezas mediante filtros por marca, modelo, año y referencia.
- Mensajería privada entre compradores y vendedores.
- Supervisión de las conversaciones mediante inteligencia artificial para detectar posibles fraudes y generar avisos para moderación.

Como funcionalidades adicionales, se prevé incorporar alertas de stock, perfiles con valoraciones y un panel de moderación para gestionar las incidencias detectadas. Estas características se desarrollarán después de completar las funciones esenciales del MVP.

### Viabilidad y recursos
Consideramos que el proyecto es viable para nuestro equipo de cuatro personas, ya que contamos con conocimientos de programación y desarrollo web que servirán como base. Sin embargo, tendremos que ampliar nuestros conocimientos en JavaScript, Node.js, APIs REST, despliegue y trabajo con MongoDB.

Para reducir la complejidad, desarrollaremos las funcionalidades de forma progresiva, comenzando por el registro, los anuncios y las búsquedas, y continuando con la mensajería y la detección de posibles fraudes. Utilizaremos herramientas como GitHub para organizar el trabajo y servicios como Vercel y Render para el despliegue.

### Riesgos técnicos
Los principales riesgos son la curva de aprendizaje de las nuevas tecnologías, los retrasos en la conexión entre frontend y backend, los problemas de despliegue y los conflictos al trabajar en equipo. Para reducirlos, utilizaremos plantillas de código, datos de prueba, despliegues tempranos y una organización del trabajo mediante ramas y Pull Requests.

En conclusión, el proyecto es técnicamente viable si priorizamos las funcionalidades esenciales y dejamos las características complementarias para etapas posteriores, asegurando primero una versión funcional del marketplace.

## Fase 3 · Objetivos y alcance

### Introducción
En esta fase definimos qué queremos conseguir y hasta dónde vamos a llegar. Fijamos un objetivo general y cuatro objetivos específicos medibles sobre la búsqueda técnica de recambios, el mapa de usuarios, el contacto entre usuarios y la detección de fraudes mediante IA, junto con la forma de comprobar cada uno antes de la defensa final. Después delimitamos el alcance: plataforma, usuarios y datos de las demos, lo que dejamos fuera y las ampliaciones futuras.

### Objetivos
* **Objetivo general:** Que cualquier persona que necesite un recambio de coche pueda encontrar la pieza compatible, localizar a vendedores cercanos en un mapa y negociar su compra sin riesgo de estafa.
* **Objetivos específicos:** todos son SMART y se comprobarán antes de la defensa final.

| Objetivo | Qué se mide | Valor de éxito | Cómo se comprueba |
|---|---|---|---|
| Encontrar una pieza compatible con los filtros técnicos en menos de 2 minutos | Tiempo hasta encontrar la pieza | Al menos 4 de 5 personas lo logran | Prueba cronometrada con 5 personas ajenas al equipo |
| Mostrar correctamente la ubicación de los usuarios en el mapa de Google Maps | Perfiles que aparecen en su ubicación correcta | Al menos 9 de 10 cuentas bien ubicadas | Demo con 10 cuentas de prueba en distintas direcciones |
| Abrir un chat con otro usuario desde el mapa a la primera y sin ayuda | Usuarios que completan el flujo sin equivocarse de pantalla | Al menos 4 de 5 usuarios (80 %) | Observación de 5 personas ajenas al equipo usando la app por primera vez |
| Detectar intentos de estafa en el chat y generar el aviso para moderación | Mensajes fraudulentos detectados y falsos avisos | Al menos 8 de 10 fraudulentos detectados y como máximo 2 falsos avisos en 10 mensajes normales | Guion de 20 mensajes simulados (pago adelantado por Bizum, pago externo, insultos) en una demo |

### Alcance
* **MVP:** El recorrido del MVP y la priorización MoSCoW están desarrollados en la Fase 2. El mapa de usuarios forma parte del proyecto y sirve para localizar vendedores cercanos y abrir un chat con ellos.
* **Plataforma:** Solo web adaptada al móvil (mobile-first), no app nativa. El uso principal será desde el móvil, y una web evita el tiempo de desarrollo y la publicación en tiendas de aplicaciones.
* **Usuarios y datos:**
  * Entre 10 y 15 cuentas de prueba, para validar el mapa, el catálogo y la mensajería.
  * Zona regional de España, para simular búsquedas de proximidad en el mapa.
  * Todos los datos son de prueba (perfiles, anuncios, fotos, fichas técnicas y chats), sin exponer datos reales. Los chats para probar la IA serán conversaciones simuladas.

### Lo que no haremos
| Qué | Por qué |
|---|---|
| Pasarela de pagos en línea / depósito retenido | Aumenta la complejidad técnica y legal; el pago se acuerda directamente entre las partes. |
| Gestión de envíos e integración logística | Priorizamos la búsqueda y el contacto local; los envíos se acuerdan de forma privada. |
| Aplicación móvil nativa (Android / iOS) | Supone más tiempo de desarrollo y subida a tiendas; la web adaptable cubre el uso en móvil. |
| Verificación automática por número de bastidor (VIN) | Requiere APIs automotrices de pago fuera del alcance del proyecto. |

### Ampliaciones futuras
Ordenadas como hoja de ruta, de lo primero que haríamos a lo último:
1. **Panel activo de moderación:** interfaz para que los administradores gestionen los avisos e incidencias generados por la IA.
2. **Alertas de stock:** aviso automático cuando se publique una pieza que coincida con una búsqueda guardada.
3. **Pasarela de pago:** retención del dinero hasta comprobar la recepción y compatibilidad de la pieza.
4. **Verificación técnica por bastidor (VIN):** decodificación automática de los datos del vehículo.
