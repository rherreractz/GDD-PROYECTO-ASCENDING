# Interfaz visual

Toda la interfaz se dibuja por código con `OnGUI` (`FloorDirector.cs`, `PauseMenu.cs`, `MenuPrincipal.cs`, `Cargador.cs`, `CuadroNarracion.cs`). Las medidas usan una unidad `u` proporcional a la pantalla, así que escala con la resolución.

## HUD en juego

```
┌───────────────────────────────────────────────────────────────┐
│ [retrato] ABBY                                   Enemigos: 3  │
│           ██████████ VIDA 100 / 100                           │
│           ███████ STAMINA                                     │
│                                                               │
│                 ¡PISO DESPEJADO!                              │
│            Sigue la luz hasta la salida                       │
│                                                               │
│             E · Usar la fuente de curación                    │
│                    LA SOMBRA · FURIA                          │
│              ███████████████░░░░░░░░                          │
│ WASD Mover  Clic izq. Atacar  Clic der. Bloquear  Espacio ... │
└───────────────────────────────────────────────────────────────┘
```

| Elemento | Posición | Comportamiento |
| --- | --- | --- |
| Retrato de Abby | Arriba a la izquierda | Recorte del sprite centrado en la cabeza; destella en azul al bloquear |
| Nombre | Junto al retrato | `ABBY`; en el tutorial, `DANTE` |
| Barra de vida | Bajo el nombre | Texto `VIDA 100 / 100`; va de verde a rojo; una franja dorada muestra la vida recién perdida; **parpadea por debajo del 30 %** |
| Barra de stamina | Bajo la vida, al 80 % de su ancho | Azul; **naranja** con menos de `40`; **roja** con menos de `20`; el marco parpadea si se intenta bloquear sin stamina |
| Enemigos restantes | Arriba a la derecha | `Enemigos: N`, solo durante una horda |
| Barra del jefe | Abajo al centro, 55 % del ancho | Nombre en mayúsculas; al enfurecerse añade `· FURIA` y cambia a rojo vivo |
| Cartel central | Tercio superior | Título grande y subtítulo en cursiva sobre banda oscura; entra deslizándose |
| Aviso de fuente | Sobre la barra de controles | `E · Usar la fuente de curación`, parpadeante |
| Barra de controles | Borde inferior | Siempre visible |
| Números flotantes | Sobre los personajes | Daño en rojo, bloqueo en azul, curación en verde |

## Textos flotantes de combate

`BLOQUEO` · `¡ESQUIVA PERFECTA!` · `¡CRÍTICO!` · `¡Tajo de impulso!` · `¡FURIA!` · `Vida al máximo` · `¡Caíste al vacío!` · `¡De vuelta al camino!`

## Pantallas

| Pantalla | Contenido |
| --- | --- |
| Carga | Título del piso, subtítulo, barra, `Cargando...` y un consejo |
| Caída | `Abby cayó.` · `Enter · Reintentar el piso` · `Esc · Menú principal` |
| Piso superado | `¡PISO N SUPERADO!` · tiempo · enemigos derrotados · `Enter / Espacio para continuar` |
| Narración | Cuadro que crece con el texto; achica la letra si no cabe (`CuadroNarracion.Cabe`) |

Menús completos en [[02 - UI y Menús]].

## Señales en el mundo

| Señal | Significado |
| --- | --- |
| Franja o anillo rojo en el suelo | Zona donde va a caer un ataque |
| Anillo naranja | Punto de caída del Acechador |
| Anillo morado | Golpe de área de Dante |
| Haz de luz morada con runas | Siguiente horda |
| Grieta negra con borde morado | Va a salir un enemigo |
| Cristal verde que flota | Fuente disponible; apagada si ya se usó |
| Destello sobre un objeto | Nota legible |

> **Pendiente:** capturas reales del HUD, la pausa, la carga y la pantalla de caída.
