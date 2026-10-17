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
| Jugando | Jefe final | Cliffhanger / Fin de la demo | Fin de la historia de la demo |

## Reglas globales

1.
2.
3.

## Casos especiales

Documenta excepciones importantes para evitar interpretaciones diferentes durante la implementación.


> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
