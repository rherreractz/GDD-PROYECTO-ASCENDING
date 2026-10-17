# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema | Propósito | Dependencias | Estado |
|---|---|---|---|
| Combate | Espada y bloqueo | Controles, vida, IA | Por diseñar |
| IA de enemigos | Comportamiento de hordas y jefe | Combate, niveles | Por diseñar |
| Niveles / pisos | Estructura de hordas y jefe | IA, combate | Por diseñar |
| Cámara | Seguir al jugador en 2.5D | Controles | Por diseñar |
| Cinemáticas y diálogo | Presentar la historia | Narrativa | Por diseñar |

## Plantilla de sistema

### Nombre

**Objetivo:**

**Entradas:**

**Procesamiento / reglas:**

**Salidas:**

**Estados posibles:**

**Dependencias:**

**Interacciones:**

**Datos que necesita:**

**Datos que genera:**

**Riesgos:**

**Criterios de aceptación:**

## Relaciones entre sistemas

Controles → Combate (ataque, combo, bloqueo) → Vida y stamina → HUD.
IA de enemigos → Combate → Vida de Abby.
Niveles → IA (oleadas) y fuentes de curación → Vida.
Estados del juego → Cinemática, Jugando, Derrota, Cliffhanger.

> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
