# 🐾 ¡Alcanza a Richard! — Juego 8-bits

Un mini-juego en pixel art (HTML5 + Canvas, sin dependencias) donde **Lara**
persigue a su caniche blanco **Richard** por el parque. Hay que esquivar o
saltar bancos, arbustos y conos, evitar frenarte en los charcos, y atrapar a
Richard 5 veces antes de que se acabe el tiempo.

No necesita instalación ni librerías: es un único archivo `index.html`.

## ▶️ Jugar en local

Simplemente abre `index.html` con doble clic en cualquier navegador.

## 🎮 Controles

- **← → / A D**: mover a Lara
- **Espacio / ↑**: saltar
- **R**: reiniciar (en pantalla de victoria/derrota)
- En móvil: botones táctiles en pantalla

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
desde el navegador, sin instalar nada.

## 🛠️ Personalizarlo

Todo el juego está en un único archivo `index.html`, comentado por
secciones:

- **Sprites**: los personajes son matrices de texto (pixel art) en las
  constantes `LARA_FRAME_*` y `RICHARD_FRAME_*`, con sus colores en
  `laraColors` / `richardColors`. Puedes cambiar colores de pelo, ropa o
  arnés ahí mismo.
- **Dificultad**: cambia `timeLeft` (segundos totales) o las velocidades
  `lara.speed` / `richard.baseSpeed`.
- **Obstáculos**: la función `genObstacles()` genera bancos, arbustos,
  charcos y conos a lo largo del nivel.
