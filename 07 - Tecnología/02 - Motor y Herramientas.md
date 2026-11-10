# Motor y herramientas

## Motor

| Componente | Versión |
| --- | --- |
| Unity | `6000.6.4f1` |
| Universal Render Pipeline | `17.6.0` |
| Input System | `1.20.0` |
| AI Navigation | `2.0.14` |
| Timeline | `6.6.0` |
| uGUI | `2.6.0` |
| Test Framework | `1.8.0` |
| Visual Scripting | `1.9.12` (sin uso en el juego) |

Fuente: `ProjectVersion.txt` y `Packages/manifest.json`.

## Herramientas

| Herramienta | Uso |
| --- | --- |
| C# con Visual Studio / Rider | Programación |
| Git y GitHub | Control de versiones; repositorio `Gabriel-Garcia69/AbbysTower` |
| PixelLab | Generación de sprites en 8 direcciones y animaciones (Skeleton v3) |
| Pixelorama | Retoque de sprites |
| Python (`Tools/texgen`) | Generación de texturas de los escenarios |
| Obsidian | Este GDD |
| Figma | Diseño de la app complementaria |
| Asistente de IA para programación | Apoyo en código, pruebas automáticas y documentación |

## Herramientas propias del editor

| Menú o script | Función |
| --- | --- |
| `PixelLabImporter` | Importa sprites de PixelLab y calcula el tamaño para que el personaje mida igual en todas las poses |
| `PixelLabClips` | Arma los clips de animación |
| `Abby/Exterior/Hora: Noche` | Regenera Cala Sombría de noche |
| `Abby/Separar superficies encimadas` | Corrige caras en el mismo plano; **hay que correrlo de nuevo si se regenera un mapa** |
| `HoleAudit`, `TreeAudit` | Buscan huecos en el terreno y árboles que tapan la cámara |
| `DioramaRoute` | Salta al siguiente piso para probar |

## Recursos de terceros

| Recurso | Licencia | Uso |
| --- | --- | --- |
| Inter SemiBold | OFL | Texto del juego |
| Press Start 2P | OFL | Logo |
| Kenney Impact Sounds | CC0 | Referencia para los efectos; en `References/`, fuera del build |

## Compilación

Ejecutable de Windows `AbbysTower.exe`, unos 330 MB, con las 14 escenas de la ruta. El recorte de shaders de posproceso de URP está desactivado para que bloom, color y viñeta funcionen en el ejecutable.
