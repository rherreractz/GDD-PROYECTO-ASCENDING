# Registro visual

Efectos del juego, definidos en `CombatFx.cs` salvo que se indique.

| Efecto | Descripción | Color | Se dispara en |
| --- | --- | --- | --- |
| Tajo | Arco de luz frente a Abby; más grande en el tercer golpe | Celeste; dorado en el 3.º; cian en tajo de impulso; rosa en crítico | `AbbyAttack` |
| Estela de impulso | Copias del sprite que se desvanecen en `0,22 s` | Cian translúcido | `AbbyDash` |
| Anillo de guardia | Aro al cubrirse y al bloquear | Azul claro | `AbbyBlock` |
| Chispas de bloqueo | 18 partículas | Azul claro | `AbbyBlock.TryBlock` |
| Chispas de daño | 14 partículas y tinte rojo del sprite | Rojo | `PlayerHealth` |
| Curación | 30 partículas que suben | Verde | `PlayerHealth.Heal` |
| Esquiva perfecta | 25 partículas y cámara lenta | Rosa | `AbbyAttack.OnPerfectDodge` |
| Caída de Abby | 50 partículas y sacudida fuerte | Lila | `PlayerHealth.Die` |
| Grieta del abismo | Pozo negro, borde morado, humo y luz | Morado | Aparición de enemigos |
| Franja de aviso | Rectángulo en el suelo hacia donde embiste | Rojo | `TowerEnemy` |
| Anillo de aviso | Círculo donde cae un golpe de área | Rojo, naranja o morado | Acechador, Espectro, Dante |
| Furia | 80 partículas y sacudida | Color de ojos del jefe | Fase 2 de Dante |
| Baliza de horda | Haz de luz, resplandor en el suelo, aros y runas que giran | Morado | `GuiaHordas` |
| Fuente | Cristal que flota y gira; luz que late | Verde | `HealingShrine` |
| Llamas | Partículas en fogatas y braseros | Naranja | Entornos |
| Parpadeo de antorchas | Variación de intensidad | Cálido | `LightFlicker` |

## Cámara

| Efecto | Uso |
| --- | --- |
| Sacudida (`CameraShake`) | `0,05` al impulsarse, `0,08` al bloquear, `0,22` al recibir daño, `0,35` en furia, `0,4` al caer |
| Congelación (`HitStop`) | `0,035 s` por tajo, `0,07 s` en el tercero, tajo de impulso y crítico |
| Toma de entrada | Aérea, baja hasta Abby; valores por piso en `ZonasCamara.Aperturas` |
| Planos (`CameraShot`) | 11 planos en la escena final; contrapicado con lente abierto en la cinemática del Coloso |

## Capturas

> **Pendiente:** el equipo graba una partida y deja en `Media/Capturas/` una imagen por fila de esta tabla y por piso. Lista mínima: HUD en combate, bloqueo, esquiva perfecta, grieta, baliza, fuente, pantalla de carga, pausa, opciones, caída, piso superado, Dante en fase 2 y créditos.
