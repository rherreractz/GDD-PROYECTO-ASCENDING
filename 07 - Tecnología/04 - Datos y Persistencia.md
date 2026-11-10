# Datos y persistencia

## Dónde viven los datos del juego

El proyecto no usa ScriptableObjects ni archivos de datos externos. Los valores están en tres lugares:

| Lugar | Qué contiene | Ejemplo |
| --- | --- | --- |
| Constantes y campos en código | Reglas de combate y enemigos | `AbbyBlock.DanoRecibido = 0.08f`; el `switch` de `TowerEnemy.Configure` |
| Prefab | Valores de Abby y su cámara | `Abby.prefab`: `speed: 5`, `jumpHeight: 1.2` |
| Escena | Hordas, salidas, fuentes y notas colocadas | `RoomEncounter.healthMultiplier`, `FloorExit.nextScene` |

## Tablas de datos en código

| Tabla | Archivo | Contenido |
| --- | --- | --- |
| `Difficulty.Presets` | `Difficulty.cs` | 4 modos |
| `DioramaBuilder.Info` | `DioramaBuilder.Level.cs` | Título, subtítulo, siguiente escena y multiplicador de vida por piso |
| `DioramaBuilder.Roster` | `DioramaBuilder.Level.cs` | Lista de enemigos por piso |
| `Historia.Relato` | `Historia.cs` | Comentarios de Abby por escena |
| `Historia.Notas` | `Historia.cs` | Texto final de 7 notas, por identificador |
| `ZonasCamara.Aperturas` | `ZonasCamara.cs` | Toma de entrada por piso |
| `IntroImagenes.Guion` | `IntroImagenes.cs` | Imagen, duración y texto de cada paso de la intro |

Una sola fuente para los nombres propios: `Historia.Ciudad`, `Historia.Hermano`, `Historia.CapitanNombre`, `Historia.Padre`. Cambiar una constante cambia el nombre en todo el juego.

## Recursos cargados en tiempo de ejecución (`Resources`)

| Ruta | Contenido |
| --- | --- |
| `AbbyAnim/Tajo1..3/<dirección>` | Cuadros del combo |
| `EnemigosSprites/<Tipo>/<dirección>` | Reposo de enemigos |
| `EnemigosAnim/<Tipo>/<Caminar\|Atacar>/<dirección>` | Animaciones de enemigos |
| `DanteHumano/…`, `ColosoAnim/…`, `Personajes/…` | Personajes de la historia |
| `Intro/NN_nombre` | Imágenes de la intro, ordenadas por su número |
| `Fuentes/` | Inter y Press Start 2P |
| `Audio/Musica_<Pista>`, `Audio/<Efecto>` | Opcional: reemplaza al audio sintetizado |

Convención de direcciones: `south`, `south-east`, `east`, `north-east`, `north`, `north-west`, `west`, `south-west`.

## Persistencia

Solo `PlayerPrefs`: progreso, modo de juego, volúmenes y vista de cámara. Claves y reglas en [[04 - Guardado y Configuración]].

## Estado en memoria

| Dato | Clase | Vida |
| --- | --- | --- |
| Vida entre pisos | `RunState.SavedHealth` | Hasta morir o cerrar el juego |
| Notas encontradas | `SecretTracker` | La sesión |
| Enemigos vivos | `TowerEnemy.All` | El piso |
