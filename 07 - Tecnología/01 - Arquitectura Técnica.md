# Arquitectura Técnica

## Descripción de la sección

Explica cómo está construido técnicamente el videojuego y cómo se comunican sus componentes.

## Arquitectura

```text
Entrada
  ↓
Controlador
  ↓
Lógica de juego
  ↓
Sistemas
  ↓
Datos / Persistencia
  ↓
Presentación
```

## Componentes principales

| Componente | Responsabilidad | Dependencias |
|---|---|---|

| Componente | Responsabilidad | Dependencias |
|---|---|---|
| Controlador del jugador | Movimiento, ataque y bloqueo | Entrada |
| Vida y stamina | Estado del personaje | Combate |
| IA de enemigos | Comportamiento y hordas | Combate, niveles |
| Gestor de niveles | Hordas, fuentes de curación y jefe | IA |
| Cámara | Seguir al jugador | Controlador |
| UI | HUD y menús | Vida y stamina |
| Gestor de estados | Cinemática, juego, derrota | Todos |

## Comunicación

Por eventos y referencias directas entre componentes (por definir).

## Principios técnicos

- Bajo acoplamiento cuando sea razonable.
- Responsabilidades claras.
- Código mantenible.
- Datos separados de lógica cuando corresponda.
- Evitar dependencias innecesarias.

> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
