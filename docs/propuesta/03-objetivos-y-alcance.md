# Fase 3 · Objetivos y alcance · <estudio>
## Introducción
## 1. Objetivos
### Objetivo general
Conseguir que particulares y profesionales puedan encontrar recambios de coche compatibles y conectar con otros usuarios cercanos mediante filtros técnicos y un mapa interactivo con Google Maps.
### Objetivos específicos
| ID | Objetivo SMART | Qué se mide | Valor de éxito | Cómo se comprueba |
| :--- | :--- | :--- | :--- | :--- |
| 01 | Que un usuario sea capaz de encontrar una pieza compatible usando los filtros técnicos en menos de 2 minutos | El tiempo que tarda en encontrar la pieza | Es capaz de hacerlo en el tiempo determinado | Con testers elegidos al azar en una prueba cronometrada |
| 02 | Que el sistema de alertas de stock envíe la notificación correcta en al menos el 90% de las coincidencias publicadas | Porcentaje de alertas enviadas respecto al total de piezas coincidentes subidas | Al menos 9 de cada 10 alertas se envían sin fallos (90%) | Registro de errores simulando la subida de 10 piezas con el equipo |
| 03 | Que el mapa de Google Maps muestre sin errores de ubicación al 100% de los usuarios registrados en una zona | Porcentaje de perfiles geolocalizados correctamente en el mapa | 0 errores al cargar los pines de ubicación en el mapa | Comprobando en una demo con 10 cuentas de prueba en distintas direcciones |
| 04 | Que al menos el 80% de los usuarios consigan abrir un chat desde el perfil del mapa en su primer intento sin ayuda | Porcentaje de usuarios que completan el flujo sin equivocarse de pantalla | Al menos 4 de cada 5 usuarios lo logran a la primera | Observando a 5 personas reales usar el mapa por primera vez |
## 2. Alcance
### El MVP          ([enlace a la fase 2](./02-viabilidad-tecnica.md))
### Plataforma

La plataforma elegida es móvil, será una aplicació web móvil, se debe a que teniendo en cuenta nuestros objetivos y funciones que tenemos planeadas para la aplicación, encaja m´´as en plataformas móviles.

### Usuarios y datos

Estimación de Usuarios: Se trabajará con un volumen de 10 a 15 cuentas de usuario de prueba, para ser capaces de validar el comportamiento del mapa, el catálogo y la mensajería.

Origen: El oigen de los usuarios será España, enfocados en una zona regional para poder simular búsquedas de proximidad en el mapa.

Origen de los datos: Se utilizarán datos de prueba. Los perfiles, publicaciones de piezas, fotografías, fichas técnicas y chats serán generados con datos de prueba para verificar los filtros, el corecto funcionamiento de las alertas y la geolocalización sin exponer datos reales ni requerir ctálogo real en fase de desarrollo.

### Lo que no haremos
  | Qué | Por qué |
  | :--- | :--- |
  | **Pasarela de pagos en línea / depósito retenido** | Aumenta la complejidad técnica y legal en la fase inicial; el acuerdo económico y el pago se realizan directamente entre las partes. |
  | **Gestión de envíos e integración logística** | Priorizamos la búsqueda y el contacto local de proximidad; los envíos se acuerdan de forma privada. |
  | **Aplicación móvil nativa (Android / iOS)** | Supone mayor tiempo de desarrollo y subida a tiendas (Play Store / App Store); la web adaptable (Mobile-First) cubre el uso en móviles desde el navegador. |
  | **Verificación automática por número de bastidor (VIN)** | Integrar la decodificación automática por bastidor requiere contratar APIs automotrices de pago fuera del alcance inicial del proyecto. |
### Ampliaciones futuras   (lista numerada, en orden)
1. Panel activo de moderación: Interfaz visual para que los administradores gestionen de forma cómoda los avisos e incidencias generados por el sistema de moderación.
2. Sistemas de alertas de stock activas: Avisos automáticos cuando se publique una pieza que coincida con una búsqueda guardada por el usuario.
3. Pasaerla de pago: Retención del dinero hasta comprobar la recepción y compatibilidad de la pieza.
4. Verificación técnica por código: Decodificación automática de los datos del vehículo a partir del número de bastidor.
