# Criterios de calidad

## Definición de "terminado"

Una función está terminada cuando cumple las cinco:

1. Hace lo que dice este GDD, con los valores de [[02 - Mecánicas]] y [[03 - Enemigos y NPC]].
2. No deja errores en la consola en ninguna escena de la ruta.
3. Funciona en el **ejecutable**, no solo en el editor.
4. La probó alguien que no la programó.
5. Está en la rama y documentada si cambió algo del GDD.

## Criterios de la demo

| Criterio | Meta | Estado en `bf6203d` |
| --- | --- | --- |
| Estabilidad | 0 errores en consola en la ruta | Cumple en pruebas automáticas por escena |
| Fluidez | 60 FPS a 1080p | Cumple sin combate en el ejecutable; combate sin medir |
| Carga | Menos de 1 s entre pisos | Cumple (0,2 a 0,6 s) |
| Completable | Se llega de principio a fin sin atorarse | Probado por partes; falta de corrido |
| Legibilidad del combate | Todo ataque avisa antes de pegar | Cumple |
| Legibilidad del texto | Ningún texto se sale de su cuadro | Cumple (`CuadroNarracion.Cabe`) |
| Coherencia visual | Mismo tamaño de personaje en todas las poses | Cumple (`PixelLabImporter`) |
| Recuperación | Una falla no obliga a empezar de cero | Cumple con la limitación de los pisos 5 a 7 |
| Duración | 15 minutos | Sin medir con 8 pisos |

## Prioridad de bugs

| Nivel | Definición | Ejemplo |
| --- | --- | --- |
| Bloqueante | Impide terminar la demo | Una salida que no se abre |
| Alto | Se nota en la presentación | Caída de cuadros en combate |
| Medio | Molesta sin impedir | La fuente no responde al mando |
| Bajo | Detalle | Un texto que dice "bajar" |

Solo los bloqueantes y altos justifican reabrir el código congelado.
