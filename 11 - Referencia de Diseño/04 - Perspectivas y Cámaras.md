# Perspectivas y cámaras

## Perspectiva: 2.5D

Personajes en sprites 2D que siempre dan la cara a la cámara (`SpriteBillboard`), sobre un mundo 3D. El movimiento es libre en el plano del suelo, con altura (salto, escaleras, desniveles).

## Cámara del juego

| Parámetro | Valor |
| --- | --- |
| Tipo | Tercera persona, fija e inclinada, tipo maqueta |
| Seguimiento | Sigue a Abby; ella va algo arriba del centro de la pantalla |
| Campo de visión | `38°` (teleobjetivo suave, aplana la perspectiva) |
| Distancia | `10 m` |
| Giro por el jugador | No (`CamaraFija = true`); `Q` y `E` ya no giran |
| Giro automático | Unos grados por zona del mapa (`ZonasCamara`), también en combate |
| Inclinación | `F5` normal, `F6` con 5° más |

## Otras cámaras

| Cámara | Cuándo |
| --- | --- |
| Toma aérea de entrada | Al cargar cada piso; baja hasta Abby |
| Vista de reposo | A los `6 s` sin moverse |
| Cámara libre | `F3`; orbita con el mouse, choca con obstáculos y nunca se acerca a menos de `2,5 m`; `F4` regresa |
| Planos de cinemática | Tutorial (contrapicado al Coloso) y final (11 planos) |
| Menú | Paneo lento alrededor de cuatro paisajes |

## Por qué fija

Con sprites en 8 direcciones, una cámara que gira obliga a recalcular qué dibujo mostrar y desorienta en combate. Fija, el jugador aprende la pantalla y los avisos del suelo se leen siempre igual.
