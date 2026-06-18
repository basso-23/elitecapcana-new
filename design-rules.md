# Reglas generales de diseño y CSS

## Principio central

Cada proyecto debe sentirse claro, consistente y diseñado con intención. No debe parecer una plantilla genérica ni una suma de decisiones aisladas.

Estas reglas son obligatorias para mantener orden visual y técnico entre proyectos. Si una excepción es necesaria, debe responder a una razón concreta del layout o del producto.

## Composición visual

- Mantener jerarquía visual clara: título, subtítulo, contenido principal y acciones.
- Usar espacios de forma consistente; no llenar cada área disponible con contenido.
- Alternar secciones densas con secciones más respiradas cuando el flujo lo necesite.
- Usar imágenes, iconos y recursos visuales solo cuando ayuden a entender o reforzar el contenido.
- Mantener cada sección o componente con un objetivo claro.
- Evitar estilos decorativos que no aporten estructura, legibilidad o intención.

## Sistema CSS

- Usar CSS propio como sistema principal de estilos.
- No usar Tailwind.
- No usar CSS-in-JS, UI kits genéricos ni clases utilitarias como base visual.
- Colocar tokens, resets mínimos y patrones reutilizables al inicio del CSS.
- Es muy importante mantener orden y consistencia en el CSS y al construir cada sección; cada nueva sección debe seguir los tokens, patrones, naming y estructura definidos antes de crear estilos propios.
- Crear estilos específicos solo cuando un patrón común no alcance.
- Evitar duplicar reglas de tipografía, botones, iconos, contenedores y textos.

## Reglas tecnicas obligatorias para construir landings

- Para landings, aplicar todas las reglas generales de diseño y CSS de este documento.
- El implementador tiene libertad total para crear assets, imagenes, texturas, fondos, iconos, ilustraciones y recursos visuales si mejoran el resultado premium.
- El implementador puede buscar y usar tipografias de cualquier recurso valido, siempre que el resultado mejore la direccion visual y mantenga legibilidad.
- Se permiten animaciones, transiciones, microinteracciones, carruseles, sliders, galerias, tabs, acordeones, menus, formularios avanzados y otros elementos UI cuando ayuden al objetivo de conversion y se sientan intencionales, fluidos, responsivos y accesibles.
- Se permite buscar en internet cualquier documentacion, referencia o recurso necesario para lograr el mejor resultado posible.

## Reglas para imagenes conceptuales

- Usar siempre `imagegen` para generar las imagenes conceptuales.

## Tokens base

Los valores compartidos deben vivir en `:root`. Esta es la base mínima:

```css
:root {
	--site_max_width: 1280px;
	--font_display: "Cormorant Garamond", Georgia, serif;
	--font_body: "Manrope", Arial, sans-serif;
}
```

- Usar tokens para colores, fuentes, anchos máximos, espacios principales, radios y transiciones repetidas.
- Mantener los nombres de tokens descriptivos y en `snake_case`.
- No crear variables para valores que aparecen una sola vez.
- Usar `--site_max_width: 1280px;` como ancho máximo general de página.

## Grid vs Flexbox

- Usar `display: grid` para estructuras bidimensionales: layouts de página, secciones con columnas, galerías, cards en grilla y distribuciones con filas y columnas.
- Usar `display: flex` para estructuras lineales: navegación, botones, filas de icono + texto, grupos de acciones y listas simples.
- No usar Grid donde Flexbox resuelve una sola línea o una sola columna.
- No usar Flexbox para simular grillas complejas.
- Cada sección principal debe tener un contenedor interno centrado y limitado por `--site_max_width`.

## Breakpoint único

Trabajar siempre con un solo breakpoint:

```css
@media (max-width: 1024px) {
	/* Ajustes responsive */
}
```

- No crear breakpoints adicionales salvo instrucción explícita.
- En desktop se define la composición principal.
- En `1024px` se resuelve tablet y mobile usando layouts fluidos, `clamp()`, `min()`, `max()`, Grid y Flexbox.
- Evitar reglas responsive dispersas fuera de este breakpoint.

## Nombramiento de clases

- Todas las clases CSS deben usar `snake_case`.
- Los nombres deben describir función, bloque o patrón; no colores temporales ni posiciones accidentales.
- Usar nombres consistentes por patrón:
  - `section_inner` para contenedores centrados.
  - `section_header` para encabezados de sección.
  - `section_copy` para bloques de texto.
  - `section_title` para titulares de sección.
  - `section_text` para textos introductorios.
  - `feature_row` para filas de icono + texto.
  - `line_icon` para iconos SVG de línea.
  - `button_base` para comportamiento común de botones y enlaces tipo botón.

## Patrones reutilizables

Primero buscar si existe un patrón aplicable antes de crear una clase nueva. Combinar clase común + clase específica cuando haga falta una variación:

```html
<section class="example_section">
	<div class="example_inner section_inner">
		<header class="example_header section_header">
			<h2 class="section_title">Título de sección</h2>
			<p class="section_text">Texto introductorio claro y breve.</p>
		</header>
	</div>
</section>
```

- La clase común define el comportamiento repetido.
- La clase específica ajusta solo lo propio del bloque.
- No duplicar estilos base dentro de cada sección o componente.
- Si un patrón se repite tres veces, debe convertirse en regla compartida.

## Evitar

- Clases con nombres inconsistentes, abreviados o mezclando idiomas sin razón.
- Breakpoints múltiples para resolver casos puntuales.
- Componentes visuales con estilos únicos cuando pueden usar patrones comunes.
- Iconos genéricos sin propósito.
- Exceso de texto dentro de cards, botones, formularios o encabezados.
- Efectos, animaciones o decoraciones que perjudiquen legibilidad, rendimiento o accesibilidad.

## Regla final

La consistencia es parte del diseño. Antes de escribir CSS nuevo, revisar tokens, patrones existentes, naming y el breakpoint único. El resultado debe ser fácil de leer, fácil de mantener y suficientemente claro para que otra persona o una IA puedan continuar el proyecto sin reinterpretar el sistema.
