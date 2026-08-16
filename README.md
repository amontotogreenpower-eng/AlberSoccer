# ⚽ AlberSoccer — Sevilla FC vs Real Betis

Juego de fútbol arcade **en vista lateral**, escrito en un único archivo HTML (Canvas 2D, sin
librerías ni dependencias). Los del **Sevilla** son todos guapísimos; los del **Betis**, trolls
horribles. Y la regla de oro del Albertirrey Stadium:

> **Si marca el Sevilla, es GOL. Si marca el Betis, el VAR lo anula por fuera de juego.**

## Cómo jugar

Abre `index.html` en cualquier navegador moderno. No hace falta servidor ni instalación.

| Acción | Teclado | Pad en pantalla |
|---|---|---|
| Mover (8 direcciones) | `← ↑ ↓ →` o `WASD` | pad direccional |
| Tiro / entrada | `ESPACIO` | botón **TIRO** |
| Pase / cambiar de jugador | `C`, `X` o `INTRO` | botón **PASE** |
| Sprint | `MAYÚS` | botón **SPRINT** |
| Pausa | `P` o `ESC` | botón ❚❚ |

### Dinámica al estilo *Match Day II*

**El balón no va pegado al pie.** Cada vez que alcanzas el balón le das un toque, y hay que ir
a por él otra vez: conducir es una sucesión de toques, y si esprintas se te escapa. De ahí que
el ritmo sea pausado y que colocarse importe más que correr.

- **Barra de potencia oscilante**: mantén pulsado `ESPACIO` y la barra sube y baja sobre tu
  jugador. El disparo sale **en el instante en que alcanzas el balón**, con la potencia que
  marque la barra en ese momento (tienes una ventana de gracia si sueltas justo antes).
- **Dirección de 8 rumbos**: el golpeo va hacia donde apuntas. Cerca del área, apuntar hacia
  la portería dirige el tiro a puerta y el eje vertical elige el palo.
- **Rechaces**: un balón que te llega de frente rebota en ti en lugar de quedar controlado,
  así que los despejes y las carambolas son parte del juego.
- **Porteros de verdad**: no hay tirada secreta de "parada"; el portero para si su estirada
  llega físicamente al balón. Si no llega, es gol.
- **Cambio de jugador**: controlas al del Sevilla más cercano al balón (flecha amarilla), pero
  quien acaba de tocarlo conserva el mando; con `C` lejos del balón cambias a mano.

En el menú puedes elegir **duración** (2×1 min, 2×2 min o 2×4 min), **dificultad**
(Paseíllo, Normal, Derbi, Troll) y si quieres el **pad en pantalla** (Auto / Siempre / Nunca);
en "Auto" aparece solo en pantallas táctiles, pero también funciona con el ratón.

## Qué hay dentro

- **Toque por contacto**: no existe la posesión adherida; un sistema de intenciones
  (conducir / pasar / chutar) decide qué ocurre en el instante del golpeo, tanto para ti
  como para la IA.
- **Perspectiva real**: proyección de cámara con distancia focal, altura y horizonte, así que
  el campo, las porterías, las líneas y los jugadores escalan según su profundidad.
- **Jugadores dibujados a mano**: esqueleto animado (cadera, rodilla, tobillo, hombro, codo)
  con extremidades cilíndricas sombreadas, ciclo de carrera, chut, barrida, estirada del
  portero, celebración y llanto.
- **Caras generadas por jugador**: los del Sevilla tienen mandíbula marcada, peinados con
  brillo, pestañas, sonrisa y destellos ✨; los del Betis tienen piel verde con verrugas,
  narizota ganchuda, uniceja, colmillos torcidos, babilla y moscas revoloteando.
- **Estadio**: graderío con filas, pasillos, pancartas, focos, flashes de cámaras, público
  que salta en los goles y vallas publicitarias delante y detrás.
- **Partido completo**: dos partes con cambio de campo, reloj de 90 minutos, saques de banda,
  de esquina y de puerta, porteros con estiradas, palos, comentarista y estadísticas finales.
- **Secuencia VAR** para cada gol del Betis: monitor con líneas de escaneo, líneas de fuera de
  juego dibujadas en perspectiva sobre el campo y sello de **GOL ANULADO**.
- **Sonido sintetizado** con la Web Audio API (silbato, golpeos, palo, murmullo de grada que
  sube en las ocasiones, pitidos del VAR).

## Ficheros

```
index.html      el juego entero (motor, gráficos, audio y UI)
manifest.json   metadatos para instalarlo como app
icon.svg        icono
```

Para depurar hay un objeto `window.ALBER` con el estado del partido (`G`, `teams`, `ball`,
`allPlayers`, `newMatch()`), útil para forzar situaciones desde la consola.
