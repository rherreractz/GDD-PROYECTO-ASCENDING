# Seguridad y riesgos técnicos

## Seguridad

El juego no se conecta a internet, no pide datos personales y no escribe fuera de `PlayerPrefs`. No hay superficie de ataque relevante.

## Riesgos para la presentación

| # | Riesgo | Impacto | Mitigación |
| ---: | --- | --- | --- |
| 1 | `Continuar` no registra los pisos 5, 6 y 7 (`Progreso.Ruta` no los lista) | Tras una falla en esos pisos se vuelve al piso 4 | Conocido. Si pasa en la demo, usar `Continuar` y avisar; corregirlo es añadir tres nombres a la lista |
| 2 | Nadie ha jugado la partida completa de corrido | Un fallo entre escenas podría aparecer en vivo | Partida completa por alguien ajeno al desarrollo antes del 20; ver [[02 - Pruebas]] |
| 3 | Rendimiento en combate sin medir en el ejecutable | Caídas de cuadros con 4 enemigos y partículas | Medir en la laptop de presentación; el editor dio 57 FPS con 6 enemigos |
| 4 | Con 8 pisos la demo puede pasar de 15 minutos | Fila en el stand | Medir; como respaldo, empezar con `Continuar` en un piso avanzado |
| 5 | La fuente solo responde a `E` | Quien juegue con mando no puede curarse | Tener el teclado a la mano o presentar con teclado y mouse |
| 6 | Audio final sin integrar | Suena el sintetizado | Es funcional; el reemplazo es automático al copiar los archivos |
| 7 | La laptop de presentación falla | Sin demo | Copia del ejecutable en una segunda máquina y en USB |

## Inconsistencias conocidas en `bf6203d`

| Tema | Detalle |
| --- | --- |
| Modos de juego | Las tarjetas anuncian "Daño recibido" y "Curación", pero `Difficulty.damageTaken` y `healing` no se usan en ningún script. El modo sí cambia vida, velocidad y pausa de los enemigos |
| Daño enemigo | Los valores de `damage` por encima de `15` (Bruto `20`, Guardián `16`, golpe de área `28`) se recortan a `15` en `PlayerHealth` |
| Textos de "bajar" | Varias notas y la intro hablan de bajar pisos; el juego es de subir |
| Consejo de carga | Uno menciona al mercader y los minerales, que no están en la ruta |
| Rótulos sin usar | `DioramaBuilder.Info` conserva nombres de jefes por piso que no aparecen |

## Riesgos del entorno de desarrollo

| Problema | Qué hacer |
| --- | --- |
| Ventana "Connect to server" al abrir Unity | Es Plastic: `Cancel`, sin meter datos |
| Unity se queda en "Reloading Domain" con CPU casi en cero | Está colgado: cerrar y volver a abrir |
| Disco lleno por `Editor.log` (aviso "Layout update failed" repetido) | Borrar `%LOCALAPPDATA%\Unity\Editor\Editor.log` con Unity cerrado |
| El juego no avanza con Unity minimizado | Las pruebas usan `Application.runInBackground = true` |
| Regenerar un mapa deshace correcciones | Volver a correr `Abby/Separar superficies encimadas` y guardar la escena |

## Deuda técnica

- `PlayerController.cs` y `CombatInputReader.cs` son el primer sistema de combate (con parry); el juego usa `AbbyAttack`, `AbbyBlock` y `AbbyDash`. Conviene retirarlos.
- Escenas `Nivel1` a `Nivel9`, `Templo`, `Montana` y `SampleScene` siguen en el proyecto, apagadas en el build.
- Las herramientas temporales de `Assets/Editor` no van en Git ni en el ejecutable, pero hay que borrarlas de la carpeta antes de entregar el proyecto.
