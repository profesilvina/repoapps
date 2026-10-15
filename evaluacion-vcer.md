# Evaluación VCER: Repositorio de Aplicaciones Educativas (Vibe Coding & DUA)

Rúbrica VCER: Recomendable (85 %)  
Versión evaluada: Repositorio curado «repoapp» (32 aplicaciones educativas consolidadas en sus versiones finales y V2 optimizadas por docente, índice depurado y assets SVG/locales integrados), 14 de octubre de 2026.

Recomendable: cumple lo esencial de la guía y puede utilizarse o publicarse; las mejoras propuestas lo completan.

---

## 1. Inventario Exhaustivo del Repositorio

- **Recogida y tratamiento de datos personales:**
  - El repositorio y sus 32 aplicaciones consolidadas funcionan al 100% en el entorno local del navegador del usuario.
  - No se solicitan datos personales para navegar ni interactuar con las herramientas.
  - En las aplicaciones con funciones de reporte o práctica (como *EduLaboral*, *Álgebra* o *Escape Room 1952*), el ingreso de datos es opcional y se procesa únicamente en la memoria volátil de JavaScript (`state`) o en el almacenamiento local (`localStorage`) del dispositivo del usuario.
  - **Analítica de terceros:** Cero rastreadores. Se auditó y eliminó cualquier script residual de hosting ajeno. No contiene Google Analytics, Microsoft Clarity, Meta Pixel ni telemetría externa.
  - **Comunicaciones salientes:** Cero llamadas `fetch()` o `XMLHttpRequest` hacia servidores externos con información del alumnado.

- **Direcciones externas y dependencias de código:**
  - `https://cdn.tailwindcss.com` y `https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4`: Maquetación CSS responsiva accesible.
  - `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/` y `6.5.1`: Iconografía vectorial accesible.
  - `https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.js`: Renderizador matemático accesible en LaTeX.
  - `https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/`: Refuerzo visual positivo en secuencias lúdicas.
  - *Comportamiento sin internet:* Si se abre descargado sin conexión, las aplicaciones continúan funcionando; las tipografías son reemplazadas por las estándar del sistema operativo y los iconos o fórmulas se visualizan como texto plano estructurado. Las aplicaciones de ciencias y lógica (*Sistema Solar* y *Escape Room 1952*) sintetizan audio mediante Web Audio API nativa sin requerir archivos de sonido externos.

- **Fuentes tipográficas externas (Google Fonts):**
  - *Atkinson Hyperlegible* (baja visión y legibilidad inclusiva).
  - *Lexend* (diseñada para personas con dislexia).
  - *Fredoka* y *Comic Neue* (primeras infancias y nivel inicial).
  - *Outfit*, *Space Grotesk*, *Inter*, *Nunito*, *Courier Prime*.

- **Imágenes y recursos multimedia:**
  - Las imágenes fotográficas utilizadas en las aplicaciones de detectives visuales se encuentran integradas localmente en `appf2/img/`, sin dependencia de servidores externos.
  - La totalidad de las nuevas aplicaciones incorporadas (*Escape Room 1952*, *Exploradores del Sistema Solar*, *Análisis de Medios*) cuenta con más de 150 ilustraciones vectoriales SVG limpias o Canvas HTML5 nativos incrustados directamente en el código.
  - Los efectos sonoros y la lectura asistida en voz alta utilizan la **Web Audio API** y la **Web Speech API (`speechSynthesis`)** nativas del navegador, sin dependencias externas.

---

## 2. Puntuación y Justificación de los 10 Puntos VCER

### 1. CONTENIDO (eliminatorio) — Puntuación: 2 / 2
No se detectan errores conceptuales en lo que enseña el catálogo ni en las aplicaciones: las definiciones científicas de astronomía para 6.° grado (Sistema Solar y satélites según la UAI), el marco platónico de la Alegoría de la Caverna y falacias no formales de Filosofía (*Escape Room 1952*), el análisis crítico de la publicidad gráfica y género, las matemáticas (Ruffini, ecuaciones, fracciones) y las reglas de inglés son didácticamente rigurosas y las respuestas correctas son válidas.

### 2. DATOS PERSONALES (eliminatorio) — Puntuación: 2 / 2
No pide datos que identifiquen a nadie de forma obligatoria; los datos de práctica se guardan únicamente en el dispositivo o en memoria volátil con opción de uso anónimo, no se envían datos a ningún servidor y el repositorio está completamente libre de analítica y rastreadores de terceros.

### 3. ENTENDER QUÉ HACE — Puntuación: 2 / 2
El repositorio es un catálogo web abierto e interactivo con buscador en tiempo real y filtros por materia y nivel educativo, que compila y ejecuta 32 aplicaciones pedagógicas consolidadas (HTML/CSS/JS) creadas con Vibe Coding y enfoque DUA, presentando únicamente la versión más evolucionada de cada docente con botón de lanzamiento directo; ninguna aplicación guarda datos en servidores ni realiza comunicaciones ocultas, coincidiendo plenamente lo que declara el catálogo con lo que ejecuta el código.

### 4. DEPENDENCIAS — Puntuación: 2 / 2
Lo que carga de fuera procede de servicios conocidos y estables (Google Fonts, cdnjs, jsDelivr), está documentado en la Nota de Decisiones Arquitectónicas (`DECISIONES.md`), y todas las ilustraciones didácticas, esquemas vectoriales SVG y datos propios están almacenados dentro del material local.

### 5. ACCESIBILIDAD — Puntuación: 1 / 2
Se evaluó mediante inspección técnica de código DOM y recorrido con teclado; el portal central y las aplicaciones incorporan apoyos DUA sobresalientes (conmutador de alto contraste, escalado tipográfico A-/A+, tipografías para dislexia, barras de sintetizador de voz Text-to-Speech nativo y conmutadores de audio accesible), aunque en un grupo menor de maquetas iniciales faltan atributos `aria-label` en botones interactivos de iconos y directivas `prefers-reduced-motion` en animaciones continuas de canvas.

### 6. MATERIAL AJENO — Puntuación: 2 / 2
Cada biblioteca y elemento ajeno utilizado cuenta con una licencia de código abierto compatible (MIT, ISC, SIL OFL, Apache 2.0, CC BY 4.0), las imágenes cuentan con resolución local y los créditos de procedencia y licencias están formalizados en la documentación del repositorio.

### 7. RASTRO — Puntuación: 2 / 2
Existe una Nota de Decisiones de Diseño y Arquitectura formal (`DECISIONES.md`) que describe la estructura curada del catálogo, el contexto pedagógico, el criterio de selección de las versiones V2 consolidadas, las alternativas técnicas descartadas y los motivos de las decisiones adoptadas en materia de privacidad, DUA y Jamstack.

### 8. USO DE IA — Puntuación: 2 / 2
El repositorio declara en `README.md` y en el pie de `index.html` que fue desarrollado mediante la metodología Vibe Coding con asistencia de Antigravity CLI y Google Gemini, especificando explícitamente que la docente coordinadora revisó y validó la corrección didáctica de los contenidos curriculares, la ausencia de rastreo de datos, la extracción limpia del código y la funcionalidad accesible de los apoyos DUA.

### 9. LICENCIA — Puntuación: 2 / 2
El repositorio incluye en su raíz los archivos independientes `LICENSE` (GNU AGPL v3 para el código fuente) y `LICENSE-CONTENT` (Creative Commons CC BY-SA 4.0 para los contenidos didácticos), enlaces visibles en el pie de página del portal y el identificador estándar `SPDX-License-Identifier: AGPL-3.0-or-later` en la cabecera del código.

### 10. REUTILIZACIÓN — Puntuación: 1 / 2
El código es completamente accesible, abierto, sin comprimir ni ofuscar, e incluye una guía paso a paso para publicarlo en GitHub Pages; la modularidad de las aplicaciones agregadas (*casesData*, *roomObjects*, módulos planetarios) facilita su edición, si bien varias maquetas se beneficiarían de una mayor cantidad de comentarios explicativos internos para guiar a otros docentes en su adaptación en el aula.

---

## 3. Resultado Oficial

$$\text{Puntuación total: } 17 / 20 \text{ puntos} = 85\,\%$$

**Veredicto Oficial:** **Recomendable (85 %)**

- **Significado del veredicto:** Cumple lo esencial de la guía de Vibe Coding Responsable y puede utilizarse o publicarse en abierto con total seguridad pedagógica y técnica; las mejoras propuestas consolidan su accesibilidad y adaptabilidad docente.

---

## 4. Próximas Mejoras Opcionales para Alcanzar el 95-100%

1. **Atributos de accesibilidad en apps secundarias (+1 punto en Criterio 5):**  
   Agregar atributos `aria-label` descriptivos a los botones de solo icono en las aplicaciones de nivel inicial e incorporar la directiva `@media (prefers-reduced-motion: reduce)` en los fondos animados por canvas.
2. **Comentarios didácticos de adaptación (+1 punto en Criterio 10):**  
   Añadir en cada archivo HTML una sección comentada al inicio con instrucciones para que otro colega docente pueda cambiar las preguntas, textos o imágenes sin necesidad de conocimientos avanzados de programación.
