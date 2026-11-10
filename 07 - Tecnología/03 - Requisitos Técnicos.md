# Requisitos técnicos

## Metas

| Meta | Valor |
| --- | --- |
| Cuadros por segundo | 60, con sincronía vertical (`LimiteFPS.cs`) |
| Resolución | 1920×1080 |
| Tiempo de carga entre pisos | Menos de 1 s |
| Errores en consola | 0 en toda la ruta |

## Mediciones (4 de noviembre de 2026)

Ejecutable en la laptop de desarrollo (RTX 5050, 1920×1080), cada escena sin combate:

| Medida | Resultado |
| --- | --- |
| Cuadros por segundo sin límite | De 93 a 346 según la escena |
| Tiempo de carga | De 0,2 a 0,6 s |
| Memoria reservada | 1 089 MB |
| En el editor, con 6 enemigos | Unos 57 FPS en los 6 pisos medidos |

Fuente: `PENDIENTE_GDD.md` del repositorio.

## Tamaños

| Elemento | Tamaño |
| --- | --- |
| Ejecutable | Unos 330 MB |
| Escena más pesada | `Cascadas.unity`, 58 MB |
| Escena más ligera | `Menu.unity`, 5 KB (carga los paisajes de otras escenas) |

## Requisitos estimados

| | Mínimo estimado | Equipo de presentación |
| --- | --- | --- |
| Sistema | Windows 10 de 64 bits | Windows 11 |
| Gráficos | Tarjeta dedicada compatible con DirectX 11 | RTX 5050 |
| Memoria | 8 GB | — |
| Disco | 1 GB libre | — |

> **Pendiente:** medir el ejecutable **en combate** y en una PC más modesta; completar las características de la laptop de presentación. El mínimo es una estimación, no una medición.
