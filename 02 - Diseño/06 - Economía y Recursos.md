# Economía y recursos

**La ruta de la demo no tiene economía.** No hay moneda, tienda, inventario ni mejoras. Se decidió así el 20 de octubre para seguir el GDD 0.6.0: "solo notas".

## Recursos que sí administra el jugador

| Recurso | Máximo | Se gasta en | Se recupera con |
| --- | ---: | --- | --- |
| Vida | `100` | Golpes (`8` a `15`), caídas (`10`) | Fuente de curación (100 %, un uso por fuente); reintento |
| Stamina | `100` | Bloquear (`20` por golpe), impulso (`20`) | `25`/s tras `1 s` sin gastar |
| Fuentes | 1 o 2 por piso | Un uso cada una | No se recuperan en el mismo intento |

## Presupuesto de stamina

- 5 bloqueos seguidos, o 5 impulsos, o cualquier mezcla que sume `100`.
- De vacío a lleno: `1 s` de espera más `4 s` de regeneración.
- Atacar es gratis: la stamina es un recurso **defensivo**.

## Fuentes por escena

| Escena | Fuentes |
| --- | ---: |
| `Expedicion`, `Diorama`, `CuartosA`, `Puerto`, `Cascadas`, `Lago`, `Nevado`, `Cima` | 1 |
| `Acantilado`, `Cueva` | 2 |

## Sistemas presentes en el código y fuera de la ruta

`RunState.cs`, `ShardPickup.cs`, `MerchantShop.cs` y `TreasureChest.cs` implementan fragmentos de torre, mercader (daño `+25 %` y vida `+25` por nivel) y cofres. Pertenecen a la ruta de prueba anterior y están apagados en la ruta de la demo. Un consejo de la pantalla de carga todavía los menciona; ver [[03 - Bugs y Seguimiento]].
