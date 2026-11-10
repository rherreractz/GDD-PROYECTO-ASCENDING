# Entregas y trabajo pendiente

## Entregado (`animaciones` @ `bf6203d`)

| ID | Tarea | Comprobación en el proyecto |
| --- | --- | --- |
| COM-01 | Combo de 3 tajos `10 / 10 / 15` | `AbbyAttack.damage`; cuadros en `Resources/AbbyAnim/Tajo1..3` |
| COM-02 | Bloqueo al 8 % con stamina | `AbbyBlock`: `DanoRecibido = 0.08`, `CostoPorGolpe = 20`, `Regeneracion = 25` |
| COM-03 | Impulso con invulnerabilidad y costo | `AbbyDash`: `iframes = 0.26`; `AbbyBlock.CostoImpulso = 20` |
| COM-04 | Esquiva perfecta y tajo de impulso | `PlayerHealth.PerfectDodge`; `AbbyAttack.OnPerfectDodge` |
| COM-05 | Asistencia de apuntado | `AbbyAttack.AimAssist` |
| ENE-01 | Seis enemigos con sprites y animaciones | `TowerEnemy.Configure`; `Resources/EnemigosAnim` |
| ENE-02 | El ataque sigue al dibujo | `TowerEnemy.FaseAtaque()` |
| ENE-03 | Aparición desde grieta | `CombatFx.Grieta` |
| JEF-01 | Dante con 3 patrones y fase 2 al 50 % | `TowerEnemy.Dante.cs` (`ChooseDante`) |
| JEF-02 | Dante cae sin morir y lleva al final | `TowerEnemy.DanteDerrotado`; `DanteFinal` |
| HOR-01 | 4 hordas por piso sobre el camino | `DioramaBuilder.Hordas`; 4 `RoomEncounter` por escena |
| HOR-02 | Baliza de la siguiente horda | `GuiaHordas` |
| PIS-01 | Ocho pisos y la Biblioteca | 9 escenas con `FloorExit.nextScene` encadenado |
| PIS-02 | Cala Sombría de noche | `ExteriorBuilder.Cala`, `ExteriorNoche` |
| TUT-01 | Tutorial con Dante humano | `ExpedicionPiso20`; `Resources/DanteHumano` |
| HIS-01 | Intro en imágenes | `IntroImagenes.Guion`; `Resources/Intro` (14) |
| HIS-02 | Relato por piso y notas | `Historia.Relato`, `Historia.Notas`; 18 `LoreNote` |
| HIS-03 | Escena final y créditos | `EscenaFinal`, `DanteFinal`; escena `Final` |
| UI-01 | HUD con vida, stamina, retrato y controles | `FloorDirector.OnGUI` |
| UI-02 | Menú principal, configuración y créditos | `MenuPrincipal` |
| UI-03 | Pausa y modos de juego | `PauseMenu`, `Difficulty` |
| SIS-01 | Continuar partida | `Progreso` |
| SIS-02 | Pantalla de carga asíncrona | `Cargador` |
| SIS-03 | Reaparición al caer | `FallGuard` |
| AUD-01 | Música y efectos sintetizados | `Musica`, `Sonido` |
| BLD-01 | Ejecutable con ícono y 14 escenas | `EditorBuildSettings.asset` |

## Pendiente antes del 20 de noviembre

| ID | Tarea | Responsable | Prioridad |
| --- | --- | --- | --- |
| QA-01 | Partida completa de corrido, 15 minutos | Equipo | Alta |
| QA-02 | Prueba por una persona ajena al desarrollo | Karla / Ricardo | Alta |
| QA-03 | Rendimiento del ejecutable en combate y en otra PC | Equipo | Alta |
| GIT-01 | Pasar `animaciones` a `dev` con un PR | Gabriel / Rodrigo | Media |
| AUD-02 | Audio final en `Assets/Resources/Audio/` | Francisco | Media |
| DOC-01 | Capturas del juego para este GDD | Equipo | Media |
| LIM-01 | Borrar herramientas temporales de `Assets/Editor` | Gabriel | Baja |

## Correcciones candidatas

Solo si el equipo decide reabrir el código; hoy está congelado. Detalle en [[03 - Bugs y Seguimiento]].

| ID | Corrección | Tamaño |
| --- | --- | --- |
| FIX-01 | Añadir `Cueva`, `Lago` y `Nevado` a `Progreso.Ruta` | Una línea |
| FIX-02 | Botón de mando para la fuente | Una línea |
| FIX-03 | Aplicar o quitar "Daño recibido" y "Curación" de los modos | Pequeño |
| FIX-04 | Unificar textos de "bajar" a "subir" | Solo texto |
| FIX-05 | Quitar el consejo de carga del mercader | Una línea |
