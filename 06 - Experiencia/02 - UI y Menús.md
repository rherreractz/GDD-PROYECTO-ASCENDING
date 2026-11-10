# UI y menús

Textos literales de `MenuPrincipal.cs` y `PauseMenu.cs`.

## Menú principal

Fondo: paisajes del juego (puerto, cascadas, acantilado y cima) con paneo lento y fundido a negro entre uno y otro; la música cambia con cada paisaje.

- Título: `ABBY'S TOWER` · `La torre del abismo`
- Opciones:
  - `Continuar · Piso N` (solo con partida guardada)
  - `Nueva partida`
  - `Configuración`
  - `Créditos`
- La opción elegida se marca con `◆`.
- Pie: `↑ ↓ elegir · Enter aceptar · ← → ajustar volumen · Esc regresar`

### Configuración

| Opción | Formato |
| --- | --- |
| Volumen general | `Volumen general < 80 % >` |
| Volumen de música | `Volumen de música < 70 % >` |
| Volumen de efectos | `Volumen de efectos < 90 % >` |
| Pantalla completa | `Pantalla completa: Sí / No` |

### Salir

`¿Salir del juego?` → `No, quedarme` · `Sí, salir del juego`

### Créditos

| Rol | Persona |
| --- | --- |
| Dirección y programación | Rodrigo Herrera |
| Programación y arte | Gabriel García |
| Música y sonido | Francisco Uc |
| Experiencia de usuario | Ricardo Cetina |
| Pruebas y experiencia de usuario | Karla Damaris |

`Un proyecto de Estudio 02` · `Integradora · IDYGS103` · `Universidad Tecnológica de Cancún`

## Pausa (`Esc`)

- Encabezado: `P A U S A` · `ABBY'S TOWER · <piso>` · `N notas encontradas`
- `Continuar`
- `Opciones`
- `Reiniciar piso` (en Cala Sombría: `Reiniciar exterior`)
- `Salir al menú` → al pulsarlo cambia a `¿Seguro? Pulsa otra vez` durante `3 s`
- Pie: `↑ ↓ elegir · Enter / A aceptar · Esc / B continuar`

### Opciones → `M O D O   D E   J U E G O`

Cuatro tarjetas con nombre, descripción y color:

| Modo | Descripción en pantalla |
| --- | --- |
| FÁCIL | Para disfrutar la historia. Recibes la mitad de daño. |
| NORMAL | La experiencia pensada para el juego. |
| DIFÍCIL | Enemigos más duros y agresivos. Curarte rinde menos. |
| PESADILLA | Triple de daño y enemigos implacables. Solo para quien ya conoce la torre. |

Bajo las tarjetas, un resumen: `Daño recibido x… · Vida enemigos x… · Curación x… · Al morir pierdes …`. Efecto real de cada modo en [[03 - Sistemas]].

## Pantalla de carga

Título y subtítulo del piso, barra de progreso, `Cargando...` y un consejo al azar:

- "Clic derecho sostenido: bloquear. Recibes solo el 8 % del daño, pero gasta stamina."
- "Las sombras rojas del suelo avisan cada ataque."
- "Shift: impulso. Atraviesa las barreras de energía."
- "Las fuentes de curación restauran toda tu vida, pero cada una sirve una vez."
- "Tres clics seguidos hacen un combo: el tercer golpe pega más."

La carga es asíncrona: la escena siguiente se prepara en segundo plano y entra al llegar al 90 %.

## Navegación

Todos los menús funcionan con mouse, teclado y mando. Atajos en [[04 - Controles]].
