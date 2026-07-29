# 💻 Repositorio de Aplicaciones Educativas (Vibe Coding & DUA)

> **Autora:** Silvina Busto  
> **Enfoque Pedagógico:** Mediadores didácticos para el andamiaje cognitivo, "Socias del Pensamiento" (Perkins) y Diseño Universal para el Aprendizaje (DUA - Res. 860/25).

Este repositorio contiene una colección de aplicaciones web interactivas y mediadores didácticos desarrollados mediante la metodología **Vibe Coding** (desarrollo asistido por Inteligencia Artificial y lenguaje natural).

---

## 🚀 Aplicaciones Incluidas

1. **index.html**: Repositorio central e interfaz principal de navegación con buscador en tiempo real, filtros por nivel y materia, y accesibilidad DUA.
2. **app-ruffini-dua.htm**: Mediador didáctico interactivo para la Regla de Ruffini con impulsos socráticos, pistas graduadas y apoyos DUA (A+/A-, Alto Contraste y Síntesis de Voz Text-to-Speech).
3. **Ruffini.htm**: Calculadora y algoritmo interactivo paso a paso para la división de polinomios por la Regla de Ruffini.

---

## 🌐 Cómo Publicar este Repositorio Gratis en GitHub Pages

Para habilitar la web en línea y compartir los enlaces públicos con estudiantes o colegas:

1. Subir el proyecto a un repositorio nuevo en GitHub (ej. `repositorio-apps-educativas`).
2. En GitHub, ve a la pestaña **Settings** (Configuración) de tu repositorio.
3. En el menú lateral izquierdo, haz clic en **Pages**.
4. En la sección **Build and deployment** -> **Source**, selecciona **Deploy from a branch**.
5. En **Branch**, selecciona `main` (o `master`) y la carpeta `/ (root)`. Haz clic en **Save**.
6. En unos segundos, GitHub te proporcionará tu enlace público (ej. `https://tu-usuario.github.io/repositorio-apps-educativas/`).

---

## ✏️ Cómo Agregar Nuevas Aplicaciones al Repositorio

Abre el archivo `index.html` en un editor de texto y agrega un nuevo objeto al array `REPOSITORIO_APPS`:

```javascript
{
  id: "app-3",
  titulo: "Título de tu Nueva App",
  autor: "Silvina Busto",
  descripcion: "Descripción breve de la propuesta...",
  nivel: "Secundaria", // Primaria, Secundaria o Universidad
  materia: "Matemática",
  url: "nombre_de_tu_archivo.htm",
  tags: ["DUA", "Interactiva"]
}
```
