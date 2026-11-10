# Guardado y configuración

Todo se guarda con `PlayerPrefs` de Unity (en Windows, el registro del usuario). No hay archivos de guardado.

## Qué se guarda

| Clave | Contenido | Se escribe | Archivo |
| --- | --- | --- | --- |
| `progreso_escena` | Nombre de la última escena de la ruta | Al cargar una escena de la ruta | `Progreso.cs` |
| `abby.difficulty` | Modo de juego (0 a 3) | Al cambiarlo en Opciones | `Difficulty.cs` |
| `vol_general`, `vol_musica`, `vol_efectos` | Volúmenes de 0 a 1 en pasos de 0,1 | Al ajustarlos | `MenuPrincipal.cs` (`Ajustes`) |
| Estilo e inclinación de cámara | Vista elegida con `F5` / `F6` | Al cambiarla | `MouseOrbitCamera.cs` |

## Continuar partida

- Al entrar a un lugar de la ruta se anota su escena. El menú muestra `Continuar · Piso N`.
- `Continuar` carga esa escena desde el principio, con vida completa.
- Al terminar el juego (final con Dante) el guardado **se borra**.
- `Nueva partida` empieza en el tutorial.

> **Limitación conocida:** la lista de escenas que se guardan es `Exterior, Diorama, CuartosA, Puerto, Cascadas, Acantilado, Cima`. **No incluye `Cueva`, `Lago` ni `Nevado`** (pisos 5, 6 y 7, agregados el 5 de noviembre). Si la partida se interrumpe en esos pisos, `Continuar` regresa al piso 4. Ver [[05 - Seguridad y Riesgos Técnicos]].

## Qué no se guarda

| Dato | Comportamiento |
| --- | --- |
| Vida entre pisos | Vive en memoria (`RunState.SavedHealth`); se pierde al cerrar el juego |
| Hordas derrotadas dentro de un piso | No; el piso empieza de cero |
| Notas encontradas | Solo durante la sesión |
| Fuentes usadas | Se restablecen al reiniciar el piso |

## Configuración disponible

Volumen general, de música y de efectos; pantalla completa; modo de juego. Detalle en [[02 - UI y Menús]].

## Cambio respecto al GDD 0.6.0

El GDD decía "sin guardado". Se añadió `Continuar` para que una falla en la presentación no obligue a empezar de cero. Registrado en [[03 - Registro de Decisiones]].
