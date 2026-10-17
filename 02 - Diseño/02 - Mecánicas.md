# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

## Plantilla de mecánica

### Nombre de la mecánica

**Propósito:**  
¿Qué aporta a la experiencia?

**Activación:**  
¿Qué debe hacer el jugador?

**Reglas:**  
¿Qué puede y qué no puede ocurrir?

**Entrada:**  
¿Qué botón, gesto o acción la activa?

**Estado inicial:**

**Estado final:**

**Recursos utilizados:**

**Recompensa:**

**Penalización:**

**Interacciones con otras mecánicas:**

**Casos límite:**  
¿Qué ocurre en situaciones poco comunes?

## Mecánicas principales

### Mecánica 01 — Ataque con espada

**Propósito:** Ataque principal de Abby, al menos en el primer nivel.

**Activación:** Presionar el botón de ataque.

**Entrada:** Clic izquierdo.

**Reglas:** Animación de 4-5 frames. Daño cuerpo a cuerpo con alcance corto. Es la única arma de la demo. Combo de **3 ataques** con clics seguidos.

> [!tip] Propuesta (por aprobar)
> Daño del combo: 10 / 10 / 15.
> Ventana entre clics: 0.6 s; si se pasa, el combo vuelve a empezar.

### Mecánica 02 — Bloqueo y lectura de sombras

**Propósito:** Dar legibilidad al combate al estilo soulslike.

**Entrada:** Clic derecho (por confirmar).

**Reglas:** Las sombras en el suelo indican cuándo atacar y cuándo bloquear. Mientras bloquea, Abby recibe solo el **8 %** del daño del ataque, pero **no es inmune**. Bloquear **gasta stamina**, por lo que no se puede bloquear indefinidamente.

> [!tip] Propuesta (por aprobar)
> Stamina total: 100. Cada golpe bloqueado gasta 20.
> Atacar no gasta stamina.
> Se regenera a 25 por segundo tras 1 s sin bloquear.

### Mecánica 03 — Movimiento

**Entrada:** WASD.

**Reglas:** Movimiento en un espacio 2.5D con cámara que sigue al jugador.

## Mecánicas secundarias

- Fuentes de curación: en ciertos puntos de los pisos, restauran el 100 % de la vida.
- Cámara que sigue al jugador.
- Límites del área jugable (muros con cuadrícula en el prototipo de escenario).


> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
