# Personajes y animación

Sprites del proyecto en el commit `bf6203d`. Los GIF se armaron directo de los cuadros de `Assets/`, ampliados sin suavizado.

## Catálogo

| Personaje | Carpeta | Lienzo | Reposo | Caminar | Atacar | Otros |
| --- | --- | --- | --- | --- | --- | --- |
| Abby | `sprites/Abby`, `Resources/AbbyAnim` | 128 px (tajos 144 px) | 8 dir. | 8 dir. × 8 cuadros | 3 tajos × 5 dir. × 4–5 cuadros | Impulso 8 dir. × 9; poses Golpe, Guardia, Rodilla, Tendida |
| Dante humano | `Resources/DanteHumano` | 96 px | 8 dir. | 5 dir. × 6 | 5 dir. × 4–5 | Tendido (8 dir. y de lado) |
| La Sombra | `Resources/Personajes/Dante`, `EnemigosAnim/Dante` | 128 / 176 px | 8 dir. | 5 dir. × 6 | 5 dir. × 8 | — |
| Larva | `EnemigosSprites/Sombra`, `EnemigosAnim/Sombra` | 128 / 176 px | 8 dir. | 5 dir. × 8 | 5 dir. × 8 | — |
| Acechador | `…/Saltador` | 104 / 176 px | 8 dir. | 5 dir. × 6 | 5 dir. × 8 | — |
| Bruto | `…/Bruto` | 96 / 176 px | 8 dir. | 5 dir. × 6 | 7 dir. × 8 | — |
| Embestidor | `…/Embestidor` | 96 / 176 px | 8 dir. | 5 dir. × 8 | 5 dir. × 8 | — |
| Guardián | `…/Escudero` | 96 / 176 px | 8 dir. | 5 dir. × 6 | 5 dir. × 8 | — |
| Espectro | `…/Hechicero` | 104 / 176 px | 8 dir. | 5 dir. × 8 | 5 dir. × 8 | Proyectil × 4 |
| Coloso | `Resources/ColosoAnim` | 176–192 px | — | — | — | Rugido × 6, Zarpazo × 6, Golpe × 8 |
| Capitán, cazador, soldado, civil | `Resources/Personajes` | — | 8 dir. | — | — | — |

Las animaciones se dibujan en 5 direcciones (sur, sureste, este, noreste, norte); las del oeste se obtienen **espejando por escala**, porque el material `SpriteLit3D` ignora `flipX`.

## Abby

![](../Media/Sprites/Abby_8dir.png)

| Caminar (sur) | Caminar (este) | Caminar (norte) |
| --- | --- | --- |
| ![](../Media/GIFs/Abby_Walking_south.gif) | ![](../Media/GIFs/Abby_Walking_east.gif) | ![](../Media/GIFs/Abby_Walking_north.gif) |

| Tajo 1 | Tajo 2 | Tajo 3 |
| --- | --- | --- |
| ![](../Media/GIFs/Abby_Tajo1_south.gif) | ![](../Media/GIFs/Abby_Tajo2_south.gif) | ![](../Media/GIFs/Abby_Tajo3_south.gif) |
| ![](../Media/GIFs/Abby_Tajo1_east.gif) | ![](../Media/GIFs/Abby_Tajo2_east.gif) | ![](../Media/GIFs/Abby_Tajo3_east.gif) |

| Impulso (sur) | Impulso (este) |
| --- | --- |
| ![](../Media/GIFs/Abby_Dash_south.gif) | ![](../Media/GIFs/Abby_Dash_east.gif) |

**Poses** (un cuadro por dirección):

| Golpe | Guardia |
| --- | --- |
| ![](../Media/Sprites/Abby_Pose_Golpe.png) | ![](../Media/Sprites/Abby_Pose_Guardia.png) |

| De rodillas | Tendida |
| --- | --- |
| ![](../Media/Sprites/Abby_Pose_Rodilla.png) | ![](../Media/Sprites/Abby_Pose_Tendida.png) |

Reglas de animación (`AbbySpriteAnimator.cs`):

- El ritmo de los pasos sigue la velocidad real de Abby.
- Cada tajo del combo reinicia su animación (`AbbyAttack.Swings`).
- El **bloqueo es una pose** de guardia con tinte azulado, sin animación.
- El **golpe recibido** es un tinte rojo de `0,15 s` con sacudida; no tiene cuadros propios.
- Al norte y al sur corre con los cuadros de caminar, porque la carrera perdía la espada en la mitad de los cuadros.
- La espada va siempre en la mano derecha.

## Dante humano

![](../Media/Sprites/DanteHumano_8dir.png)

| Caminar | Atacar | Tendido |
| --- | --- | --- |
| ![](../Media/GIFs/DanteHumano_Caminar_south.gif) | ![](../Media/GIFs/DanteHumano_Atacar_east.gif) | ![](../Media/Sprites/DanteHumano_Tendido.png) |

Solo se usa en el tutorial y tendido en el final. No tiene impulso, bloqueo ni golpe recibido propios: reutiliza caminar, reposo y el tinte rojo.

## La Sombra

![](../Media/Sprites/Dante_Sombra_8dir.png)

| Caminar | Atacar (sur) | Atacar (este) |
| --- | --- | --- |
| ![](../Media/GIFs/Dante_Sombra_Caminar_south.gif) | ![](../Media/GIFs/Dante_Sombra_Atacar_south.gif) | ![](../Media/GIFs/Dante_Sombra_Atacar_east.gif) |

## Enemigos de horda

| Enemigo | Reposo en 8 direcciones | Caminar (este) | Atacar (este) |
| --- | --- | --- | --- |
| Larva | ![](../Media/Sprites/Larva_8dir.png) | ![](../Media/GIFs/Larva_Caminar_east.gif) | ![](../Media/GIFs/Larva_Atacar_east.gif) |
| Acechador | ![](../Media/Sprites/Acechador_8dir.png) | ![](../Media/GIFs/Acechador_Caminar_east.gif) | ![](../Media/GIFs/Acechador_Atacar_east.gif) |
| Bruto | ![](../Media/Sprites/Bruto_8dir.png) | ![](../Media/GIFs/Bruto_Caminar_east.gif) | ![](../Media/GIFs/Bruto_Atacar_east.gif) |
| Embestidor | ![](../Media/Sprites/Embestidor_8dir.png) | ![](../Media/GIFs/Embestidor_Caminar_east.gif) | ![](../Media/GIFs/Embestidor_Atacar_east.gif) |
| Guardián | ![](../Media/Sprites/Guardian_8dir.png) | ![](../Media/GIFs/Guardian_Caminar_east.gif) | ![](../Media/GIFs/Guardian_Atacar_east.gif) |
| Espectro | ![](../Media/Sprites/Espectro_8dir.png) | ![](../Media/GIFs/Espectro_Caminar_east.gif) | ![](../Media/GIFs/Espectro_Atacar_east.gif) |

Además del dibujo, los enemigos se mueven por código: respiran, rebotan al caminar, se agachan al avisar, se estiran al lanzarse y tiemblan al recibir.

## El Coloso

| Rugido | Zarpazo | Golpe |
| --- | --- | --- |
| ![](../Media/GIFs/Coloso_Rugido.gif) | ![](../Media/GIFs/Coloso_Zarpazo.gif) | ![](../Media/GIFs/Coloso_Golpe.gif) |

## Jefes dibujados que no aparecen en la demo

| Guardián de las Ruinas | Capitán sin Barco | Señor del Torrente | Gárgola del Faro Roto |
| --- | --- | --- | --- |
| ![](../Media/GIFs/Jefe_Guardian_Ruinas_Atacar_south.gif) | ![](../Media/GIFs/Jefe_Capitan_Atacar_south.gif) | ![](../Media/GIFs/Jefe_Torrente_Atacar_south.gif) | ![](../Media/GIFs/Jefe_Gargola_Atacar_south.gif) |

## Tabla de personajes del proyecto

![](../Media/Referencias/Personajes_y_sprites.png)

> **Pendiente:** bocetos a mano y archivos fuente de Pixelorama, si el equipo quiere incluirlos en `Media/ConceptArt/`.
