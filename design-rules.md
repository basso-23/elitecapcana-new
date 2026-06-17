# Design Rules for Premium Real Estate Landing Pages

## Principio central

La landing debe sentirse premium, especifica para el proyecto y orientada a conversion. No debe parecer una plantilla generica.

## Que significa premium en este sistema

Premium no significa saturar con efectos. Premium significa:

- Composicion limpia.
- Jerarquia visual clara.
- Mucho control del espacio.
- Fotografia o renders protagonistas.
- Tipografia con caracter editorial.
- CTAs visibles pero elegantes.
- Microcopy confiable y concreto.
- Consistencia visual entre secciones.
- Sensacion de exclusividad, confianza y deseo.

## Reglas de composicion

- Usar grids claros y alineaciones consistentes.
- Evitar llenar cada espacio con contenido.
- Crear ritmo entre secciones densas y secciones respiradas.
- Alternar bloques visuales grandes con texto breve.
- Usar titulares fuertes y subtitulares concretos.
- Mantener cada seccion con un objetivo claro.

## Reglas de conversion

Cada landing debe responder rapidamente:

1. Que es el proyecto.
2. Donde esta ubicado.
3. Para quien es ideal.
4. Por que es deseable.
5. Que accion debe tomar el usuario.

## CTAs recomendados

- Solicitar informacion
- Agendar visita
- Descargar brochure
- Hablar por WhatsApp
- Ver disponibilidad
- Cotizar unidad

## Evitar

- Iconos genericos sin criterio.
- Exceso de texto en hero.
- Formularios demasiado largos.
- Secciones sin CTA o sin objetivo.
- Copiar referencias de forma literal.
- Usar imagenes genericas si existen assets reales del proyecto.
- Prometer caracteristicas no verificadas.

## Reglas para IA generativa visual

Cuando se pidan imagenes conceptuales:

- Usar siempre `imagegen` para generar la imagen conceptual.
- Guardar la imagen generada dentro del proyecto o carpeta del lote correspondiente.
- No pasar a especificacion tecnica ni implementacion sin esa imagen generada.
- Generar 3 secciones consecutivas por lote.
- Mantener una misma direccion visual en todo el lote.
- Incluir suficiente detalle para que el resultado pueda pasar a codigo.
- Evitar texto ilegible como dependencia critica.
- Usar placeholders realistas para renders, mapas, formularios y fotografias.
- Aceptar que la imagen pueda incluir detalles especificos inventados como fechas, telefonos, precios secundarios, textos legales o microcopy de maqueta, siempre que funcionen como guia visual y no como copy final.
- No bloquear el flujo por esos detalles de maqueta; deben corregirse despues en la especificacion tecnica y en la implementacion.
- Entregar siempre especificacion textual junto a la imagen.

## Reglas para pasar a codigo

## Reglas tecnicas obligatorias para construir landings

- Todas las landings deben construirse en Astro.
- Antes de crear un proyecto Astro nuevo, revisar la documentacion oficial de instalacion en https://docs.astro.build/en/getting-started/ y usar la version estable mas reciente disponible.
- Usar CSS propio como sistema principal de estilos. No depender de Tailwind, CSS-in-JS, UI kits genericos o clases utilitarias como base visual.
- Todas las clases CSS creadas para la landing deben usar formato snake_case.
- El implementador tiene libertad total para crear assets, imagenes, texturas, fondos, iconos, ilustraciones y recursos visuales si mejoran el resultado premium.
- El implementador puede buscar y usar tipografias de cualquier recurso valido, siempre que el resultado mejore la direccion visual y mantenga legibilidad.
- Se permiten animaciones, transiciones, microinteracciones, carruseles, sliders, galerias, tabs, acordeones, menus, formularios avanzados y otros elementos UI cuando ayuden al objetivo de conversion y a la sensacion premium.
- Se permite buscar en internet cualquier documentacion, referencia o recurso necesario para lograr el mejor resultado posible.
- Las animaciones y elementos UI deben sentirse intencionales, fluidos y responsivos; no deben distraer ni perjudicar performance, accesibilidad o conversion.

## Especificacion minima para implementacion

Cada lote visual debe convertirse en:

- Nombre de seccion.
- Objetivo de seccion.
- Copy sugerido.
- Jerarquia visual.
- Layout desktop.
- Layout mobile.
- Componentes necesarios.
- Interacciones.
- Notas de espaciado.
- Assets requeridos.
