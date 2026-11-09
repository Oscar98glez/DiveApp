# DiveApp

Bitácora de inmersiones de buceo con un globo terráqueo interactivo.

- **Globo**: arrastra para girarlo, rueda o botones +/− para el zoom. Los continentes donde has buceado se ven en color arena y cada punto rojo es un sitio de buceo.
- **Pulsa un continente** para ver sus inmersiones y estadísticas (número, tiempo bajo el agua, profundidad máxima, temperatura media).
- **Pulsa una inmersión** para ver la ficha completa con el perfil de profundidad, gas, condiciones, equipo, vida marina y validación.
- **Nueva inmersión**: formulario con todos los datos de un logbook (ver abajo). Calcula solo el tiempo (con hora de entrada/salida), el continente (con las coordenadas), la MOD del Nitrox y el consumo SAC.

Los datos se guardan en el navegador (`localStorage`). Al abrirla por primera vez aparecen inmersiones de ejemplo que se pueden quitar.

## Cómo abrirla

Abre `index.html` en el navegador (necesita conexión para cargar D3 y las fuentes).

## Datos que se registran

| Sección | Campos |
| --- | --- |
| Datos generales | Nº de inmersión, fecha, hora de entrada y salida, punto de buceo, zona, país, continente, latitud y longitud |
| Profundidad y tiempo | Profundidad máxima y media, tiempo total, intervalo en superficie, parada de seguridad (profundidad y duración), paradas de descompresión |
| Gas y botella | Mezcla (aire, nitrox, trimix), % O₂ y He, material y volumen de la botella, presión inicial y final → consumo SAC y MOD |
| Condiciones | Temperatura del agua en superficie y en el fondo, temperatura del aire, visibilidad, corriente, estado del mar, tiempo, tipo de agua |
| Tipo de inmersión | Entrada (barco, orilla…), actividad (arrecife, pecio, nocturna, deriva, cueva, profunda, pared, foto, formación, fauna grande) |
| Equipo y personas | Traje, lastre, ordenador, centro de buceo, compañero/a, guía o instructor |
| Experiencia | Vida marina vista, valoración (1–5 estrellas), notas |
| Validación | Certificación usada, firma / sello del instructor o centro |

## Estructura

- `index.html` – la app (HTML, CSS y JS).
- `js/continents.js` – contornos de los continentes (Natural Earth 1:110m, dominio público).
