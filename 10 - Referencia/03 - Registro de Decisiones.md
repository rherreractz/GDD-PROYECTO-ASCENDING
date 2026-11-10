# Registro de decisiones

Decisiones vigentes en `bf6203d`, con su motivo. Fuente: `Docs/Cambios_respecto_al_GDD.md`, `PENDIENTE_GDD.md` y acuerdos del equipo.

| Fecha | Área | Decisión | Motivo |
| --- | --- | --- | --- |
| Preprod. | Historia | La torre misteriosa y melancólica; Abby busca a su hermano | Da un motivo personal al ascenso |
| Preprod. | Nombres | El hermano es Dante; el padre, Angelo; el capitán, Elías Vargas; el pueblo, Cala Sombría | Definidos por el equipo; viven en `Historia.cs` |
| Preprod. | Dirección | La torre **se sube** (nombre clave Ascending) | Corrige el guion original, que bajaba a un abismo |
| Preprod. | Enemigos | Sin enemigos humanos | Costo de los sprites |
| 20 oct | Protagonista | Se llama Abby, no "Abis" | El GDD manda sobre el guion |
| 20 oct | Combate | Combo `10 / 10 / 15` y bloqueo con stamina, **conservando salto e impulso** | Los mapas usan saltos; el impulso gasta `20` de stamina para que no se abuse |
| 20 oct | Armas | Solo espada | Un sistema bien terminado |
| 20 oct | Objetos | Solo notas; fuera mercader, cofres, pociones y minerales | GDD 0.6.0 |
| 20 oct | Jefes | Un único jefe: Dante | GDD 0.6.0; los otros cuatro quedan dibujados y sin usar |
| 20 oct | Cámara | Fija; `F3` cámara libre, `F4` vuelve | Para poder mostrar los mapas |
| 20 oct | Guardado | `Continuar` guarda el último lugar y se borra al terminar | Si algo falla en la presentación no se empieza de cero |
| 20 oct | Lugares | Se suman Cala Sombría y la Biblioteca (una horda) | Aportan a la historia y al ritmo |
| 20 oct | Orden | Tutorial → Cinemática | Del guion: primero se vive la expedición, luego se explica |
| Oct | Intro | Imágenes fijas con paneo, no cinemática en tiempo real | Menos costo de arte; el mismo efecto emocional |
| Oct | Tutorial | Prólogo jugable con Dante en el piso 20 | Enseña los controles y presenta a quien se va a buscar |
| 1–2 nov | Luz | Los pisos de día pasan al atardecer | Tono de la historia; no requiere regenerar escenas |
| 1–2 nov | Animación | El ataque enemigo sigue al dibujo: mitad carga, mitad golpe | Que lo que se ve sea lo que pega |
| 3 nov | Combo | Tres tajos con animación propia de 4–5 cuadros | Antes usaba la pose del impulso |
| 3 nov | Bloqueo | Es una pose, sin animación | Presupuesto de generaciones de arte |
| 4 nov | Cala Sombría | De noche y 3 veces más grande | Coincide con las imágenes de la intro |
| 5 nov | Pisos | **Ocho** en lugar de cinco: Gruta, Lago y Aldea nevada | Dar espacio a la historia de regreso de Dante |
| 5 nov | Final | Escena propia sin enemigos, con créditos | El reencuentro necesita su propio lugar |
| 5 nov | Historia | El colgante del padre une principio y final | Hilo emocional concreto |
| 5 nov | Tutorial | Dante humano con sprites propios; el golpe del Coloso corta a negro | No mostrar qué les pasó |
| 5 nov | Tipografía | Inter para el texto; Press Start 2P solo en el logo | Legibilidad |
| 5 nov | Paleta | No se fuerza DawnBringer 32 | 0 % de píxeles exactos; cambiaría todo el arte |
| 6 nov | Cámara | Toma aérea de entrada en todos los pisos; se abre tras 6 s en reposo | Mostrar el paisaje sin quitar el control |
| 9 nov | Audio | Sintetizado por código, reemplazable por archivos | Funciona sin esperar al audio final |
| 10 nov | Alcance | Juego congelado en `bf6203d`; solo pruebas hasta el 20 | Estabilidad para la presentación |

## Decisiones abiertas

| Tema | Opciones |
| --- | --- |
| Jefes dibujados sin usar | Dejarlos fuera o sumarlos después de la demo |
| Correcciones B-01 a B-05 | Reabrir el código para cinco cambios pequeños o aceptarlos para la demo |
| Audio final | Integrarlo antes del 20 o presentar con el sintetizado |
