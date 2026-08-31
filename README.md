# Matemáticas

Libro introductorio de matemáticas escrito en español. El proyecto presenta los conceptos de manera progresiva, rigurosa y accesible, con especial atención a la diferencia entre números y sus representaciones, la estructura de las expresiones, la motivación de las propiedades y la separación entre los conceptos matemáticos y los algoritmos de cálculo.

El contenido desarrollado actualmente abarca:

- sistemas de numeración y sistema decimal;
- números naturales, enteros y racionales;
- adición y sustracción;
- igualdades y ecuaciones;
- producto y sus propiedades;
- división, fracciones y escritura decimal;
- clasificación mediante las inclusiones `N ⊆ Z ⊆ Q`.

El capítulo sobre potencias está preparado en la estructura del proyecto, pero todavía no contiene desarrollo.

## Estructura

```text
.
├── main.tex                  # Documento principal
├── context.md                # Contexto metodológico y estado del proyecto
├── misc/
│   ├── envs.tex              # Entornos personalizados de LaTeX
│   └── boxes.tex             # Estilos visuales para tcolorbox
└── chapters/
    ├── 1_suma/               # Capítulo 1: Los números
    │   ├── main.tex
    │   ├── 1_sistemas_numeracion.tex
    │   ├── 2_suma.tex
    │   ├── 3_sustraccion.tex
    │   ├── 4_ecuaciones.tex
    │   ├── 5_sumas_multiples.tex
    │   ├── 6_ejercicios.tex
    │   └── resumen.tex
    ├── 2_producto/            # Capítulo 2: Producto
    │   ├── main.tex
    │   ├── 1_producto_natural.tex
    │   ├── 2_propiedades_prod.tex
    │   ├── 3_ejercicios.tex
    │   ├── 4_producto_entero.tex
    │   ├── 5_producto_racional.tex
    │   ├── 6_conjuntos.tex
    │   ├── 7_ejercicios.tex
    │   └── resumen.tex
    └── 3_potencia/            # Capítulo 3: Potencia
        └── main.tex
```

Las secciones internas se incorporan mediante `\input` y los capítulos completos mediante `\include` desde `main.tex`. Los archivos auxiliares de LaTeX y el PDF generado no forman parte de la fuente editable.

## Compilación

Se necesita una distribución de LaTeX con los paquetes utilizados por el proyecto y las fuentes Computer Modern Unicode (CMU). Como `main.tex` utiliza `fontspec`, debe compilarse con LuaLaTeX o XeLaTeX, no con pdfLaTeX.

Desde la raíz del proyecto, ejecute el compilador dos veces para actualizar correctamente el índice:

### LuaLaTeX

```bash
lualatex main.tex
lualatex main.tex
```

### XeLaTeX

```bash
xelatex main.tex
xelatex main.tex
```

El resultado será `main.pdf`. Durante la compilación se generan archivos auxiliares como `.aux`, `.log`, `.out` y `.toc`; están excluidos mediante `.gitignore`.

## Licencia

El contenido textual, matemático y gráfico original de este proyecto se distribuye bajo la licencia **Creative Commons Atribución-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)**.

Esto permite copiar, redistribuir, adaptar y crear material derivado, incluso con fines comerciales, siempre que se reconozca la autoría, se incluya un enlace a la licencia y las adaptaciones se distribuyan bajo la misma licencia.

Texto completo de la licencia: <https://creativecommons.org/licenses/by-sa/4.0/deed.es>

Autor: Elio Valentino Anci.
