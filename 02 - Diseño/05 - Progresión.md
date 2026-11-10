# Progresión

No hay niveles de personaje ni mejoras en la ruta: Abby termina con las mismas herramientas con que empieza. La progresión es del **jugador** y del **piso**.

## Curva por piso

| Piso | Escena | Vida de enemigos | Enemigo nuevo | Lista de la horda (en orden cíclico) |
| --- | --- | ---: | --- | --- |
| Tutorial | `Expedicion` | `×0,8` | — | Larva (entrenamiento); Larva, Bruto, Larva, Acechador (la oleada) |
| 1 | `Diorama` | `×1` | Larva del Abismo | Larva |
| — | `CuartosA` | `×1,05` | — | Larva |
| 2 | `Puerto` | `×1,15` | Acechador, Bruto | Larva, Acechador, Larva, Bruto |
| 3 | `Cascadas` | `×1,3` | Embestidor | Larva, Embestidor, Acechador, Bruto |
| 4 | `Acantilado` | `×1,45` | Guardián | Guardián, Larva, Embestidor, Bruto, Acechador |
| 5 | `Cueva` | `×1,6` | — | Acechador, Guardián, Embestidor, Bruto |
| 6 | `Lago` | `×1,75` | Espectro | Espectro, Larva, Guardián, Embestidor |
| 7 | `Nevado` | `×2,05` | — | Espectro, Guardián, Bruto, Acechador |
| 8 | `Cima` | `×1,6` | Dante | Espectro, Guardián, Embestidor, Bruto, Acechador |

Fuentes: multiplicador en `DioramaBuilder.Level.cs` (`LevelInfo.hp`) y guardado en cada escena (`RoomEncounter.healthMultiplier`); listas en `DioramaBuilder.Roster`.

## Qué aprende el jugador en cada tramo

| Tramo | Lección | Cómo la enseña el juego |
| --- | --- | --- |
| Tutorial | Mover, saltar, combo, curarse, bloquear | Pasos guiados con Dante; ahí la vida no baja de `1` |
| Piso 1 | Leer la franja roja | Solo Larvas: `40` de vida, caen con un combo y un tajo |
| Piso 2 | Bloquear golpes fuertes | El Bruto pega `15` y solo lo frena el tercer tajo |
| Piso 3 | Moverse de la línea | El Embestidor carga `9,5 m` en línea recta |
| Piso 4 | Rodear o romper la guardia | El Guardián para de frente lo que no sea tercer tajo o tajo de impulso |
| Pisos 5 a 7 | Priorizar objetivos | El Espectro dispara de lejos y se teletransporta si te acercas |
| Piso 8 | Todo junto | Cinco tipos mezclados y Dante |

## Golpes necesarios por enemigo (modo Normal)

Con el combo `10 / 10 / 15` (35 por combo):

| Enemigo | Piso donde debuta | Vida ahí | Combos completos |
| --- | --- | ---: | ---: |
| Larva | 1 | `40` | 2 (cae en el 4.º tajo) |
| Acechador | 2 | `63` | 2 |
| Bruto | 2 | `138` | 4 |
| Embestidor | 3 | `91` | 3 |
| Guardián | 4 | `138` | 4 |
| Espectro | 6 | `79` | 3 |
| Dante | 8 | `768` | 22 |

La vida por piso de cada tipo está en [[03 - Enemigos y NPC]].
