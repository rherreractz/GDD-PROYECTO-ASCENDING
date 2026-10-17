# Reglas y Estados del Juego

## Descripción de la sección

Define las reglas globales y los estados que puede atravesar el videojuego.

## Estados principales

- Menú principal
- Carga
- Jugando
- Pausa
- Victoria
- Derrota
- Game Over
- Créditos

## Transiciones

| Estado origen | Evento | Estado destino | Condición |
|---|---|---|---|
| Menú principal | Iniciar | Cinemática / Tutorial | Pulsar jugar |
| Jugando | Vida en 0 | Derrota | Abby derrotada |
| Derrota | Reintentar | Jugando | Reinicia el piso actual |
| Cinemática | Termina | Tutorial / Jugando | Cinemática inicial completa |
| Jugando | Jefe final | Cliffhanger / Fin de la demo | Fin de la historia de la demo |

## Reglas globales

1. Los enemigos no son humanos.
2. El bloqueo reduce el daño al 8 %, no da inmunidad.
3. Bloquear gasta stamina; sin stamina no se puede bloquear.
4. La vida solo se restaura en las fuentes de curación.

## Casos especiales

Si Abby muere durante el jefe, se reinicia el combate con el jefe.
La cinemática inicial se puede saltar con una tecla.

> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
