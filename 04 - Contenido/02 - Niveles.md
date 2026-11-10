# Niveles

Todos los pisos de la torre comparten reglas: 4 hordas sobre el camino, guía de luz morada, al menos una fuente y una salida que se abre al final. Cambia el paisaje, la mezcla de enemigos y la vida de estos. Los mapas se generan con `DioramaBuilder` (uno por piso) y se guardan en la escena.

## Tutorial · Piso 20 (`Expedicion`)

| Dato | Valor |
| --- | --- |
| Personaje | Dante humano |
| Escenario | Gruta de roca natural, runas en el suelo plano, abismo al fondo (`DioramaBuilder.ExpedicionCueva.cs`) |
| Encuentros | `Entrenamiento`: 3 Larvas · `La oleada`: 6 enemigos (Larva, Bruto, Larva, Acechador…) |
| Vida de enemigos | `×0,8` |
| Regla especial | La vida de Dante no baja de `1` |

Pasos guiados, en orden y con su texto en pantalla:

1. `WASD / stick izquierdo: moverte`
2. `Espacio: saltar. Sube al escalón`
3. `Sigue a la expedición`
4. `Clic izquierdo: atacar · tres clics seguidos: combo (el tercer golpe pega más)`
5. `Las fuentes de curación restauran toda tu vida. Acércate y presiona E (cada fuente sirve una vez)`
6. `Clic derecho sostenido: bloquear. Recibes solo el 8 % del daño, pero gasta stamina. Las sombras rojas del suelo avisan cada ataque`
7. `Bien hecho. Sigamos hasta el borde.` → `Acércate al borde del abismo` → cinemática del Coloso.

## Cala Sombría (`Exterior`)

Pueblo costero de noche: 73 casas, Calle Mayor, plaza del mercado, campamento y la torre al fondo, a `217 m` del punto de inicio. Lo único con color es el fuego y el aura morada de la torre. Sin enemigos. A `5 m/s` son unos 45 segundos de caminata hasta el portal.

## Pisos de la torre

| Piso | Escena | Paisaje y recorrido | Arquitectura | Hordas (enemigos) | Fuentes | Notas |
| --- | --- | --- | --- | --- | ---: | ---: |
| 1 | `Diorama` | Pueblo con río; camino de tierra hasta la plaza | Casas de entramado | 4 (5·5·5·5) | 1 | 2 |
| — | `CuartosA` | Biblioteca cerrada; arena de `24 × 18 m` | Libreros y salas | 1 (5) | 1 | 1 |
| 2 | `Puerto` | Plaza, cabo del faro y punta del muelle; bancales bajos | Casas de pescador encaladas, escaleras de madera | 4 (5·5·4·5) | 1 | 2 |
| 3 | `Cascadas` | Río que baja cuatro bancales; se sube contra la corriente | Piedra con techo de paja, puentes | 4 (5·5·5·5) | 1 | 2 |
| 4 | `Acantilado` | Prado, escalinata a la playa con barco naufragado, isla, puente largo y faro | Pizarra; hecho en cubos | 4 (5·5·5·5) | 2 | 2 |
| 5 | `Cueva` | Caverna inundada: lago turquesa, cuatro islas y puentes | Pueblo minero, bosque de cristal, techo con cristales | 4 (5·5·5·5) | 2 | 2 |
| 6 | `Lago` | Orilla de un lago en calma con pueblo de pescadores | Casas bajas junto al agua | 4 (5·5·5·5) | 1 | 2 |
| 7 | `Nevado` | Calle de una aldea nevada con las luces prendidas | Posada y casas con nieve | 4 (5·5·5·5) | 1 | 3 |
| 8 | `Cima` | Islas sobre el abismo, de la isla de inicio a la arena final | Ruinas de piedra | 4 (5·6·5·6) + Dante | 1 | 2 |

Arena estándar: `12 × 9 m`. Arena de Dante: `20 × 18 m`.

## Final (`Final`)

Un pedazo de torre sobre el abismo, sin enemigos (`DioramaBuilder.Final.cs`, `EscenaFinal.cs`): escalinata con un descanso plano donde yace Dante, una puerta que se abre y, detrás, el pueblo y una casa en la nieve con los créditos.

## Límites y seguridad del mapa

- El borde jugable se ve distinto en cada piso (agua, risco, muro, vacío); la colisión es la misma.
- Caer bajo `Y = -3` reaparece a Abby en el último suelo firme.
- Si queda atrapada bajo el terreno más de `0,35 s`, vuelve al camino sin daño: `¡De vuelta al camino!`.

> **Pendiente:** una captura por piso en `Media/Capturas/`.
