# Audio y música

**Todo el audio de `bf6203d` se sintetiza por código** al abrir el juego, a `22 050 Hz` (`Musica.cs`, `Sonido.cs`). El proyecto no contiene archivos de audio. La música se compone en otro hilo para no trabar el arranque de las hordas.

El sistema está preparado para reemplazo: si existe `Assets/Resources/Audio/Musica_<Pista>` o `Assets/Resources/Audio/<Efecto>`, se usa ese archivo en lugar del sintetizado.

## Música

| Pista | Tempo | Progresión | Dónde suena |
| --- | ---: | --- | --- |
| `Menu` | 64 bpm | La m · Fa · Do · Mi | Menú, intro y créditos |
| `Paisaje` | 78 bpm | Re · La · Si m · Sol | Exploración en los pisos con agua y al terminar cada horda |
| `Combate` | 92 bpm | Re m · Si♭ · Fa · La | Al empezar cada horda; de fondo en la Cima, el tutorial y la Biblioteca |
| `Jefe` | 124 bpm | La m · Sol · Fa · Mi | Dante |
| `Vacia` | 116 bpm | Caja de música en chiptune | Piso 7, la aldea vacía |
| `Final` ("Despedida") | 58 bpm | Piano solo; el violín entra cuando Abby lo encuentra | Escena final |

La pista cambia sola (`Musica.cs`): al cargar una escena, al empezar una horda y al terminarla.

El cambio entre pistas es un cruce suave: la que sale baja despacio mientras entra la siguiente.

## Efectos

| Efecto | Cuándo suena |
| --- | --- |
| `Espada` | Cada tajo; sube de tono con el número de golpe del combo |
| `Bloqueo` | Golpe bloqueado |
| `Dano` | Abby recibe daño |
| `Impulso` | Al impulsarse, con variación de tono |
| `Fuente` | Al usar una fuente |
| `Muerte` | Abby cae |
| `Alerta` | Aviso de ataque de un enemigo; momentos de alerta en el tutorial y la cinemática |
| `Paso` | Pasos de Abby (`Pasos.cs`) |
| `Clic` | Navegación de menús |
| `Destello` | Destellos de enemigos y de la cinemática |
| `Rugido`, `Temblor`, `Impacto` | Cinemática del Coloso |
| `Latido`, `Colgante`, `Ventana` | Escena final |

## Mezcla

| Canal | Valor inicial |
| --- | ---: |
| General | 80 % |
| Música | 70 % |
| Efectos | 90 % |

Se ajustan en pasos de 10 % desde Configuración y se guardan entre sesiones.

## Estado

El audio sintetizado es **provisional**. El plan de audio final es teclado, órgano y violín con 7 efectos grabados, a cargo de Francisco Uc.

> **Pendiente:** herramientas, proceso y créditos de la música final, y confirmar si entra antes del 20 de noviembre.
