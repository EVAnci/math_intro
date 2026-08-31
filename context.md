# Contexto del proyecto Matemáticas

## Propósito de este archivo

Este documento sirve como contexto de trabajo para revisar, ampliar y redactar el libro. Describe el estado real del proyecto, la estructura de los archivos y las decisiones metodológicas que deben conservarse. Antes de modificar un capítulo, úselo para mantener la continuidad conceptual y el estilo del texto.

El proyecto es un libro introductorio de matemáticas escrito en español. Busca desarrollar una comprensión conceptual de las operaciones y de los conjuntos numéricos sin convertir la exposición en un tratado fundacional. El rigor debe estar al servicio de la comprensión: cada definición, propiedad o procedimiento importante debe tener una motivación y no presentarse como una regla misteriosa.

---

## Estado actual del proyecto

El archivo principal incluye tres capítulos:

```latex
\include{chapters/1_suma/main}
\include{chapters/2_producto/main}
\include{chapters/3_potencia/main}
```

- El capítulo 1, `Los números`, está desarrollado. Presenta sistemas de numeración, naturales, adición, enteros, sustracción, ecuaciones, sumas de varios términos y ejercicios.
- El capítulo 2, `Producto`, está desarrollado hasta la división decimal y la clasificación de `N`, `Z` y `Q`. Incluye ejercicios iniciales y ejercicios integradores.
- El capítulo 3, `Potencia`, solo tiene el archivo `chapters/3_potencia/main.tex`, actualmente vacío. Es el siguiente capítulo por desarrollar.

Los archivos `main.pdf`, `main.aux`, `main.log`, `main.out` y `main.toc` son artefactos de compilación. El PDF y los auxiliares están ignorados por Git según `.gitignore`; no deben tratarse como fuente del libro.

---

## Mapa de archivos

### Configuración general

- `main.tex`: clase `book` en tamaño `a5paper`, idioma español, fuentes CMU, paquetes matemáticos y gráficos, inclusión de entornos y cajas, portada, índice y capítulos.
- `misc/envs.tex`: definición de entornos numerados y del entorno `note`.
- `misc/boxes.tex`: estilos visuales `resumen` y `remember` para `tcolorbox`.
- `.gitignore`: excluye auxiliares de LaTeX, artefactos del editor y `main.pdf`.

### Capítulo 1: `chapters/1_suma/`

El archivo `main.tex` define `\chapter{Los números}` y carga los siguientes archivos en este orden:

1. `1_sistemas_numeracion.tex`: idea de sistema de numeración y sistema decimal.
2. `2_suma.tex`: naturales, adición, operación y operandos, representaciones, práctica de sumas y algoritmo decimal de la adición.
3. `3_sustraccion.tex`: opuestos, enteros, usos del signo menos y sustracción como suma del opuesto.
4. `4_ecuaciones.tex`: igualdad, ecuación, conservación de la igualdad y resolución de ecuaciones aditivas.
5. `5_sumas_multiples.tex`: suma binaria aplicada varias veces, asociatividad, sumandos, términos y expresiones con sustracciones.
6. `6_ejercicios.tex`: ejercicios con enteros y ecuaciones.
7. `resumen.tex`: resumen en cajas `tcolorbox`.

### Capítulo 2: `chapters/2_producto/`

El archivo `main.tex` define `\chapter{Producto}` y carga:

1. `1_producto_natural.tex`: producto de naturales, suma repetida, factores, estructura de expresiones y precedencia.
2. `2_propiedades_prod.tex`: clausura, conmutatividad, elemento neutro, producto por cero, asociatividad y distributividad.
3. `3_ejercicios.tex`: práctica inicial con productos de naturales y reconocimiento de estructura.
4. `4_producto_entero.tex`: extensión a enteros y determinación conceptual de los signos mediante opuestos y distributividad.
5. `5_producto_racional.tex`: fracciones, racionales, fracciones equivalentes, producto racional, inverso, división, escritura decimal y algoritmo de la división.
6. `6_conjuntos.tex`: inclusiones `\mathbb N\subseteq\mathbb Z\subseteq\mathbb Q`.
7. `7_ejercicios.tex`: ejercicios integradores sobre enteros, racionales, productos, inversos, división, decimales, conjuntos y preguntas conceptuales.
8. `resumen.tex`: resumen en cajas `tcolorbox`.

---

## Metodología de escritura

La secuencia habitual de una idea es:

1. presentar una situación o una pregunta que motive la noción;
2. introducir la notación y explicar qué significa cada parte;
3. distinguir la operación de la expresión que la representa y de su valor;
4. mostrar uno o más ejemplos completamente desarrollados;
5. justificar las propiedades a partir de ideas ya introducidas, cuando sea posible;
6. practicar mediante ejercicios agrupados por propósito;
7. ampliar el conjunto numérico cuando el conjunto anterior ya no alcanza;
8. separar el concepto del algoritmo de cálculo;
9. cerrar con un resumen de las ideas y relaciones principales.

Los capítulos no deben avanzar como una lista de reglas aisladas. La ampliación de `N` a `Z` y de `Z` a `Q` debe aparecer como respuesta a operaciones o ecuaciones que no pueden resolverse en el conjunto anterior. Las expresiones equivalentes deben utilizarse para mostrar que una cantidad puede tener varias representaciones.

El texto se dirige preferentemente al lector mediante **usted**. Hay formulaciones antiguas en primera persona o con `tú` que pueden revisarse gradualmente, pero no deben introducirse nuevas inconsistencias. El tono debe ser directo, accesible y preciso, sin infantilizar al lector.

Los ejercicios se agrupan por la tarea que se quiere practicar, no por niveles llamados “básico”, “intermedio” o “avanzado”. Los tipos ya utilizados son:

- reescribir expresiones;
- evaluar expresiones;
- descomponer números;
- completar igualdades;
- reconocer la estructura de una expresión;
- resolver y comprobar ecuaciones;
- justificar propiedades;
- construir expresiones con condiciones dadas;
- cambiar entre representaciones fraccionarias, divisiones y decimales;
- clasificar números según los conjuntos a los que pertenecen.

Cuando un ejercicio admita varias respuestas, debe decirse explícitamente. Cuando la consigna evalúe una expresión, conviene aclarar si se pide solo la transformación o también el numeral final.

---

## Principios conceptuales transversales

### Número y representación

Un número y una forma de escribirlo no son lo mismo. Expresiones distintas pueden representar la misma cantidad:

```latex
302+22=324
```

La expresión `302+22` ya representa un número; evaluarla consiste en encontrar otra representación equivalente, normalmente más directa. No debe decirse que el resultado “crea” la suma o que solo el numeral final es el número.

Este principio reaparece en:

```latex
4\cdot2=2+2+2+2=8
\qquad
1\div2=\frac12=0{,}5.
```

### Operación, expresión, evaluación y algoritmo

- Una **operación** es la regla que actúa sobre ciertos operandos.
- Una **expresión** es una escritura que representa un número o una operación entre números.
- **Evaluar** una expresión es determinar o producir una representación de su valor.
- Un **algoritmo** es un procedimiento sistemático para evaluar ciertos tipos de expresiones.

El algoritmo decimal de la suma no define la adición. Del mismo modo, el algoritmo de la división no define la división. Ambos organizan propiedades, descomposiciones y operaciones ya estudiadas.

### Estructura de las expresiones

Hay que identificar el nivel en el que actúa cada operación. En

```latex
7+3\cdot5
```

la suma exterior tiene como sumandos `7` y `3\cdot5`; dentro del segundo sumando, `3` y `5` son factores. No debe confundirse el producto completo con sus factores.

No es correcto afirmar que no se pueden “sumar sumas y productos”. Sí se puede sumar una cantidad representada por un producto, por ejemplo `2+(3\cdot4)`. Lo importante es reconocer la estructura de la expresión.

### Igualdad y ecuación

El signo `=` afirma que sus dos miembros representan el mismo número; no es únicamente una orden para calcular de izquierda a derecha. Una ecuación es una igualdad con uno o más valores desconocidos. Resolverla consiste en encontrar los valores que la hacen verdadera.

Las transformaciones que conservan una igualdad deben aplicarse a ambos miembros. La frase “pasar al otro lado y cambiar de signo” puede mencionarse como abreviatura posterior, pero nunca como explicación fundamental.

---

## Contenido consolidado del capítulo 1

### Sistemas de numeración y naturales

Se introduce la idea de que un sistema de numeración permite representar cantidades mediante símbolos y reglas. El sistema decimal es posicional: el valor de una cifra depende de su posición. Por ejemplo,

```latex
4387=4000+300+80+7.
```

Se adopta explícitamente

```latex
\mathbb N=\{0,1,2,3,\ldots\}.
```

La introducción es intuitiva y no pretende definir formalmente los naturales desde los fundamentos.

### Adición

Sobre naturales se escribe

```latex
+\colon\mathbb N\times\mathbb N\to\mathbb N,
```

y luego, al trabajar con enteros,

```latex
+\colon\mathbb Z\times\mathbb Z\to\mathbb Z.
```

Los operandos de una suma son **sumandos**. La adición es binaria: recibe dos números cada vez. Las sumas de más de dos términos son aplicaciones sucesivas de la misma operación; la asociatividad permite omitir paréntesis cuando solo aparecen adiciones.

Se estudian conmutatividad, asociatividad, elemento neutro `0` y existencia del opuesto.

### Enteros y sustracción

El opuesto de `a` es `-a` y satisface

```latex
a+(-a)=0.
```

Se adopta

```latex
\mathbb Z=\{\ldots,-3,-2,-1,0,1,2,3,\ldots\},
\qquad
\mathbb N\subseteq\mathbb Z.
```

El signo menos tiene dos usos relacionados pero distintos:

- en `-5`, indica el opuesto de `5`;
- en `8-5`, indica una sustracción.

La sustracción se define mediante la adición:

```latex
a-b=a+(-b).
```

Al reescribir una expresión como suma de opuestos, cada número con su signo constituye un sumando. La sustracción no debe tratarse como conmutativa ni asociativa; la libertad para ordenar o agrupar aparece después de convertirla en una suma.

### Igualdades y ecuaciones

Se trabaja principalmente con ecuaciones aditivas, por ejemplo `x+3=8` y `x-4=9`. La solución se obtiene sumando el opuesto del término correspondiente en ambos miembros y se comprueba mediante sustitución.

### Algoritmo de la adición

Se presenta después del cálculo mental y de las descomposiciones. La alineación de cifras responde al valor posicional. Las “llevadas” se explican mediante descomposiciones como

```latex
13=10+3,
```

es decir, diez unidades forman una decena. El procedimiento vertical es una herramienta para evaluar sumas, no la definición de la adición.

---

## Contenido consolidado del capítulo 2

### Producto de naturales

El producto es una operación binaria:

```latex
\cdot\colon\mathbb N\times\mathbb N\to\mathbb N.
```

En naturales se introduce mediante la suma repetida:

```latex
a\cdot b=
\underbrace{b+b+\cdots+b}_{a\text{ veces}}.
```

Los operandos son **factores** y el valor de la expresión completa se llama **producto**. La suma repetida es una interpretación inicial sobre `N`, no una definición literal suficiente para productos racionales.

### Estructura y precedencia

En una expresión que combina suma y producto, la precedencia del producto sobre la suma es una **convención de escritura**. Así,

```latex
7+3\cdot5
```

significa `7+(3\cdot5)`, no `(7+3)\cdot5`. No debe justificarse diciendo que el producto es “más importante” ni como consecuencia de que inicialmente se interprete mediante sumas repetidas.

### Propiedades del producto

Sobre naturales se desarrollan:

```latex
a\cdot b=b\cdot a
```

```latex
(a\cdot b)\cdot c=a\cdot(b\cdot c)
```

```latex
a\cdot1=a,\qquad a\cdot0=0
```

```latex
a\cdot(b+c)=a\cdot b+a\cdot c,
```

```latex
(a+b)\cdot c=a\cdot c+b\cdot c.
```

La clausura, la conmutatividad, el neutro, el producto por cero, la asociatividad y la distributividad se motivan mediante sumas repetidas, arreglos rectangulares, agrupaciones y valor posicional. La formulación preferida es que muchas propiedades **pueden comprenderse** a partir de la suma; evitar decir formalmente que el producto “hereda” propiedades sin explicar el argumento.

### Producto de enteros

La suma repetida ya no basta para expresiones como `(-3)\cdot4` o `(-3)\cdot(-4)`. Se extiende el producto a

```latex
\cdot\colon\mathbb Z\times\mathbb Z\to\mathbb Z
```

conservando las propiedades relevantes. Mediante distributividad se obtiene

```latex
a\cdot(-1)=-a.
```

De allí se deduce que multiplicar exactamente un factor por su opuesto produce el opuesto del producto, y que dos factores opuestos producen un producto positivo:

```latex
(-a)\cdot b=-(a\cdot b),
\qquad
(-a)\cdot(-b)=a\cdot b.
```

La regla de los signos debe presentarse como consecuencia de los opuestos, la distributividad y las propiedades del producto, no como una tabla aislada.

### Racionales, fracciones y producto

Los enteros no resuelven ecuaciones como `2\cdot x=1`, por lo que se introduce una ampliación. Para `a,b\in\mathbb Z` con `b\ne0`, la escritura `a/b` representa el número que satisface `b\cdot(a/b)=a`. Los números que admiten tal representación son los racionales:

```latex
\mathbb Q=\left\{\frac ab:a,b\in\mathbb Z,\ b\ne0\right\}.
```

Una misma cantidad puede tener representaciones fraccionarias equivalentes:

```latex
\frac ab=\frac{ac}{bc},\qquad c\ne0.
```

El producto racional se justifica conceptualmente y queda expresado por

```latex
\frac ab\cdot\frac cd=\frac{a\cdot c}{b\cdot d}.
```

La suma repetida no se utiliza como explicación general de este producto.

### Inverso y división

Todo racional no nulo tiene inverso multiplicativo. Si `a\ne0`,

```latex
\left(\frac ab\right)^{-1}=\frac ba.
```

El cero no tiene inverso porque ningún producto `0\cdot x` puede ser `1`. Para `x,y\in\mathbb Q` con `y\ne0`, la división se define como

```latex
x\div y=x\cdot y^{-1}.
```

Por tanto, dividir no se define mediante restas sucesivas. Las restas sucesivas son solo una estrategia útil para algunos cocientes naturales.

### Decimales y algoritmo de la división

La escritura decimal es otra representación de ciertos racionales; no crea un conjunto numérico nuevo. Se conectan décimos, centésimos y milésimos con potencias de diez:

```latex
0{,}5=\frac12,
\qquad
0{,}25=\frac14.
```

El algoritmo de la división se explica como una forma compacta de combinar productos, restas, descomposición y valor posicional. Puede continuar con décimos, centésimos y milésimos cuando el cociente no es entero. No debe presentarse como una definición nueva de la división.

### Conjuntos numéricos

Se establece la cadena de inclusiones:

```latex
\mathbb N\subseteq\mathbb Z\subseteq\mathbb Q.
```

Una escritura puede ocultar el conjunto más pequeño al que pertenece el número: por ejemplo, `5`, `5/1` y `5{,}0` representan el mismo racional, que además es entero y natural.

---

## Convenciones LaTeX y estilo técnico

- Mantener el idioma español con `polyglossia` y la notación matemática de `amsmath`, `amssymb` y `amsthm`.
- Compilar con XeLaTeX o LuaLaTeX, porque `main.tex` usa `fontspec`.
- Usar `\input` para las secciones internas de cada capítulo y `\include` para los capítulos desde `main.tex`.
- Usar `example`, `definitionbox`, `corollary`, `proposition`, `remark` y `property` cuando haga falta una caja numerada con título; todos están definidos en `misc/envs.tex`.
- Usar `note` para aclaraciones breves no numeradas.
- Usar `tcolorbox` con el estilo `resumen` en las secciones finales de resumen.
- Respetar la numeración automática de secciones, ejemplos y cajas. No hardcodear números de capítulo o de ejemplo.
- Emplear coma decimal en el texto español: `0{,}5`.
- Mantener los nombres de archivo y las rutas actuales; no volver a los archivos históricos eliminados `chapters/1_suma_y_los_numeros.tex` y `chapters/2_producto.tex`.

---

## Puntos pendientes y precauciones

- Desarrollar `chapters/3_potencia/main.tex` siguiendo la metodología ya establecida. La nota al pie de `5_producto_racional.tex` anuncia que las potencias se profundizarán allí.
- Revisar la introducción de `1_sistemas_numeracion.tex`: contiene formulaciones coloquiales y la frase “los números no existen, los inventa usted”, que puede entrar en tensión con el tratamiento posterior de los números como objetos matemáticos. Si se edita, conservar la intuición histórica/conceptual sin afirmar una tesis filosófica innecesariamente fuerte.
- Revisar gradualmente la consistencia del tratamiento de **usted**, especialmente en el material inicial del capítulo 1.
- Revisar afirmaciones sobre cierre y propiedades cuando se generalicen a nuevos conjuntos. Una propiedad puede mantenerse, pero su dominio debe indicarse explícitamente.
- Mantener la distinción entre una decisión matemática y una convención de notación. Esto es especialmente importante para precedencia, escritura decimal, fracciones equivalentes y algoritmos.

---

## Próximo punto de trabajo

El siguiente trabajo natural es desarrollar el capítulo de potencias. Antes de escribirlo, conviene decidir su recorrido exacto, pero debería conectar con lo ya establecido:

1. potencia como producto repetido en naturales;
2. base, exponente y valor de una potencia;
3. relación entre producto y potencia;
4. propiedades justificadas, no solo reglas de exponentes;
5. extensión cuidadosa a enteros y, si corresponde, exponentes cero o negativos;
6. ejercicios agrupados por propósito;
7. resumen final en cajas.

Al continuar la redacción, no tratar el producto repetido como definición general de toda potencia sin delimitar el dominio. Conservar la estrategia central del libro: motivar la ampliación, distinguir número y representación, reconocer la estructura de las expresiones y separar concepto de algoritmo.
