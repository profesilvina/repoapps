# Nota de Decisiones de Diseño y Arquitectura (ADR)
> **Proyecto:** Repositorio de Aplicaciones Educativas (Vibe Coding & DUA)  
> **Fecha de redacción:** Octubre de 2026 *(Redactada con posterioridad a la creación inicial para documentar formalmente las decisiones técnicas y pedagógicas adoptadas)*.  
> **Coordinación:** Prof. Silvina Elena Busto  
> **Asistencia de IA:** Antigravity CLI & Google Gemini  

---

## 1. Contexto y Propósito Pedagógico
El repositorio tiene como propósito compilar, visibilizar y poner a disposición de la comunidad educativa una colección de 33 mediadores didácticos e interactivos creados por docentes mediante la metodología *Vibe Coding* (programación guiada por lenguaje natural e IA). Las aplicaciones cubren diversas áreas curriculares (Matemática, Lengua, Ciencias Naturales, Química, Artes, Música, Idiomas, Filosofía y Ciudadanía Digital) en los niveles Inicial, Primario, Secundario y Formación Docente, articuladas con los principios del Diseño Universal para el Aprendizaje (DUA).

---

## 2. Decisiones Arquitectónicas y Técnicas

### Decisión 1: Arquitectura 100% Cliente Estático (Jamstack / Client-Side Puro)
- **Contexto:** Se requería una solución tecnológica que cualquier docente o escuela de la Ciudad pudiera abrir, clonar y ejecutar sin necesidad de instalar servidores, configurar Node.js ni contratar bases de datos.
- **Decisión adoptada:** Cada aplicación se concibe como un archivo web autónomo (HTML5 + CSS + JavaScript vanilla) o conjunto estático que corre directamente en el navegador del usuario.
- **Alternativas descartadas:** Aplicaciones basadas en frameworks pesados con backend (Node/Express, bases de datos SQL o Firebase) que exigen mantenimiento y generan costos de suscripción y dependencias de red.
- **Consecuencias:** Máxima portabilidad, costo marginal cero y compatibilidad total con hosting gratuito estático como GitHub Pages.

---

### Decisión 2: Dependencias Externas y Comportamiento Offline
- **Contexto:** Se necesitaba una estética moderna y herramientas de accesibilidad sin reinventar componentes básicos.
- **Bibliotecas seleccionadas:**
  - **Tailwind CSS & FontAwesome Free (CDN):** Para maquetación responsiva rápida e iconografía visual intuitiva.
  - **KaTeX (CDN):** Para renderizado tipográfico accesible y de alto rendimiento de fórmulas matemáticas en LaTeX.
  - **Google Fonts (CDN):** Tipografías inclusivas como *Atkinson Hyperlegible* (baja visión), *Lexend* (dislexia) y *Fredoka* (primeras infancias).
- **Comportamiento sin conexión (Offline):**
  - Si un usuario abre las aplicaciones sin conexión a Internet, el contenido y la lógica didáctica continúan funcionando al 100%. Las fuentes tipográficas son sustituidas de forma automática por las fuentes seguras del sistema operativo (Arial, system-ui), y los iconos o fórmulas matemáticas se presentan como texto legible.

---

### Decisión 3: Privacidad Estricta de Datos y Ausencia de Analítica
- **Contexto:** Siguiendo las directrices éticas y legales de protección de datos de niñas, niños y adolescentes en el ámbito escolar (Resolución y marco normativo GCABA / guía VCER).
- **Decisión adoptada:**
  - No se solicita información personal identificable para usar las aplicaciones.
  - En las aplicaciones con simulador de currículum o prácticas (como EduLaboral o Álgebra), los campos de nombre son opcionales y los datos se procesan exclusivamente en la memoria volátil o en el almacenamiento local (`localStorage`) del dispositivo del usuario.
  - Ningún dato es transmitido a servidores remotos ni registrado en bases de datos.
  - Se prohíbe el uso de scripts de analítica de terceros (Google Analytics, Clarity, Meta Pixel, Plausible o redes publicitarias). Se auditó y removió cualquier script residual de hosting gratuito previo.

---

### Decisión 4: Accesibilidad e Inclusión (Enfoque DUA)
- **Contexto:** Garantizar que las herramientas atiendan a la diversidad del aula según la Resolución 860/25 y las pautas WCAG 2.1.
- **Decisión adoptada:**
  - El portal central incorpora barra de herramientas DUA con conmutador de **Alto Contraste** y selector dinámico de tamaño de fuente tipográfica.
  - Las aplicaciones integran soporte para **Web Speech API (`speechSynthesis`)**, permitiendo lectura en voz alta nativa sin costo ni conexión a APIs de pago.
  - Se priorizó el uso de gráficos vectoriales SVG limpios y paletas contrastadas para no depender únicamente del color para transmitir información.

---

### Decisión 5: Esquema Dual de Licenciamiento Abierto (FLOSS / REA)
- **Contexto:** Asegurar la reutilización y soberanía pedagógica de los materiales creados.
- **Decisión adoptada:**
  - **Código fuente:** Licenciado bajo **GNU AGPL v3**, obligando a que cualquier adaptación tecnológica distribuida en red conserve su carácter libre y abierto.
  - **Contenidos educativos:** Licenciados bajo **Creative Commons CC BY-SA 4.0**, permitiendo a otros docentes adaptar y traducir las secuencias didácticas reconociendo la autoría original.
