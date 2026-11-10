# Mecánicas

Todos los valores son del prefab `Abby.prefab` y de los scripts indicados, en el commit `bf6203d`.

## Movimiento y salto (`PlayerMotor.cs`)

| Parámetro | Valor |
| --- | ---: |
| Velocidad | `5 m/s` |
| Aceleración | `45 m/s²` (llega a velocidad máxima en `0,11 s`) |
| Altura de salto | `1,2 m` |
| Gravedad | `×1,5` de la de Unity, es decir `14,7 m/s²` |
| Coyote time | `0,1 s` después de dejar el borde |
| Memoria del salto | `0,15 s` (`PlayerInputReader.jumpBufferTime`) |

La dirección se interpreta respecto a la cámara. El sprite no gira el objeto: solo cambia el dibujo según la dirección.

## Combo de espada (`AbbyAttack.cs`)

| Tajo | Daño | Empuje | Congelación al impactar |
| --- | ---: | ---: | ---: |
| 1 | `10` | `5` | `0,035 s` |
| 2 | `10` | `5` | `0,035 s` |
| 3 | `15` | `11` | `0,07 s` |

| Parámetro | Valor |
| --- | ---: |
| Preparación / golpe activo / recuperación | `0,05 s` / `0,12 s` / `0,16 s` |
| Duración de un tajo | `0,33 s` |
| Combo completo | `35` de daño en `0,99 s` |
| Ventana para encadenar | `0,6 s`; pasado ese tiempo el combo vuelve al tajo 1 |
| Avance por tajo | `5 m/s` durante el golpe activo, unos `0,6 m` |
| Caja de golpe | `1,9 × 1,4 × 1,7 m`, centrada `0,95 m` al frente |
| Asistencia de apuntado | Gira hacia el enemigo más cercano a menos de `4,2 m` y dentro de `70°` |

Atacar **no gasta stamina**. Mientras bloquea, Abby no ataca. Un clic durante un tajo queda guardado y encadena el siguiente.

**Daño final de un tajo = `daño base × (1,6 si es tajo de impulso) × (2 si hay crítico)`**

## Bloqueo y stamina (`AbbyBlock.cs`)

| Parámetro | Valor |
| --- | ---: |
| Stamina máxima | `100` |
| Daño recibido al bloquear | `8 %` |
| Costo por golpe bloqueado | `20` |
| Empuje recibido al bloquear | `35 %` |
| Velocidad al cubrirse | `45 %` (`2,25 m/s`) |
| Espera antes de regenerar | `1 s` sin bloquear ni gastar |
| Regeneración | `25` por segundo (de 0 a 100 en `4 s`) |
| Invulnerabilidad tras bloquear | `0,25 s` |

Con stamina llena se bloquean **5 golpes seguidos**. Con menos de `20` no se puede bloquear y la barra parpadea. El bloqueo cubre en cualquier dirección.

## Impulso (`AbbyDash.cs`)

| Parámetro | Valor |
| --- | ---: |
| Velocidad | `17 m/s` |
| Duración | `0,18 s` (unos `3,1 m`) |
| Invulnerabilidad | `0,26 s` desde que empieza |
| Recarga | `0,5 s` |
| Costo | `20` de stamina |

Funciona en el aire y deja estelas del sprite cada `0,035 s`.

- **Esquiva perfecta:** si un golpe iba a alcanzarla durante la invulnerabilidad, aparece `¡ESQUIVA PERFECTA!`, el tiempo baja al `25 %` durante `0,35 s` y el siguiente tajo dentro de `1,6 s` es **crítico** (`×2`).
- **Tajo de impulso:** atacar durante el impulso o hasta `0,2 s` después hace `×1,6` de daño y `12` de empuje. Rompe la guardia del Guardián.

## Vida y daño recibido (`PlayerHealth.cs`)

| Parámetro | Valor |
| --- | ---: |
| Vida máxima | `100` |
| Invulnerabilidad tras un golpe | `0,7 s` (el sprite parpadea) |
| Daño por golpe enemigo | Se ajusta siempre al rango **`8` a `15`** |
| Caída al vacío | `10` de daño y reaparece en el último suelo firme (`FallGuard.cs`) |

Orden de resolución de un golpe entrante:

1. Si Abby está en invulnerabilidad de impulso: no hay daño (y puede contar como esquiva perfecta).
2. Si está en invulnerabilidad tras un golpe: no hay daño.
3. El daño se ajusta al rango `8–15`.
4. Si está bloqueando con stamina: el daño se multiplica por `0,08` y gasta `20` de stamina.
5. Se resta la vida, se aplica el empuje y se muestra el número flotante.

Por el paso 3, el golpe más fuerte del juego quita `15` y, bloqueado, `1,2`. Abby aguanta como mínimo **7 golpes** sin bloquear.

## Fuente de curación (`HealingShrine.cs`)

Se activa con `E` a menos de `2,4 m`. Restaura el `100 %` de la vida y se apaga: un solo uso. Con la vida llena no se gasta y muestra `Vida al máximo`.
