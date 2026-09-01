-# Hoja de ruta del capítulo 4: Polinomios

## Objetivo

Pasar del cálculo con números y potencias al cálculo literal, introduciendo los polinomios como expresiones que pueden evaluarse, transformarse y utilizarse para resolver ecuaciones.

## Recorrido propuesto

1. **Del cálculo numérico al cálculo literal**
   - Letras como cantidades variables o desconocidas.
   - Expresiones algebraicas y evaluación.
   - Variables, constantes y parámetros.
   - Convenciones como `3x`, `x^2` y `2(x+1)`.

2. **Monomios y polinomios**
   - Monomio, coeficiente, parte literal, término y grado.
   - Términos semejantes.
   - Polinomio, grado y forma ordenada.
   - Polinomios como expresiones y como funciones.
   - Polinomio nulo, constantes, polinomios lineales y cuadráticos.

3. **Suma y resta de polinomios**
   - Reducción de términos semejantes.
   - Justificación mediante la propiedad distributiva.
   - Evaluación de polinomios antes y después de transformar su escritura.

4. **Multiplicación de polinomios**
   - Producto de monomios.
   - Monomio por polinomio.
   - Polinomio por polinomio.
   - Distributividad como fundamento del algoritmo.
   - Productos notables:
     \[
     (a+b)^2,\qquad (a-b)^2,\qquad (a+b)(a-b).
     \]

5. **División de polinomios**
   - División por un monomio.
   - División de un polinomio por otro.
   - Algoritmo de la división:
     \[
     P(x)=D(x)Q(x)+R(x),\qquad \deg R<\deg D.
     \]
   - Diferencia entre dividendo, divisor, cociente y resto.

6. **Factoreo: la multiplicación en sentido inverso**
   - Factor común.
   - Factor común por agrupación.
   - Diferencia de cuadrados.
   - Trinomio cuadrado perfecto.
   - Trinomios cuadráticos sencillos.
   - Suma y diferencia de cubos, si el alcance del capítulo lo permite.
   - Comprobación expandiendo nuevamente el factoreo.

7. **Raíces de un polinomio**
   - Definición:
     \[
     a\text{ es raíz de }P\Longleftrightarrow P(a)=0.
     \]
   - Diferencia entre raíz de un polinomio, cero de una función y solución de una ecuación.
   - Motivación: utilizar las raíces para resolver ecuaciones.
   - Propiedad del producto nulo:
     \[
     AB=0\Longrightarrow A=0\text{ o }B=0.
     \]
   - Teorema del factor:
     \[
     P(a)=0\Longleftrightarrow (x-a)\text{ es factor de }P(x).
     \]

8. **Teorema del resto y regla de Ruffini**
   - El resto de dividir `P(x)` por `x-a` es `P(a)`.
   - Ruffini como forma abreviada de esa división.
   - Uso de Ruffini para comprobar raíces y reducir el grado.
   - Aclarar que Ruffini no encuentra automáticamente todas las raíces: requiere una raíz o candidatos adecuados.

9. **Ecuaciones de segundo grado**
   - Resolución por factoreo.
   - Completar el cuadrado.
   - Demostración de la fórmula cuadrática:
     \[
     x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}.
     \]
   - Discriminante y cantidad de soluciones reales.
   - Relación entre fórmula, raíces y factorización.

10. **Ejercicios integradores y resumen**
    - Evaluar, sumar, multiplicar y dividir polinomios.
    - Expandir y factorizar para comprobar resultados.
    - Encontrar raíces mediante factoreo y Ruffini.
    - Resolver ecuaciones lineales, cuadráticas y algunas de grado superior factorizables.

## Decisiones de alcance y orden

- No comenzar con factoreo: primero debe construirse la multiplicación de polinomios, ya que factorear es realizarla en sentido inverso.
- No presentar “ecuaciones polinomiales” como si todas fueran a resolverse en este capítulo. El alcance será: ecuaciones de primer y segundo grado, y algunas ecuaciones de grado superior resolubles por factoreo y Ruffini.
- Demostrar la fórmula cuadrática mediante completar el cuadrado, en lugar de presentarla como una regla aislada.
- Introducir Ruffini después del teorema del resto y del teorema del factor, para explicar qué calcula y por qué funciona.
- Trabajar inicialmente con raíces reales y señalar que algunos polinomios, como `x^2+1`, no tienen raíces reales. La introducción de los números complejos puede reservarse para un capítulo posterior.
- Mantener la estructura de los capítulos anteriores: motivación, notación, ejemplos desarrollados, propiedades justificadas, ejercicios agrupados por propósito y resumen final.
