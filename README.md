# ⚽ AlberSoccer — Sevilla FC vs Real Betis

Juego de fútbol arcade **en vista lateral**, escrito en un único archivo HTML (Canvas 2D, sin
librerías ni dependencias). Los del **Sevilla** son todos guapísimos; los del **Betis**, trolls
horribles. Y la regla de oro del Albertirrey Stadium:

> **Si marca el Sevilla, es GOL. Si marca el Betis, el VAR lo anula por fuera de juego.**

## Cómo jugar

Abre `index.html` en cualquier navegador moderno. No hace falta servidor ni instalación.

| Acción | Teclado | Táctil |
|---|---|---|
| Mover | `← ↑ ↓ →` o `WASD` | joystick (mitad izquierda) |
| Tiro (mantener carga la potencia) / entrada | `ESPACIO` | botón **TIRO** |
| Pase / cambiar de jugador | `C`, `X` o `INTRO` | botón **PASE** |
| Sprint | `MAYÚS` | botón **SPRINT** |
| Pausa | `P` o `ESC` | botón ❚❚ |

Controlas siempre al jugador del Sevilla más cercano al balón (marcado con la flecha amarilla).
Al dar un pase, el control pasa automáticamente al receptor.

En el menú puedes elegir **duración** (2×45 s, 2×90 s o 2×3 min) y **dificultad**
(Paseíllo, Normal, Derbi, Troll).

## Qué hay dentro

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
