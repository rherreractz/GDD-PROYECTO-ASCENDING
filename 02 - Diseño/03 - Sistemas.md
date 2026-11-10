# Sistemas

## Hordas (`RoomEncounter.cs`, `DioramaBuilder.Hordas.cs`)

| Regla | Valor |
| --- | --- |
| Hordas por piso | `4` (la Biblioteca tiene `1`) |
| Enemigos por horda | `5` puntos de aparición (4 o 6 en algunas arenas de Puerto y Cima) |
| Enemigos vivos a la vez | Hasta `4`; el resto entra cada `0,45 s` conforme caen |
| Inicio | Al pisar la arena o acercarse a menos de `7 m` de su marca |
| Tipo de enemigo | Se toma de la lista del piso en orden cíclico: aparición `i` usa `lista[i mod n]` |
| Vida | Vida base del tipo × multiplicador del piso × modo de juego |
| Correa | Los enemigos persiguen hasta `20 m` fuera de la arena |
| Abandono | Si Abby se aleja, aparece `TE ALEJASTE` y los enemigos vuelven a su guarida |
| Salida | Se abre al derrotar las 4. Dante solo aparece con las 4 derrotadas; antes muestra `AÚN NO` |

Las hordas se colocan sobre el camino, repartidas de la entrada a la salida y a `16 m` o más una de otra, para que siempre se puedan terminar.

## Guía de hordas (`GuiaHordas.cs`)

Un haz de luz morada con aros y runas marca la siguiente horda. El HUD dice `Faltan N hordas: sigue la luz morada` y, al terminar, `¡PISO DESPEJADO!`.

## Aparición de enemigos

Cada enemigo sale de una **grieta del abismo**: pozo negro con borde morado, humo y luz. No puede recibir ni hacer daño hasta que termina de subir.

## Aguante y empuje de los enemigos (`TowerEnemy.cs`)

- **Aguante (`poise`):** daño acumulado necesario para interrumpir al enemigo. Con `0`, cualquier tajo lo frena.
- **Empuje recibido (`knockTaken`):** de `1` (retrocede completo) a `0,08` (casi no se mueve).

## Modos de juego (`Difficulty.cs`)

Se eligen en Pausa → Opciones y se guardan entre sesiones.

| Modo | Vida de enemigos | Velocidad de enemigos | Pausa entre ataques |
| --- | ---: | ---: | ---: |
| FÁCIL | `×0,7` | `×0,9` | `×1,3` |
| NORMAL | `×1` | `×1` | `×1` |
| DIFÍCIL | `×1,35` | `×1,12` | `×0,8` |
| PESADILLA | `×1,8` | `×1,25` | `×0,6` |

> **Inconsistencia conocida:** la tarjeta de cada modo también anuncia `Daño recibido` y `Curación`, pero esos dos multiplicadores no se aplican en el código de `bf6203d`. Ver [[05 - Seguridad y Riesgos Técnicos]].

## Vida entre escenas (`RunState.cs`)

La vida con la que Abby sale de un piso es la que tiene al entrar al siguiente. Al morir se borra y el reintento empieza con vida completa.

## Cámara (`MouseOrbitCamera.cs`, `ZonasCamara.cs`)

| Parámetro | Valor |
| --- | --- |
| Tipo | Fija, inclinada, sigue a Abby |
| Campo de visión | `38°` |
| Distancia | `10 m` |
| Entrada al piso | Toma aérea que baja hasta Abby |
| Reposo | Tras `6 s` quieta, la cámara se abre y recorre el paisaje (no en Expedición, Gruta ni Final) |
| Zonas | Gira unos grados en ciertas zonas de cada mapa |
| Oclusión | Casas y árboles que tapan a Abby dejan de dibujarse (`OccluderFade.cs`) |

## Efectos de impacto

Congelación breve al conectar (`HitStop.cs`), sacudida de cámara (`CameraShake.cs`), números flotantes de daño y chispas (`CombatFx.cs`).
