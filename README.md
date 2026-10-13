# Taller Práctico DIW (RA2) — Proyecto Refactorizado

> **Módulo:** Diseño de Interfaces Web (DIW)  
> **Unidad:** UD02 — Uso de Estilos  
> **Resultado de Aprendizaje:** RA2 — Crear interfaces Web homogéneas definiendo y aplicando estilos.  
> **Curso Académico:** 2026–2027  

---

## 1. Descripción del Proyecto

Este proyecto consiste en la **refactorización integral** de un sitio web tipo *portfolio* de 3 páginas (`index.html`, `sobre.html` y `contacto.html`). Se ha transformado un código heredado ineficiente (con estilos en línea y bloque `<style>` interno) en una **arquitectura modular escalable y mantenible basada en SASS/SCSS**.

### Objetivos alcanzados:
1. **Limpieza y Semántica HTML5:** Eliminación total de atributos `style="..."` e incrustaciones internas, garantizando el principio DRY (*Don't Repeat Yourself*).
2. **Arquitectura SASS Modular:** Separación de responsabilidades en parciales (`_*.scss`) unificados mediante `@use`.
3. **Identidad Visual y Tipografía:** Definición de una paleta de colores centralizada y tipografías externas desde Google Fonts (*Montserrat* para títulos y *Roboto* para cuerpo).
4. **Compleción del Sitio:** Maquetación e integración semántica de la nueva página `contacto.html` con un formulario estructurado e interactivo.
5. **Compilación y Estándares:** Compilación automática con *Live Sass Compiler* y validación mediante las herramientas del W3C.

---

## 2. Estructura de Directorios

```text
proyecto-refactorizado/
├── index.html              # Página principal (Inicio)
├── sobre.html              # Página de información (Sobre mí)
├── contacto.html           # Página de contacto con formulario
├── README.md               # Documentación del proyecto
├── css/
│   ├── main.css            # CSS compilado final para producción
│   └── main.css.map        # Mapa de fuente para depuración
└── scss/
    ├── _variables.scss     # Paleta de colores, fuentes y constantes
    ├── _reseteo.scss       # Box Model universal y estilos base
    ├── _header.scss        # Cabecera principal y barra de navegación
    ├── _contenido.scss     # Estilos de tarjetas, contenedores y listados
    ├── _formulario.scss    # Campos de entrada y formulario de contacto
    ├── _botones.scss       # Mixins y clases de botones reutilizables
    ├── _footer.scss        # Pie de página unificado
    └── main.scss           # Archivo principal de ensamblaje SASS
## 3. Arquitectura SASS y Diseño

El proyecto aprovecha las capacidades avanzadas del preprocesador SASS:

* **Variables Centralizadas (`_variables.scss`):**
  * Color primario corporativo: `#004a99`
  * Color secundario (efectos/foco): `#00aaff`
  * Superficies y fondos: `#f4f4f4` y `#ffffff`
  * Fuentes web: `Montserrat` y `Roboto`
* **Anidamiento (*Nesting*):** Reducción de duplicación de selectores en elementos jerárquicos (`nav ul li a`).
* **Mixins Reutilizables (`_botones.scss`):** Abstracción de patrones comunes para botones y estados `:hover` y `:focus`.
* **Reseteo del Modelo de Caja (`_reseteo.scss`):** Aplicación de `box-sizing: border-box;` en todo el documento.

---

## 4. Instrucciones de Ejecución y Desarrollo

### Requisitos previos:
* Visual Studio Code
* Extensión **Live Sass Compiler** (por Glenn Marks)

### Pasos para compilar:
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/TU-USUARIO/proyecto-refactorizado.git
## 5. Validación y Calidad del Código

* **HTML5:** Estructura validada mediante el [W3C Markup Validation Service](https://validator.w3.org/).

![PruebaHTML5](/img/pruebaHTML5.png)


* **CSS3:** Hoja de estilos `css/main.css` verificada sin errores en el [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/).

![PruebaCSS](/img/pruebaCSS.png)

---

## Autor
* **Estudiante:** [Manuel Parrilla Lahoz]
* **Curso:** 2º DAW — Diseño de Interfaces Web