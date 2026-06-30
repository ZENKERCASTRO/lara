[README.md](https://github.com/user-attachments/files/29502746/README.md)
# 🐾 ¡Alcanza a Richard! — Juego 8-bits (vertical, móvil)

Un mini-juego en pixel art (HTML5 + Canvas, sin dependencias) optimizado para
**pantallas de móvil en vertical**. Lara corre automáticamente por el camino
de un parque persiguiendo a su caniche blanco **Richard**, que va delante.
Tú solo te mueves a los lados (deslizando el dedo) para esquivar bancos,
arbustos, conos, charcos y otros perros que están paseando por el camino.
No hay que saltar: todo el reto está en esquivar de lado a lado y aprovechar
los momentos en que Richard se para a olfatear para acercarte y atraparlo,
5 veces antes de que se acabe el tiempo.

No necesita instalación ni librerías: es un único archivo `index.html`.

## ▶️ Jugar en local

Abre `index.html` con doble clic en cualquier navegador (se ve mejor en
móvil o achicando la ventana en vertical).

## 🎮 Controles

- **Deslizar el dedo / arrastrar el ratón** sobre el camino: mover a Lara a los lados
- **← → / A D**: alternativa de teclado
- **R**: reiniciar (en pantalla de victoria/derrota)
- Botones ◀ ▶ en pantalla como apoyo táctil adicional

La barra de color bajo el marcador indica lo cerca que está Richard: verde =
muy cerca (¡atrápalo!), amarillo = a media distancia, rojo = se está
escapando.

## 🚀 Subirlo a GitHub Pages (paso a paso)

1. Crea un repositorio nuevo en GitHub (por ejemplo `alcanza-a-richard`).
2. Sube el archivo `index.html` (y este `README.md`) a la raíz del
   repositorio. Puedes hacerlo desde la web de GitHub con
   "Add file → Upload files", o por terminal:
   ```bash
   git init
   git add index.html README.md
   git commit -m "Juego: Alcanza a Richard"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/alcanza-a-richard.git
   git push -u origin main
   ```
3. En GitHub, ve a **Settings → Pages**.
4. En "Build and deployment", elige **Source: Deploy from a branch**.
5. Selecciona la rama **main** y la carpeta **/ (root)**, luego **Save**.
6. Espera 1-2 minutos. Tu juego quedará publicado en:
   `https://TU_USUARIO.github.io/alcanza-a-richard/`

¡Y listo! Puedes compartir ese enlace con quien quieras para que jueguen
desde el navegador, sin instalar nada, incluso desde el móvil.

## 🛠️ Personalizarlo

Todo el juego está en un único archivo `index.html`, comentado por
secciones:

- **Sprites**: los personajes son matrices de texto (pixel art) en las
  constantes `LARA_FRAME_*` y `RICHARD_FRAME_*`, con sus colores en
  `laraColors` / `richardColors`. Los perros de otros paseantes usan
  `npcDogColorsBrown` / `npcDogColorsBlack`. Puedes cambiar colores de pelo,
  ropa o arnés ahí mismo.
- **Dificultad**: cambia `TOTAL_TIME` (segundos totales) o `SCROLL_SPEED`
  (velocidad de avance del camino).
- **Obstáculos**: la función `genObstacles()` genera bancos, arbustos,
  charcos, conos y perros paseando a lo largo del camino.

