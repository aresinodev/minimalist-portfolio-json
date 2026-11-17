# Rediseño visual del portfolio (cartel)

Rama `feat/redesign-modern-ui` (desde `develop`). Dirección elegida: `design/portfolio-redesign/06-brutalist-poster.html`.

## Specs

- **S1** «Quiero actualizar el diseño a algo más moderno, minimalista pero a la vez que llame la atencion.»
- **S2** «Antes de hacer una rama nueva, crear una rama develop y a partir de ahí empezamos a hacer nuevas ramas para todos los futuros cambios de la web.»
- **S3** «hay una foto personal mia, estaria bien que la implementaras dentro del diseño, donde tú creas que quedaria mejor»
- **S4** «me gustaba el diseño anterior. solamente te pedía unos cambios minimos para que no fuera tan estandar de IA.»
- **S5** «la foto creo que quedaria mejor en la parte izquierda, no entre medias.»
- **S6** «el color verde, fuera color naranja» · «me quedo con el naranja pero aplica el cambio que dices» (azul marino como secundario).
- **S7** «cuando se hace hover en los links de este tipo, en vez de que ponga un recuadro de fonde naranja, que haga un efecto de encoger el texto» · «quitamos el subrayado. dejamos solamente que se haga más pequeñito el texto».
- **S8** «las cajas de este tipo, veo que algunas tienen espacio bajo el texto y otras están ajustadas. quiero que todas queden iguales. sin tanto espacio por abajo.»
- **S9** «el hover de estas tags lo quitamos. no quiero que se ponga el fondo de ningun color cuando se hace hover sobre ellos.»
- **S10** «La parte de formacion debe de ser una seccion más como la de proyectos, experiencia, etc.» · «dejemos solamente esa formacion, no añadimos ninguna mas.»
- **S11** «Eliminamos el numero de telefono»
- **S12** «Esto debería de estar a la izquierda encima de la foto, el titulo y lo otro» (etiqueta) → después «Eliminalo».
- **S13** «Deberia de estar la parte superior de la imagen alineado con la parte superior del titulo» · «quiero este alineado la parte superior de la foto, no la sombra».
- **S14** «Esto lo pondría debajo de la foto» (ubicación) · «Aquí pondría el sobre mí de abajo» · «Ponlo debajo de la foto y el titulo mejor» · «Que ocupe todo el ancho del recuadro que lo contiene».
- **S15** «Coge la foto y el titulo, y centralo. Al menos en desktop.»
- **S16** «El 12+ lo veo redundante ya que aparece en el recuadro de la derecha»
- **S17** «Esto lo vamos a quitar, no lo veo necesario» (insignia de cifras del hero).

## Tasks

- [x] T1 Tokens, tipografía y Layout (S1, S4, S6) — commit
- [x] T2 Barra superior con navegación (S1) — commit
- [x] T3 Hero: retrato local, titular, resumen a todo el ancho, ubicación (S3, S5, S12-S16) — commit
- [x] T4 Experiencia con filas compartidas (S1, S8) — commit
- [x] T5 Proyectos con hover de encogido (S7) — commit
- [x] T6 Habilidades sin hover (S8, S9) — commit
- [x] T7 Formación como sección única (S10) — commit
- [x] T8 Contacto y pie con Cmd+K (S11) — commit
- [x] T9 Limpieza y build en verde (S1) — commit
- [x] T10 Contacto, pie con Cmd+K (S11) — commit

## Log

- L1 «este es el proyecto de mi portfolio, mi pagina personal. Quiero actualizar el diseño a algo más moderno, minimalista pero a la vez que llame la atencion. También me gustaria actualizar a la ultima version estable la teconología con la que está desarrollada. Si ves algun stack que utilizar mejor que el actual, me lo dices. Itera conmigo si es necesario para actualizar el diseño. También todo esto desarrollarlo en una nueva rama. Antes de hacer una rama nueva, crear una rama develop y a partir de ahí empezamos a hacer nuevas ramas para todos los futuros cambios de la web.»
- L2 Dirección elegida: cartel con crema, tinta, naranja `#ff6a00` y azul marino `#1e2a78`, tras tres tandas de artboards (01-11).
- L3 El alcance de este documento es el rediseño visual. La actualización de Astro 4.3 → 7 y Node 20 → 24 sigue fuera del documento, como unidad aparte.
- L4 La foto pasó de `imgur` a asset local (`src/assets/retrato.jpg`), 440×440, en blanco y negro vía CSS.
- L5 (histórico, superado por L7) Las dos formaciones nuevas de S10 no se pueden añadir sin datos: `cv.json` tiene una sola entrada en `education` y cero certificados. No se inventan.
- L6 Corte de commits: `e17d15d` (T1-T7, 1203 líneas cambiadas: sistema visual, hero y secciones) y el commit siguiente (T8-T10: contacto, pie y limpieza). El rediseño reescribe casi toda la página, así que el primer slice excede el objetivo de ~400 líneas; se deja registrado el límite entre slices para la revisión.
- L7 «dejemos solamente esa formacion, no añadimos ninguna mas.» — se retira la parte de S10 que pedía añadir dos formaciones. La sección queda con la única entrada real de `cv.json`; no se toca código porque la implementación ya estaba así.
- L8 Revisión nativa `review-ca2085f1a0943cdb` (lentes readability y reliability): 1 hallazgo crítico R3-001 y 6 no bloqueantes. R3-001 corregido en `2e8e8e0`; el validador dirigido lo rechazó y la autoridad quedó escalada/terminal (`native_stop_required`), sin continuación ofrecida. Los cuatro no bloqueantes con regresión real (R2-002, R3-002, R3-003, R3-004) se corrigieron por separado. R2-003 (etiqueta y nota de Experiencia hardcodeadas) queda como deuda conocida.
