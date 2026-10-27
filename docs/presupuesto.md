# Presupuesto

## Introducción
Calculamos el coste del proyecto a partir de las horas de trabajo. Estimamos las horas de cada tarea antes de empezar, medimos las horas reales con Toggl Track y al final de cada sprint comparamos las dos cosas.

## 1. Cómo estimamos
- Cada tarea se estima en el Sprint Planning con Planning Poker (1, 2, 3, 5, 8, 13).
- La estimación se guarda en el campo "Estimación (horas)" de GitHub Projects.
- Cada persona registra su tiempo en Toggl Track, con el nombre del issue en la descripción.
- Al cerrar el sprint calculamos las horas reales, el coste real y la desviación.

## 2. Coste por hora

Los cuatro somos estudiantes, así que todos tenemos perfil Junior y usamos el mismo precio.

| Persona | Perfil | €/hora |
|---|---|---|
| Gonzalo | Junior | 20 € |
| Óscar | Junior | 20 € |
| Laura | Junior | 20 € |
| Ismael | Junior | 20 € |

## 3. Horas estimadas por sprint

| Sprint | Gonzalo | Óscar | Laura | Ismael | Total |
|---|---|---|---|---|---|
| 1. Setup y arquitectura | 9 | 9 | 8 | 8 | 34 |
| 2. Autenticación y roles | 8 | 9 | 9 | 8 | 34 |
| 3. Funcionalidades (parte 1) | 9 | 8 | 9 | 8 | 34 |
| 4. Funcionalidades (parte 2) | 9 | 9 | 8 | 8 | 34 |
| 5. Testing y optimización | 8 | 8 | 8 | 10 | 34 |
| 6. Despliegue y documentación | 8 | 8 | 8 | 10 | 34 |
| **Total** | **51** | **51** | **50** | **52** | **204** |

## 4. Coste estimado por sprint

| Sprint | Gonzalo | Óscar | Laura | Ismael | Total |
|---|---|---|---|---|---|
| 1 | 180 € | 180 € | 160 € | 160 € | 680 € |
| 2 | 160 € | 180 € | 180 € | 160 € | 680 € |
| 3 | 180 € | 160 € | 180 € | 160 € | 680 € |
| 4 | 180 € | 180 € | 160 € | 160 € | 680 € |
| 5 | 160 € | 160 € | 160 € | 200 € | 680 € |
| 6 | 160 € | 160 € | 160 € | 200 € | 680 € |
| **Total** | **1.020 €** | **1.020 €** | **1.000 €** | **1.040 €** | **4.080 €** |

## 5. Estimación frente a realidad
Esta tabla se actualiza al final de cada sprint con los datos de Toggl.

| Sprint | Horas estimadas | Horas reales | Desviación | Coste estimado | Coste real |
|---|---|---|---|---|---|
| 1 | 34 | | | 680 € | |
| 2 | 34 | | | 680 € | |
| 3 | 34 | | | 680 € | |
| 4 | 34 | | | 680 € | |
| 5 | 34 | | | 680 € | |
| 6 | 34 | | | 680 € | |
| **Total** | **204** | | | **4.080 €** | |

### Tareas que han llevado más tiempo del previsto

| Sprint | Tarea | Estimado | Real | Por qué | Qué cambiamos |
|---|---|---|---|---|---|
| | | | | | |

## 6. Costes adicionales

| Concepto | Coste |
|---|---|
| Vercel, Render y MongoDB Atlas (planes gratuitos) | 0 € |
| Google Maps, Cloudinary, Toggl, GitHub y Bitwarden (planes gratuitos) | 0 € |
| Dominio | 12 € al año |
| Licencias de software | 0 € |
| Marketing | 0 € |
| **Total** | **12 €** |

## 7. Presupuesto total

| Concepto | Importe |
|---|---|
| Desarrollo (204 horas) | 4.080 € |
| Costes adicionales | 17 € |
| **Total estimado** | **4.092 €** |
