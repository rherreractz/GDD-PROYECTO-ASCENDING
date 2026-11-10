# Estructura del contenido

## Escenas del build (orden de `EditorBuildSettings.asset`)

| # | Escena | Rótulo de carga | Contenido | Sigue a |
| ---: | --- | --- | --- | --- |
| 0 | `Menu` | MENÚ PRINCIPAL | Menú sobre paisajes del juego | `Expedicion` |
| 1 | `Expedicion` | PISO 20 · La expedición | Tutorial con Dante, 2 encuentros, 1 fuente, cinemática del Coloso | `Intro` |
| 2 | `Intro` | PRÓLOGO · Cala Sombría, 2030 | 14 imágenes | `Exterior` |
| 3 | `Exterior` | CALA SOMBRÍA · Al pie de la torre | Caminata sin combate | `Diorama` |
| 4 | `Diorama` | PISO 1 · El Pueblo del Risco | 4 hordas, 1 fuente, 2 notas | `CuartosA` |
| 5 | `CuartosA` | CUARTOS · Pereza · La Biblioteca Dormida | 1 horda, 1 fuente, 1 nota | `Puerto` |
| 6 | `Puerto` | PISO 2 · El Puerto de las Mareas | 4 hordas, 1 fuente, 2 notas | `Cascadas` |
| 7 | `Cascadas` | PISO 3 · El Valle de las Cascadas | 4 hordas, 1 fuente, 2 notas | `Acantilado` |
| 8 | `Acantilado` | PISO 4 · El Sendero del Acantilado | 4 hordas, 2 fuentes, 2 notas | `Cueva` |
| 9 | `Cueva` | PISO 5 · La Gruta de Cristal | 4 hordas, 2 fuentes, 2 notas | `Lago` |
| 10 | `Lago` | PISO 6 · El Lago de los Espejos | 4 hordas, 1 fuente, 2 notas | `Nevado` |
| 11 | `Nevado` | PISO 7 · La Aldea de la Nieve Eterna | 4 hordas, 1 fuente, 3 notas | `Cima` |
| 12 | `Cima` | PISO 8 · El borde del abismo | 4 hordas, Dante, 1 fuente, 2 notas | `Final` |
| 13 | `Final` | — | Escena final y créditos | `Menu` |

Los conteos se leyeron de cada archivo `.unity` (componentes `RoomEncounter`, `HealingShrine`, `LoreNote` y `FloorExit.nextScene`).

## Totales

| Elemento | Cantidad |
| --- | ---: |
| Pisos jugables de la torre | 8, más la Biblioteca |
| Hordas en la ruta | 33 |
| Enemigos de horda en la ruta | 166 |
| Tipos de enemigo en la ruta | 6 |
| Jefes | 1 |
| Fuentes de curación | 12 |
| Notas legibles | 18 |
| Imágenes de la intro | 14 |

## Contenido en el proyecto que no entra a la demo

| Contenido | Estado |
| --- | --- |
| Jefes Guardián de las Ruinas, Capitán sin Barco, Señor del Torrente y Gárgola del Faro Roto | Con sprites y animaciones; no aparecen. El único jefe es Dante |
| Enemigos Arquero y Torbellino | Con lógica, sin sprite; fuera de las listas |
| Escenas `Templo`, `Montana`, `Nivel1` a `Nivel9`, `SampleScene` | Ruta de prueba anterior; apagadas en el build |
| Cuartos de Gula, Avaricia y Envidia | Con rótulo de carga; sin escena en el build |
| Mercader, cofres y fragmentos | Código presente, apagado en la ruta |
