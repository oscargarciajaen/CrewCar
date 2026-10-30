# Fase 3 · Objetivos y alcance · Grupo 3

## Introducción
En esta fase definimos qué queremos conseguir y hasta dónde vamos a llegar. Fijamos un objetivo general y cuatro objetivos específicos medibles sobre la búsqueda técnica de recambios, el contacto entre usuarios y un mapa dónde puedes ver dónde se encuentran los usuarios de la aplicación que tengan la función activada, con la posibilidad de filtrar por amigos. Después delimitamos el alcance: plataforma, usuarios y datos de las demos, lo que dejamos fuera y las ampliaciones futuras.

## 1. Objetivos

### Objetivo general
Que cualquier persona que necesite un recambio de coche pueda encontrar la pieza compatible, localizar a vendedores cercanos en un mapa y negociar su compra sin riesgo de estafa.

### Objetivos específicos

| ID | Objetivo SMART | Qué se mide | Valor de éxito | Cómo se comprueba |
| :--- | :--- | :--- | :--- | :--- |
| 01 | Que un usuario encuentre una pieza compatible con los filtros técnicos en menos de 2 minutos, antes de la defensa final. | Tiempo hasta encontrar la pieza. | Al menos 4 de 5 personas lo logran en menos de 2 minutos. | Prueba cronometrada con 5 personas ajenas al equipo. |
| 02 | Que el mapa de Google Maps muestre correctamente la ubicación de los usuarios de prueba, antes de la defensa final. | Porcentaje de perfiles que aparecen en su ubicación correcta. | Al menos 9 de 10 cuentas de prueba bien ubicadas. | Demo con 10 cuentas de prueba en distintas direcciones, comprobando cada pin. |
| 03 | Que al menos el 80 % de los usuarios consigan abrir un chat con otro usuario desde el mapa a la primera y sin ayuda, antes de la defensa final. | Porcentaje de usuarios que completan el flujo sin equivocarse de pantalla. | Al menos 4 de 5 usuarios lo logran. | Observación de 5 personas ajenas al equipo usando la app por primera vez. |

## 2. Alcance

### El MVP
El recorrido del MVP y la priorización MoSCoW están en la [Fase 2](./02-viabilidad-tecnica.md). Aquí solo añadimos que el mapa de usuarios con Google Maps forma parte del proyecto y se usa para localizar vendedores cercanos y abrir un chat con ellos.

### Plataforma
Solo web adaptada al móvil (mobile-first), no app nativa. Con nuestros objetivos, el uso principal será desde el móvil, y una web evita el tiempo de desarrollo y la publicación en tiendas de aplicaciones.

### Usuarios y datos
- **Usuarios:** entre 10 y 15 cuentas de prueba, para validar el mapa, el catálogo y la mensajería.
- **Zona:** España, centrada en una zona regional para simular búsquedas de proximidad en el mapa.
- **Datos:** todos de prueba. Perfiles, anuncios, fotos, fichas técnicas y chats son generados por nosotros, sin exponer datos reales. 
### Lo que no haremos

| Qué | Por qué |
| :--- | :--- |
| **Pasarela de pagos en línea / depósito retenido** | Aumenta la complejidad técnica y legal; el pago se acuerda directamente entre las partes. |
| **Gestión de envíos e integración logística** | Priorizamos la búsqueda y el contacto local; los envíos se acuerdan de forma privada. |
| **Aplicación móvil nativa (Android / iOS)** | Supone más tiempo de desarrollo y subida a tiendas; la web adaptable cubre el uso en móvil. |
| **Verificación automática por número de bastidor (VIN)** | Requiere APIs automotrices de pago fuera del alcance del proyecto. |

### Ampliaciones futuras
Ordenadas como hoja de ruta, de lo primero que haríamos a lo último:

1. **Alertas de stock:** aviso automático cuando se publique una pieza que coincida con una búsqueda guardada.
2. **Pasarela de pago:** retención del dinero hasta comprobar la recepción y compatibilidad de la pieza.
3. **Verificación técnica por bastidor (VIN):** decodificación automática de los datos del vehículo.
