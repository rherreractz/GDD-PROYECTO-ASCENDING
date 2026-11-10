# Entornos

## Cómo se construyen

Los mapas no se modelan a mano: los genera `DioramaBuilder` (30 archivos parciales, uno por piso o por tipo de pieza) y `ExteriorBuilder` para Cala Sombría. El resultado se guarda en la escena. Cambiar un mapa implica regenerarlo desde el menú `Abby/…` del editor y guardar.

| Pieza | Archivo | Detalle |
| --- | --- | --- |
| Terreno | `DioramaBuilder.Terrain.cs` | Malla con ruido; escenas 3 veces más ligeras al fusionar el terreno |
| Caminos | `DioramaBuilder.Caminos.cs` | Una sola malla por material: tierra, empedrado y grava, sin parpadeo en esquinas |
| Casas | `DioramaBuilder.Casas.cs` | Un estilo por piso, con techo real |
| Vegetación | `DioramaBuilder.Plants.cs` | Árboles y plantas; se quitan los que tapan la cámara |
| Estructuras | `DioramaBuilder.Estructuras.cs` | Fogatas y braseros con partículas, carpas, pozo, puestos, faro roto, santuario |
| Agua | `AbbyWater.shader`, `AbbyWaterfall.shader` | Olas, espuma y corriente por vértice en los ríos |
| Cielo | `AbbySky.shader`, `AbbySkyNoche.shader`, `AbbyAurora.shader` | Cielo propio por piso |
| Cristales | `AbbyCristalFacetado.shader` | Gruta de Cristal |

## Identidad de cada piso

| Piso | Materiales y arquitectura | Luz |
| --- | --- | --- |
| Cala Sombría | 73 casas, calles anchas, plaza y campamento | Noche (`ExteriorProfile_Noche`) |
| Piso 20 | Roca natural con columnas y peñascos; runas de neón en el suelo | Baja, con luz de sala |
| 1 · Pueblo | Entramado de madera, camino de tierra, río | Atardecer |
| 2 · Puerto | Encalado de pescador, tejas, muelle y escaleras de madera con barandal | Atardecer |
| 3 · Cascadas | Piedra con paja, bancales anchos, cascadas curvas con bruma | Atardecer, más claro |
| 4 · Acantilado | Pizarra, en cubos; playa, barco, puente, faro, arcos y farallones | Sol que no termina de ponerse |
| 5 · Gruta | Bloques de roca, lago turquesa, cristales en el techo | Cerrada, luz de cristal |
| 6 · Lago | Agua en calma, sierra continua al fondo | Atardecer |
| 7 · Aldea nevada | Nieve, posada, ventanas encendidas | Última noche del invierno |
| 8 · Cima | Islas de piedra sobre el vacío | Cielo abierto, sin franja en el horizonte |
| Final | Escalinata, puerta, casa en la nieve | Propia |

## Texturas

Generadas con `Tools/texgen/texgen.py` y `pixel_diorama.py`, a baja resolución para que combinen con el pixel art.

## Posproceso

Perfiles de volumen por tipo de escena: `DioramaProfile`, `ExteriorProfile`, `ExteriorProfile_Noche` y `ExpedicionProfile`. Incluyen bloom, ajuste de color y viñeta; el enfoque tipo maqueta lo hace `TiltShiftFocus.cs`.
