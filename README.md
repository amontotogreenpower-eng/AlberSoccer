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
| Tiro | `ESPACIO` | botón **TIRO** |
| Pase / cambiar de jugador | `C` o `INTRO` | botón **PASE** |
| Regate (recorte + acelerón) | `X` o `Z` | botón **REGATE** |
| Entrada (robar el balón) | `V` o `B` | botón **ENTRADA** |
| Sprint | `MAYÚS` | botón **SPRINT** |
| Pantalla completa | `F` | botón ⛶ |
| Pausa | `P` o `ESC` | botón ❚❚ |

### Dinámica

**El balón se queda contigo en cuanto llegas a él.** Al alcanzarlo lo controlas y lo conduces
por delante con toques y bote; se pierde si te lo roban, si te barren o al golpear. Cuanto más
rápido corres, más lejos lo llevas.

- **Barra de potencia oscilante**: mantén pulsado `ESPACIO` y la barra sube y baja sobre tu
  jugador; el disparo sale al soltar, con la potencia que marque en ese instante. Si no tienes
  el balón, el golpeo se produce en cuanto lo alcanzas.
- **Golpeos con espectáculo**: el balón deja una estela de cometa que arde en los cañonazos,
  el punto de golpeo suelta un fogonazo y una doble onda sobre el césped, la cámara acusa el
  impacto y los disparos más fuertes ralentizan el tiempo un instante.
- **Dirección de 8 rumbos**: el golpeo va hacia donde apuntas. Cerca del área, apuntar hacia
  la portería dirige el tiro a puerta y el eje vertical elige el palo.
- **Robo**: quitar el balón por delante es más fácil que por la espalda, y quien va a por él
  aprieta mejor que un compañero cualquiera. Hay un instante de gracia tras controlarlo.
- **Porteros de verdad**: no hay tirada secreta de "parada"; el portero para si su estirada
  llega físicamente al balón, y sale a achicar cuando le entran conduciendo.
- **Cambio de jugador**: controlas al del Sevilla más cercano al balón (flecha amarilla), pero
  quien lo lleva conserva el mando; con `C` lejos del balón cambias a mano.
- **Entrada**: barrida dirigida al rival que lleva el balón o, si no lo hay, al balón.
- **Regate**: recorte hacia donde apuntes con acelerón; los rivales pegados se quedan clavados.
- **Pase al hueco**: el balón se envía por delante del compañero, y un aro verde marca a quién
  va dirigido. El control pasa al receptor.

En el menú puedes elegir **duración** (2×1 min, 2×2 min o 2×4 min), **dificultad**
(Paseíllo, Normal, Derbi, Troll) y si quieres el **pad en pantalla** (Auto / Siempre / Nunca);
en "Auto" aparece solo en pantallas táctiles, pero también funciona con el ratón.

Los mandos en pantalla son un pad direccional grande a la izquierda —con la flecha activa
iluminada— y cinco botones en rombo a la derecha, cada uno con su icono y su color: ⚽ TIRO,
➜ PASE, ⚡ REGATE, 🦶 ENTRADA y » SPRINT. En pantallas apaisadas bajas se reescalan solos.

## Qué hay dentro

- **Toque por contacto**: no existe la posesión adherida; un sistema de intenciones
  (conducir / pasar / chutar) decide qué ocurre en el instante del golpeo, tanto para ti
  como para la IA.
- **Perspectiva real**: proyección de cámara con distancia focal, altura y horizonte, así que
  el campo, las porterías, las líneas y los jugadores escalan según su profundidad.
- **Realización televisiva**: una cámara de banda con zona muerta, anticipación y temblor de
  operador, que corta entre plano general (saques y envíos largos), plano medio y plano corto
  (jugadas de área). El graderío escala y se desplaza con ella, así que fondo y campo siempre
  cuadran.
- **Repetición instantánea**: se graban los últimos cinco segundos de juego y, tras un gol del
  Sevilla, se emiten a cámara lenta desde una segunda cámara —más baja y cerrada— con su rótulo
  de repetición, antes de volver a la celebración.
- **Orientación real de los jugadores**: el cuerpo no se voltea como un folio. Cada jugador
  tiene un ángulo en el plano del campo y su esqueleto se proyecta en 3D, de modo que se les ve
  de perfil, de frente (con la cara y el escudo) y de espaldas (con la nuca y el dorsal), y el
  torso se ensancha o estrecha según el giro.
- **Zancada sin patinaje**: la fase del paso avanza con la distancia recorrida, no con el reloj,
  y la pierna de apoyo retrocede de forma lineal, así que el pie se queda clavado en el césped.
  El cuerpo además gira de forma progresiva y se inclina al acelerar o frenar.
- **Jugadores dibujados a mano**: esqueleto animado (cadera, rodilla, tobillo, hombro, codo)
  con extremidades cilíndricas sombreadas, ciclo de carrera, chut, barrida, estirada del
  portero, celebración y llanto.
- **Caras generadas por jugador**: los del Sevilla tienen mandíbula marcada, peinados con
  brillo, pestañas, sonrisa y destellos ✨; los del Betis tienen piel verde con verrugas,
  narizota ganchuda, uniceja, colmillos torcidos, babilla y moscas revoloteando.
- **Estadio**: graderío con filas, pasillos, pancartas, focos, flashes de cámaras, público
  que salta en los goles y vallas publicitarias delante y detrás.
- **Se adapta a la pantalla**: el ancho del campo visible depende del formato del monitor —en
  panorámicas se ve el terreno entero y no hay bandas negras—, los mandos escalan con la altura
  disponible y en vertical avisa de girar el dispositivo.
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
