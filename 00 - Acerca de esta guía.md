# Acerca de esta guía

Este GDD describe el juego **como quedó construido**, no como se planeó. Reglas del documento:

- **Un dato, un lugar.** Cada valor vive en una sola nota y las demás lo enlazan. Los números de combate están en [[02 - Mecánicas]]; los de enemigos, en [[03 - Enemigos y NPC]].
- **Fuente citada.** Los valores van en `código` junto al archivo de donde salen (`AbbyAttack.cs`, `Abby.prefab`, escena `Cima.unity`).
- **Textos literales.** Los rótulos de HUD y menús se copian tal como aparecen en pantalla.
- **Diferencias a la vista.** Donde el juego se aparta del GDD 0.6.0 o donde el código tiene una inconsistencia, se dice en la nota y se reúne en [[03 - Registro de Decisiones]] y [[05 - Seguridad y Riesgos Técnicos]].
- **Pendiente** marca lo que el código no puede responder (resultados de pruebas con personas, capturas del juego corriendo, proceso de audio final).

| Convención | Significado |
| --- | --- |
| `m/s`, `s`, `m` | Unidades de Unity: metros y segundos |
| Piso N | Número que ve el jugador en la pantalla de carga |
| `Escena` | Nombre del archivo `.unity` |
| Modo Normal | Todos los valores se dan en modo Normal salvo que se indique |
