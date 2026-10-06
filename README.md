# 3 ejercicios Tailwind CSS

### Plantilla base

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Dojo Tailwind</title>
  <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>
<body>
  <!-- Tu código aquí -->
</body>
</html>
```

## Ejercicio 1: Tarjeta de producto

Maqueta una tarjeta de producto centrada en la pantalla, sobre un fondo verde claro.

### Requisitos

- [ ] La página ocupa al menos toda la pantalla, con fondo verde claro, y la tarjeta queda centrada en horizontal y en vertical.
- [ ] La tarjeta es blanca, de ancho máximo pequeño (pero que en móvil ocupe todo el ancho disponible), con esquinas redondeadas, sombra y padding generoso.
- [ ] Título en negrita y tamaño `xl`, descripción en gris, precio en verde, grande y en negrita.
- [ ] Botón azul que ocupa todo el ancho de la tarjeta, con texto blanco, esquinas redondeadas y un azul más oscuro al pasar el ratón.
- [ ] Separaciones verticales razonables entre elementos (usa márgenes).

### Una ayuda 

- Centrar algo en pantalla: piensa en `min-h-screen` y en dos clases de flexbox.
- Ancho que se adapta pero con tope: `w-full` más un `max-w-*`.
- Los márgenes entre elementos pueden ser `mt-*`.


## Ejercicio 2: Barra de navegación

Crea una barra de navegación oscura que se quede pegada arriba al hacer scroll.

### Requisitos

- [ ] La barra tiene fondo oscuro, texto blanco y padding horizontal y vertical.
- [ ] A la izquierda, el nombre de la web en negrita y tamaño `xl`. A la derecha, una lista de enlaces: *Inicio*, *Cursos*, *Contacto* y un botón-enlace *Registro*.
- [ ] Los enlaces están separados entre sí, alineados verticalmente y cambian a azul claro al pasar el ratón.
- [ ] *Registro* tiene fondo azul, esquinas redondeadas y un azul más oscuro en `hover`.
- [ ] La barra se queda fija en la parte superior al hacer scroll.
- [ ] Debajo, un `<main>` con bastante texto (en VS Code: escribe `p*15>lorem` y pulsa Tab) para poder comprobar el scroll.

### Una ayuda

- Logo a un lado y enlaces al otro: `flex` con `justify-between`.
- Los `<li>` de una lista no se ponen en fila solos: la `<ul>` también necesita ser `flex`.
- Para que se quede pegada: investiga `sticky` y `top-0`. Si el contenido pasa por encima, necesitarás `z-10`.

## Ejercicio 3: Galería responsive

Crea una cuadrícula de 8 cajas de colores que se reorganice según el ancho de la pantalla.

### Requisitos

- [ ] 8 elementos, cada uno con un color de fondo distinto, un número grande en el centro (texto blanco, negrita) y altura fija.
- [ ] Todos con esquinas redondeadas y separación entre ellos.
- [ ] **1 columna** en móvil, **2 columnas** desde tablet (`md`), **4 columnas** desde portátil (`lg`).
- [ ] Desde tablet, el **primer elemento** ocupa 2 columnas.
- [ ] La página tiene un padding para que no se pegue a los bordes.

### Una ayuda

- El contenedor es un `grid`; las columnas por breakpoint se escriben igual que cualquier otra clase pero con prefijo.
- Para centrar el número dentro de cada caja puedes usar flex (`flex items-center justify-center`) o `grid place-items-center`.
- `col-span-*` solo se aplica desde `md:`, así que lleva prefijo.