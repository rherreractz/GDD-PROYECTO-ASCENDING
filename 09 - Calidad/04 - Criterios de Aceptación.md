# Criterios de aceptación

Comportamiento esperado en `animaciones` @ `bf6203d`. Cada fila se puede comprobar jugando.

| Área | Comportamiento esperado |
| --- | --- |
| Arranque | Sin partida guardada: tarjeta de título y tutorial. Con partida: menú con `Continuar · Piso N`. |
| Menú | `Nueva partida`, `Configuración` y `Créditos` responden a mouse, teclado y mando. Salir pide confirmación. |
| Tutorial | Siete pasos en orden; el HUD dice `DANTE`; la vida no baja de 1; termina con la cinemática del Coloso y corte a negro. |
| Intro | 14 imágenes con texto que cabe; tarjeta `Año 2035` antes del discurso; se salta manteniendo `Esc`. |
| Cala Sombría | Noche; Abby llega al portal caminando y carga el Piso 1. |
| Movimiento | `5 m/s`; la diagonal no es más rápida; salta `1,2 m`; no atraviesa muros. |
| Combo | Tres clics dan `10`, `10`, `15`. Esperar más de `0,6 s` reinicia el combo. El tercer tajo empuja más. |
| Apuntado | Con un enemigo a menos de `4,2 m` y dentro de `70°`, el tajo gira hacia él. |
| Bloqueo | Clic derecho sostenido: el golpe quita el `8 %` y `20` de stamina, aparece `BLOQUEO`. Con menos de `20` de stamina no bloquea y la barra parpadea. |
| Stamina | Empieza a recuperarse `1 s` después del último gasto, a `25` por segundo. |
| Impulso | `Shift` desplaza unos `3 m`, gasta `20` de stamina y tiene `0,5 s` de recarga. Sin stamina no sale. |
| Esquiva perfecta | Impulsarse a través de un golpe muestra `¡ESQUIVA PERFECTA!`, cámara lenta y el siguiente tajo dice `¡CRÍTICO!`. |
| Tajo de impulso | Atacar al terminar el impulso muestra `¡Tajo de impulso!` y rompe la guardia del Guardián. |
| Daño recibido | Ningún golpe quita más de `15` ni menos de `8` sin bloquear. Tras un golpe hay `0,7 s` de invulnerabilidad con parpadeo. |
| Fuente | `E` cerca: vida al 100 %, cartel `FUENTE DE CURACIÓN`, queda apagada. Con vida llena: `Vida al máximo` y no se gasta. |
| Caída | Caer al vacío quita `10` y devuelve a Abby al último suelo firme. |
| Hordas | 4 por piso; 5 enemigos, máximo 4 a la vez; salen de grietas. El HUD muestra `Enemigos: N`. |
| Guía | Una luz morada marca la siguiente horda; el texto indica cuántas faltan. |
| Salida | Solo se abre con las 4 hordas derrotadas; lleva al piso correcto de [[01 - Estructura del Contenido]]. |
| Enemigos | Cada tipo avisa en el suelo antes de pegar y se comporta según [[03 - Enemigos y NPC]]. El Guardián para los tajos 1 y 2 de frente. El Espectro se teletransporta a menos de `3,5 m`. |
| Progresión | El enemigo nuevo de cada piso aparece según [[05 - Progresión]]. |
| Dante | Aparece solo con las 4 hordas derrotadas (`AÚN NO` si se entra antes). Tres patrones. Al 50 %: `¡FURIA!`. Al llegar a 0 cae y empieza el final. |
| Derrota | `Abby cayó.`; `Enter` reinicia el piso con vida y stamina completas. Contra Dante, reaparece frente a su arena. |
| Piso superado | Muestra tiempo y enemigos derrotados; `Enter` o `Espacio` continúa. |
| Vida entre pisos | La vida con que se sale de un piso es la del siguiente. |
| Relato | Abby comenta al entrar, a la mitad y al abrirse la salida. |
| Notas | 18 en total; se leen con `E`; la pausa muestra cuántas se encontraron. |
| Pausa | `Esc` detiene el juego; `Salir al menú` pide pulsar dos veces. |
| Modos | Cuatro; cambian vida, velocidad y pausa de los enemigos; se conservan al cerrar. |
| Final | "Abby…", recuerdos, "Volví.", "Continuará…", créditos con los cinco integrantes, vuelta al menú y guardado borrado. |
| Audio | Hay música en cada escena; cambia al empezar y terminar una horda; los tres volúmenes funcionan. |
| Rendimiento | 60 FPS a 1080p en la laptop de presentación; carga menor a 1 s. |
| Estabilidad | Ningún error en consola en la ruta completa. |

## Aceptado con limitación

| Área | Limitación aceptada para la demo |
| --- | --- |
| Continuar | No guarda en los pisos 5 a 7 (B-01) |
| Mando | La fuente requiere el teclado (B-02) |
| Modos | "Daño recibido" y "Curación" no tienen efecto (B-03) |
| Audio | Sintetizado, a falta del final |
