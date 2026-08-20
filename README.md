# 🔴 Pokédex
Buscador de Pokémon con datos en tiempo real y diseño inspirado en un dispositivo Pokédex, construido con **HTML, CSS y JavaScript puro (Vanilla JS)** — consume la [PokéAPI](https://pokeapi.co/) para mostrar información completa de cualquier Pokémon, con enfoque en datos útiles para jugadores competitivos: tipos, debilidades y movimientos. Incluye un modo de comparación para ver dos Pokémon lado a lado.

## 🚀 Demo en vivo
👉 [Ver la Pokédex funcionando](https://MaxVF97.github.io/Pokedex/)

## ✨ Funcionalidades
- 🔍 Búsqueda por nombre o número, con Enter o botón
- 🎲 Botón de Pokémon aleatorio
- ⚔️ **Modo comparación**: busca dos Pokémon y muestra sus tarjetas lado a lado, con:
  - Reproducción secuencial de sus gritos (con diferencia de 2 segundos entre uno y otro)
  - Sincronización automática de las animaciones si ambos son legendarios
  - Alturas de cada sección igualadas entre ambas tarjetas para una comparación visual prolija
- ⚔️ **Modo comparación mejorado**: al re-comparar con una tarjeta ya en
  pantalla, elige cuál conservar con clic + confirmación; botón dinámico
  que cambia a "Cancelar" para salir del modo comparación en cualquier
  momento
- 📊 Estadísticas base (HP, Ataque, Defensa, Ataque/Defensa Especial,
  Velocidad) con barras de progreso, con efecto de brillo pulsante en
  Pokémon legendarios
- 🎨 Fondo temático por tipo en cada sección de la tarjeta, generado con
  los íconos de tipo de la propia API

- 🔊 Grito del Pokémon reproducido automáticamente, con botón para repetirlo
- 🏷️ Tipo(s) del Pokémon, con ícono e identificación en español
- ⚔️ Debilidades por tipo, calculadas consultando la API en tiempo real, con íconos
- 📈 Lista de movimientos que aprende subiendo de nivel, ordenados, con scroll propio
- 💎 Piedra evolutiva (si aplica), con su ícono correspondiente, en cualquier etapa de la cadena evolutiva
- ⭐ Aviso especial si el Pokémon es legendario, con efectos visuales animados (marco, texto y estrellas)
- ⬅️➡️ Navegación anterior/siguiente dentro de la Pokédex (en modo búsqueda individual)
- 🔄 Botón de reinicio para limpiar la búsqueda y el estado de comparación en un solo clic
- 🎨 Color de la tarjeta y de los botones cambia dinámicamente según el tipo principal del Pokémon
- 💡 Estados visuales del dispositivo: LEDs y ventanas emergentes distintas para "buscando", "no encontrado" y "reinicio"
- 📱 Diseño responsivo: se adapta a computadora, tablet y celular
- 🚫 Manejo de errores si el nombre no existe o el campo está vacío, con mensajes diferenciados
- 🔤 Nombre siempre capitalizado, sin importar cómo se escriba

## 🛠️ Tecnologías
Construido con **HTML, CSS y JavaScript puro**, sin frameworks ni librerías. Consume dos APIs públicas: la [PokéAPI](https://pokeapi.co/) para datos de Pokémon, tipos, especies e ítems, y el repositorio open-source [PokeAPI/sprites](https://github.com/PokeAPI/sprites) para íconos de tipo, ítems y sprites animados.

## 📚 Lo que practiqué en este proyecto
- Peticiones a APIs externas con `fetch`, `async`/`await` y manejo de promesas
- Encadenamiento de múltiples peticiones dependientes entre sí
- `for...of` para recorrer arrays de forma asíncrona (a diferencia de `.forEach()`)
- Recursión, para recorrer la cadena evolutiva de cada Pokémon
- Métodos de array: `.filter()`, `.map()`, `.sort()`, `.some()`, `.find()`, `.forEach()`
- Manejo de errores con `try`/`catch`
- Manipulación de strings: `.charAt()`, `.slice()`, `.split()`, template literals
- Refactor de lógica duplicada en funciones reutilizables y componibles (separar la obtención de datos de la generación de HTML)
- Parámetros opcionales y operador ternario para generar variantes de una misma plantilla HTML
- Manejo de estado con variables globales, incluyendo una máquina de estados simple para el modo comparación
- `data-*` attributes y `event.target` para delegación de eventos en contenido dinámico con múltiples instancias
- `setTimeout` para secuenciar acciones en el tiempo (reproducción de sonidos en orden)
- Medición y ajuste del DOM en tiempo de ejecución (`offsetHeight`) para igualar alturas entre elementos generados dinámicamente
- Manejo de errores de carga de imágenes con el evento `onerror`
- CSS Grid y Flexbox para layouts responsivos de varias columnas
- Variables CSS (custom properties) actualizadas dinámicamente desde JavaScript
- Animaciones con `@keyframes`, incluyendo animaciones sincronizadas entre múltiples elementos

## 📸 Vista previa

**Búsqueda individual**
![Búsqueda individual](preview-individual.jpeg)

**Modo comparación**
![Modo comparación](preview-comparacion.jpeg)

**Pokémon legendario**
![Efecto legendario](preview-legendario.jpeg)

**Modo comparación LEGENDARIO!**
![Modo comparación LEGENDARIO](preview-comparacion-legendario.jpeg)

---
Proyecto hecho como parte de mi aprendizaje de desarrollo web front-end.
