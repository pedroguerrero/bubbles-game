# Bubbles

Juego de burbujas hecho en HTML5 Canvas puro, sin dependencias. 10 etapas con dificultad progresiva.

## Cómo jugar

- **Mueve el mouse** (o arrastra el dedo) para apuntar
- **Haz clic** (o levanta el dedo) para disparar
- Junta **3 o más burbujas del mismo color** para hacerlas explotar
- Las burbujas que queden flotantes (sin conexión al techo) también caen y dan puntos
- Si las burbujas llegan a la línea roja de peligro, es **Game Over**

## Sistema de etapas

| Etapa | Colores | Filas iniciales | Presión (filas cada N disparos) | Burbujas piedra |
|:---:|:---:|:---:|:---:|:---:|
| 1 | 3 | 3 | sin presión | No |
| 2 | 3 | 4 | sin presión | No |
| 3 | 4 | 4 | cada 14 | No |
| 4 | 4 | 5 | cada 12 | No |
| 5 | 5 | 5 | cada 10 | No |
| 6 | 5 | 6 | cada 8 | Sí (7%) |
| 7 | 6 | 6 | cada 7 | Sí (14%) |
| 8 | 6 | 7 | cada 6 | Sí (21%) |
| 9 | 6 | 8 | cada 5 | Sí (25%) |
| 10 | 6 | 9 | cada 4 | Sí (25%) |

## Recompensas

| Acción | Efecto |
|---|---|
| Completar una etapa | +1 burbuja comodín para la siguiente |
| Reventar 3+ burbujas | 10 pts × multiplicador de racha |
| Burbujas flotantes que caen | 5 pts × multiplicador de racha |
| Racha x2 (3 combos seguidos) | Puntos dobles |
| Racha x3 (5 combos seguidos) | Puntos triples |

## Burbujas especiales

- **Comodín** (arcoíris): se convierte en el color más común entre sus vecinas al posarse. Úsalo con `W` (teclado) o tocando el botón `W` junto al lanzador.
- **Piedra** (gris): no se puede reventar por color — solo cae si queda flotante sin soporte.

## Abrir el juego

Abre `index.html` directamente en el navegador — no requiere servidor ni instalación.

## Tecnologías

- HTML5 Canvas
- JavaScript vanilla
- CSS fullscreen con escala adaptativa (soporta HiDPI/Retina y móvil)
