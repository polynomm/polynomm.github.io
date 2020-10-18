---
layout: default
title: Soluciones Ecuaciones
nav_order: 2020-10-19
description: "Soluciones"
last_modified_date: 2020-10-19T11:40:00+0000
grand_parent: Listas POLYNOMM
parent: POLYNOMM 2020
---

<link rel="stylesheet" href="{{ '/assets/css/just-the-docs-degRosa.css' | absolute_url }}">
<script>
    jtd.setTheme('degRosa');
</script>

# Soluciones de la lista de&nbsp;<span class="deg-sitio deg-sitio-texto">Ecuaciones</span><i class="jpa-anim-rel-face_screaming_in_fear jpa-2em"></i>
{:.fs-9 .no-toc}

Te traemos las soluciones a los problemas de la **Lista POLYN<span class="deg-sitio deg-sitio-texto">OMM</span>** del 28 de septiembre. 
{:.fs-6 .fw-300}

Álgebra
{:.label .deg-algebra .deg-algebra-fondo}

Teoría de números
{:.label .deg-numeros .deg-numeros-fondo}

---

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1</span>
{: .no_toc}
<!--Math League HS 2010-2011 https://davidaltizio.web.illinois.edu/More%20Diophantine%20Equations%20Overview.pdf-->

Encuentra todos los pares de enteros positivos \\((a,b)\\) tales que \\(a^2+b\\) excede a \\(b^2+a\\) por 36.
#### Solución
{: .no_toc}

En este problema, no es necesario realizar muchas operaciones:

$$\begin{align*}
36&=(a^2+b)-(b^2+a)\\[0.5em]
&=a^2-b^2+b-a\\[0.5em]
&=(a+b)(a-b)-(a-b)\\[0.5em]
&=(a+b-1)(a-b)   
\end{align*}$$
{:.math}

Vemos que \\(a+b+1>0\\), por lo que \\(a-b>0\\) y ambos factores son los divisores positivos de 36. Notamos que \\(a+b+1>a-b\\), y ambos tienen distinta paridad (ya que su diferencia es \\(2b+1\\), un número impar), por lo que analizaremos los siguientes casos:

1. \\(a+b-1=36\\), \\(a-b=1\\):
    >Resolviendo el sistema de ecuaciones, se obtiene que \\(a=19\\) y \\(b=18\\).
2. \\(a+b-1=12\\), \\(a-b=3\\):
    >Nuevamente, al resolver el sistema de ecuaciones, \\(a=8\\) y \\(b=5\\).
3. \\(a+b-1=9\\), \\(a-b=4\\):
    >En este último caso, \\(a=7\\) y \\(b=3\\).

Por lo que todos los pares de enteros \\((a,b)\\) que satisfacen las condiciones son \\((19,18)\\), \\((8,5)\\) y \\((7,3)\\).
### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">2</span>
{: .no_toc}

<!-- Problema propio https://davidaltizio.web.illinois.edu/More%20Diophantine%20Equations%20Overview.pdf -->
\\(181^2\\) puede escribirse como la diferencia de los cubos de dos enteros positivos. Encuentra la suma de dichos enteros.

#### Solución
{: .no_toc}

Sea \\(n\\) el más pequeño de dichos enteros positivos. Entonces

$$181^2=(n+1)^3-n^3=3n^2+3n+1$$
{:.math}

Esto significa que:

$$\begin{align*}
n(n+1)&=\dfrac{181^2-1}{2}\\[0.5em]
&=\dfrac{180\cdot 182}{2}\\[0.5em]
&=(2^2\cdot 3\cdot 5)(2\cdot 7\cdot 13)\\[0.5em]
&=(2^3\cdot 13)\cdot(3\cdot 5\cdot 7)\\[0.5em]
&=104\cdot 105    
\end{align*}$$
{:.math}

La única solución positiva de esta ecuación es \\(n=104\\), por lo que la suma requerida es \\(2n+1=209\\).

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">3</span>
{: .no_toc}

<!-- Math Message Boards FAQ & Community Help | AoPS. (2015, 4 febrero). AoPS. https://artofproblemsolving.com/community/c5t281f5h623945_symmetric_algebraic_equation -->

Si \\( y+4 = (x-2)^2 \\), \\(x+4 = (y-2)^2\\) y \\( x\ne y \\), encuentra el valor de \\( x^2+y^2\\).

#### Solución
{: .no_toc}

Podemos restar ambas ecuaciones y factorizar la diferencia de cuadrados:

$$
\begin{align*}
(y+4)-[x-4]&=(x-2)^2-[y-2]^2\\
y-x&=(x-2+y-2)(x-y)\\
0&=(x-y)(x+y-4)+x-y\\
&=(x-y)(x+y-3)
\end{align*}
$$
{:.math }

Como \\( x\ne y\\), \\( x-y\ne 0\\), es decir, \\( x+y=3 \\) en la última ecuación para que se cumpla la igualdad. Ahora, sumamos las dos ecuaciones iniciales para terminar.

$$
\begin{align*}
(y+4)+[x-4]&=(x-2)^2+[y-2]^2\\
x+y+\cancel{8}&=x^2+y^2-4(x+y)+\cancel{8}\\[0.5em]
x^2+y^2&=5(x+y)\\
&=15
\end{align*}
$$
{:.math }

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">4</span>

<!-- Art of Problem Solving. (s. f.). AoPS. https://artofproblemsolving.com/wiki/index.php/1990_AIME_Problems/Problem_15 -->
Encuentra el valor de \\( a_{}^{}x^5 + b_{}y^5\\), si los números reales \\( a \\), \\( b \\), \\( x \\), y \\( y\\) satisfacen las siguientes ecuaciones:

$$
\begin{align*}
ax + by&=3\\
ax^2 + by^2&=7\\
ax^3 + by^3&=16\\
ax^4 + by^4&=42
\end{align*}
$$
{:.math }

#### Solución

Sea \\(S = (x + y)\\) y \\(P = xy\\). Podemos usar la siguiente relación

$$(ax^n + by^n)(x + y) = (ax^{n + 1} + by^{n + 1}) + (xy)(ax^{n - 1} + by^{n - 1})$$
{:.math }

con las ecuaciones iniciales.

$$\begin{eqnarray*}(ax^2 + by^2)(x + y) & = & (ax^3 + by^3) + (xy)(ax + by) \\
(ax^3 + by^3)(x + y) & = & (ax^4 + by^4) + (xy)(ax^2 + by^2)\end{eqnarray*}$$
{:.math}

Lo anterior indica que

$$\begin{eqnarray*}7S & = & 16 + 3P \\
16S & = & 42 + 7P\end{eqnarray*}$$
{:.math }

Resolviendo el sistema, obtenemos que \\(S = - 14\\) and \\(P = - 38\\). Podemos finalizar de la siguiente manera:

$$\begin{eqnarray*}(ax^4 + by^4)(x + y) & = & (ax^5 + by^5) + (xy)(ax^3 + by^3) \\
(42)(S) & = & (ax^5 + by^5) + (P)(16) \\
(42)( - 14) & = & (ax^5 + by^5) + ( - 38)(16)\end{eqnarray*}$$
{:.math}

Es decir:

$$ax^5 + by^5 = 20$$
{:.math .math-display .deg-sitio .deg-sitio-fondo}


### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">5</span>
{: .no_toc}

<!--Math Message Boards FAQ & Community Help | AoPS. (2019, 7 agosto). AoPS. https://artofproblemsolving.com/community/c4h1890517p12898772-->
Determina todas las soluciones reales \\( x \\), \\( y \\) y \\( z \\) del siguiente sistema de ecuaciones:

$$\begin{cases}
x^3 - 3x = 4 - y \\
2y^3 - 6y = 6 - z \\
3z^3 - 9z = 8 - x\end{cases}$$
{:.math}

#### Solución
{: .no_toc}

El siguiente sistema es equivalente al sistema inicial:

$$
\left\{\begin{eqnarray*} x^3-3x-2&=&2-y\\2(y^3-3y-2)&=&2-z\\3(z^3-3z-2)&=&2-x\end{eqnarray*}\right.
$$
{:.math}

Podemos factorizar cada ecuación de la siguiente manera

$$
\left\{\begin{eqnarray*} (x+1)^2(x-2)&=&2-y\\2(y+1)^2(y-2)&=&2-z\\3(z+1)^2(z-2)&=&2-x\end{eqnarray*}\right.
$$
{:.math}

Vemos que, si alguno de los números \\( x \\), \\( y \\) o \\( z \\) es igual a 2, todos son iguales a 2, pues el lado derecho de una ecuación sería un factor 0 en el lado izquierdo de otra ecuación. 

Finalmente, si \\( x, y, z \ne 2\\), podemos multiplicar todas las ecuaciones, y obtener una contradicción, ya que los cuadrados de números reales no son negativos:

$$
\begin{eqnarray*} 
x,y,z&\ne&2\\
\implies 6(x+1)^2(y+1)^2(z+1)^2(x-2)(y-2)(z-2)&=&(2-x)(2-y)(2-z)\\
\implies 6(x+1)^2(y+1)^2(z+1)^2&=&-1
\end{eqnarray*}
$$
{:.math}

Por lo tanto, la única solución al sistema es \\(x=y=z=2\\).

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">6</span>
{: .no_toc}

<!-- Math Message Boards FAQ & Community Help | AoPS. (2020, 30 mayo). AoPS. https://artofproblemsolving.com/community/c4t281f4h2163356_system_of_equations -->
Resuelva el siguiente sistema de ecuaciones

$$
\begin{cases}
x^2+2=x(y+z)\\
y^2+3=y(z+x)\\
z^2+4=z(x+y)
\end{cases}
$$
{:.math }

#### Solución
{: .no_toc}

Primero, cada ecuación nos indica que \\(x\\), \\( y \\) y \\( z \\) son distintos de cero, pues en caso contrario, cada ecuación nos da una contradicción, como \\( 2=0 \\). Así, podemos realizar la división entre \\( x \\), \\( y \\) y \\( z \\).
Lo anterior nos da como resultado el siguiente sistema de ecuaciones:

$$
\begin{cases}
x+\frac{2}{x}=y+z\\[0.5em]
y+\frac{3}{y}=z+x\\[0.5em]
z+\frac{4}{z}=x+y
\end{cases}
$$
{:.math }

Puedes sumar cada par de ecuaciones

$$
\begin{align*}
\left(\cancel{x}+\frac{2}{x}\right)+\left[\cancel{y}+\frac{3}{y}\right]&=(\cancel{y}+z)[z+\cancel{x}]\\
\frac{2}{x}+\frac{3}{y}&=2z\\
2z&=\frac{3x+2y}{xy}\\
\left(y+\frac{3}{y}\right)+\left[z+\frac{4}{z}\right]&=(z+x)[x+y]\\
\frac{3}{y}+\frac{4}{z}&=2x\\
2x&=\frac{4y+3z}{yz}\\
\left(z+\frac{4}{z}\right)+\left[x+\frac{2}{x}\right]&=(x+y)[y+z]\\
\frac{2}{x}+\frac{4}{z}&=2y\\
2y&=\frac{4x+2z}{zx}
\end{align*}
$$
{:.math }

$$
\implies 2xyz=3x+2y=4y+3z=4x+2z
$$
{:.math }

Con lo anterior, podemos deducir las siguiente igualdadades:

$$
\begin{align*}
4xyz-2xyz&=2xyz\\
2(3x+2y)-(4y+3z)&=4x+2z\\
2x&=5z\\
\implies x&=\frac{5z}{2}\wedge z=\frac{2x}{5}\\[0.5em]
2xyz&=2xyz\\
4y+3z&=4x+2z\\
4y+3z&=10z+12z\\
4y&=9z\\
\implies y&=\frac{9z}{4}\\[0.5em]
&=\frac{9x}{10}
\end{align*}
$$
{:.math }

Finalmente, podemos sustituir los valores de \\( y \\) y \\( z \\) en la primera ecuación del sistema inicial:

$$
\begin{align*}
x^2+2&=x(y+z)\\[0.5em]
&=x\left(\frac{9x}{10}+\frac{2x}{5}\right)\\[0.5em]
\implies 2&=\frac{3x^2}{10}\\[0.5em]
\implies x^2&=\frac{20}{3}\\
\implies x_1=\frac{2\sqrt{15}}{3}&\wedge x_2=-\frac{2\sqrt{15}}{3}\\
\end{align*}
$$
{:.math }

Con los valores posibles de \\( x \\) determinados, se concluye que las soluciones \\( (x,y,z) \\) del sistema son <span class="math deg-sitio deg-sitio-fondo" stule="border-">\\( \left(\frac{2\sqrt{15}}{3}, \frac{3\sqrt{15}}{5}, \frac{4\sqrt{15}}{15}\right) \\)</span> y <span class="math deg-sitio deg-sitio-fondo" stule="border-">\\( \left(-\frac{2\sqrt{15}}{3}, -\frac{3\sqrt{15}}{5}, -\frac{4\sqrt{15}}{15}\right) \\)</span>.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">7</span>
{: .no_toc}

<!--Math Message Boards FAQ & Community Help | AoPS. (2010, 19 noviembre). AoPS. https://artofproblemsolving.com/community/c6t281f6h378543_symmetric_simultaneous_equations_of_degree_2010-->
Encuentra todas las 4-tuplas \\( (a,b,c,d) \\) de números reales que satisfacen el siguiente sistema de ecuaciones:

$$\begin{cases}
(b+c+d)^{2010}=3a\\
(a+c+d)^{2010}=3b\\
(a+b+d)^{2010}=3c\\
(a+b+c)^{2010}=3d
\end{cases}$$
{:.math}

#### Solución
{: .no_toc}

Primero, dado que 2010 es un entero positivo par, \\( a,b,c,d \ge 0 \\). Dado que el sistema es equivalente en cualquier permutación de los 4 números, ***sin pérdida de generalidad*** podemos suponer que \\( a\ge b\ge c\ge d\ge 0 \\). En este caso:

$$\begin{eqnarray*}
(b+c+d)^{2010}\ge (a+c+d)^{2010}&\ge&(a+b+d)^{2010}\ge(a+b+c)^{2010}\\
\implies (b+c+d)\ge(a+c+d)&\ge&(a+b+d)\ge(a+b+c)\\
\implies d\ge c&\ge&b\ge a
\end{eqnarray*}
$$
{:.math}

Esto quiere decir que \\(a=b=c=d\\). En este sentido, \\((0,0,0,0)\\) es claramente una solución, pero si todos los números son distintos de cero, basta con sustituir \\( b \\), \\( c \\) y \\( d \\) en la primera ecuación:

$$\begin{eqnarray*}
(3a)^{2010}=3a&\implies&a=\frac{1}{3}
\end{eqnarray*}
$$
{:.math}

Por lo que la otra tupla solución es \\(\left(\frac{1}{3},\frac{1}{3},\frac{1}{3},\frac{1}{3}\right)\\).

