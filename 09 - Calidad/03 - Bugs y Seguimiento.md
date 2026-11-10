# Bugs y seguimiento

## Abiertos en `bf6203d`

Encontrados al revisar el código para este GDD. Ninguno impide terminar la demo.

| ID | Prioridad | Descripción | Dónde | Corrección propuesta |
| --- | --- | --- | --- | --- |
| B-01 | Medio | `Continuar` no guarda en los pisos 5, 6 y 7 | `Progreso.Ruta` | Añadir `"Cueva", "Lago", "Nevado"` |
| B-02 | Medio | La fuente de curación no responde al mando | `HealingShrine.Update` solo lee la tecla `E` | Añadir `buttonNorth`, como en `LoreNote` |
| B-03 | Medio | Los modos anuncian "Daño recibido" y "Curación" que no se aplican | `Difficulty.damageTaken`, `healing` sin uso | Aplicarlos en `PlayerHealth` o quitar el texto |
| B-04 | Bajo | Textos que hablan de bajar pisos | `Historia.Abismo[1]`; placas de los pisos 1 y 8; tutorial ("había bajado tanto") | Cambiar a "subir" |
| B-05 | Bajo | Consejo de carga sobre el mercader y los minerales | `Cargador` | Quitarlo |
| B-06 | Bajo | El aviso `E · Usar la fuente de curación` no muestra botón de mando | `FloorDirector` | Junto con B-02 |
| B-07 | Bajo | La barra del jefe dibuja marcas al 66 % y 33 %, que Dante no usa | `FloorDirector` | Ocultarlas para Dante o marcar el 50 % |
| B-08 | Bajo | Abrir la pausa no tiene botón de mando documentado | `PauseMenu` | Verificar y documentar |

## Cerrados durante el desarrollo

| Fecha | Bug | Solución |
| --- | --- | --- |
| 1–2 nov | Las larvas se veían al revés hacia la izquierda | El material ignora `flipX`; el espejo se hace con la escala |
| 1–2 nov | El enemigo miraba a un lado y la franja apuntaba a otro | Mira hacia donde va a atacar |
| 1–2 nov | Abby cambiaba de tamaño entre poses | El importador calcula el tamaño; ya no fuerza 64 px por unidad |
| 1–2 nov | La cámara atravesaba el terreno y se pegaba a la cara de Abby | Sube sobre el terreno; no se acerca por obstáculos |
| 1–2 nov | La bahía de Cala Sombría era pasto | El fondo del mar tapaba el agua; corregido |
| 1–2 nov | El portal parecía no funcionar | `FloorExit` vuelve a buscar a Abby |
| 1–2 nov | En el ejecutable se apagaba el posproceso | URP ya no recorta esos recursos |
| 1–2 nov | La música trababa al empezar cada horda | Se compone en otro hilo |
| 2 nov | Abby se quedaba atorada bajo el terreno | `FallGuard` la devuelve al camino |
| 4 nov | Casas en medio de la Calle Mayor | Corregido en `ExteriorBuilder` |
| 5 nov | La cámara subía para no meterse al suelo y nunca bajaba | Corregido |
| 5 nov | Superficies encimadas que parpadeaban | Menú `Abby/Separar superficies encimadas` |
| 6 nov | Franja negra en el horizonte de la Cima y el final | Horizonte nuevo |

## Cómo registrar un bug

| Campo | Contenido |
| --- | --- |
| ID | `B-NN` |
| Prioridad | Bloqueante, alto, medio o bajo ([[01 - Criterios de Calidad]]) |
| Escena | Nombre de la escena |
| Pasos | Qué hacer para que ocurra |
| Esperado / Obtenido | Una línea cada uno |
| Evidencia | Captura o clip en `Media/Capturas/Bugs/` |
| Estado | Abierto, corregido en `<commit>`, o aceptado para la demo |
