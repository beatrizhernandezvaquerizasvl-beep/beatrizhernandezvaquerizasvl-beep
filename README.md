Actúa como un desarrollador frontend senior especializado en creatividades interactivas, Three.js / Canvas y física 2D/3D.

Crea un componente web interactivo con efecto "anti-gravedad" (elementos flotantes con física suave e ingravidez al interactuar) listo para incrustar en la sección hero de una página web moderna.

### 1. Dirección de Arte y Estética (Vintage Desaturado / Muted Retro)
- **Atmósfera:** Editorial retro/vintage, inspirada en impresiones analógicas, portadas de libros de los años 60-70 y estética papel prensa/riso.
- **Paleta de color (baja saturación y cálida):**
  - Fondo: Crema/marfil envejecido suave (`#F4EFEA` o `#EAE5DB`).
  - Textura opcional: Grano sutil (noise overlay) o leve trama tipo semitono/papel.
  - Colores de acento (desaturados y con carácter):
    - Terracota/Ladrillo apagado (`#C96A5B`)
    - Verde salvia/oliva suave (`#7A8B7B`)
    - Mostaza/Ocre desaturado (`#CFA85E`)
    - Azul pizarra/acero vintage (`#5E7382`)
    - Tinta oscura para texto y bordes (`#2B2A27`, nunca negro puro `#000000`).
- **Tipografía sugerida:** Fuentes serif clásicas o slab-serif estilo editorial (ej. Playfair Display, Fraunces o Newsreader) combinadas con sans-serif monoespaciada para pequeños detalles (ej. Space Mono).

### 2. Objetos y Elementos Flotantes (Anti-gravedad)
- Genera entre 6 y 10 elementos que floten de manera orgánica en el lienzo:
  - Mezcla de formas geométricas abstractas (píldoras, esferas retro, tarjetas redondeadas, estrellas de 4 puntas retro) o pequeños bloques tipo insignias ("badges" con texto breve como "EST. 2026", "ANALYTICS", "DATA", "STRATEGY").
  - Estilo visual de los objetos: Bordes limpios, sombras suaves difusas (estilo papel superpuesto) o bordes de trazo fino tipo ilustración impresa.

### 3. Comportamiento Físico e Interacción
- **Efecto de ingravidez:** Movimiento continuo, lento y oscilante (flotación senoidal o física tipo Matter.js / Canvas API).
- **Interacción con el cursor:**
  - Repulsión suave cuando el ratón se acerca (efecto de empuje hidrodinámico o magnetismo inverso).
  - Posibilidad de arrastrar y soltar (drag & drop) los elementos con inercia y amortiguación (*damping*).
- **Comportamiento en bordes:** Rebote suave contra los límites del contenedor sin salir de pantalla.

### 4. Requisitos Técnicos de Entrega
- Código limpio, autónomo y responsivo (adaptable a móvil y escritorio).
- Puede estar construido en **HTML/CSS + JavaScript vanilla (HTML5 Canvas / RequestAnimationFrame)** o usando una librería ligera como **Matter.js** o **Three.js** vía CDN.
- Mantén el rendimiento a 60 FPS con animaciones fluidas y sin dependencias pesadas.
- Incluye comentarios claros en las variables de color y física para poder calibrar la gravedad y la velocidad fácilmente.
