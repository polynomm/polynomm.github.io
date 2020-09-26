---
layout: default
title: Soluciones del Examen selectivo OMMEB 2020
nav_order: 2
description: "Soluciones completas del examen."
last_modified_date: 2020-08-29T10:00:00+0000
grand_parent: Tlaxcala
parent: Tlaxcala 2020
---

<link rel="stylesheet" href="{{ '/assets/css/just-the-docs-degArcoiris.css' | absolute_url }}">
<script>
    jtd.setTheme('degArcoiris');
</script>

# Soluciones del Selectivo final&nbsp;<span class="deg-sitio deg-sitio-texto">OMMEB 2020</span><i class="jpa-anim-rel-face_screaming_in_fear jpa-2em"></i>
{:.fs-9 .no-toc}

ADVERTENCIA: Los procedimientos matemáticos descritos pueden provocar emociones intensas.<i class="jpa-anim-rel-smiling_face_with_sunglasses jpa-2em"></i><i class="jpa-anim-rel-winking_face jpa-2em"></i><i class="jpa-anim-rel-partying_face jpa-2em"></i><i class="jpa-anim-rel-smiling_face_with_heart_eyes jpa-2em"></i><i class="jpa-anim-rel-face_blowing_a_kiss jpa-2em"></i>
{:.fs-6 .fw-300}

Especial
{:.label .deg-especial .deg-especial-fondo}

---
1. TOC
{:toc}

¡Hola! Se ha preparado un documento con las soluciones de todos los problemas del examen selectivo, para que todos puedan analizar su desempeño y mejorar. Las soluciones están explicadas detalladamente, y reúnen análisis y demostración, por lo que pueden parecer demasiado largas o teóricas. Sin embargo, casi la totalidad de los problemas requieren desarrollar una idea sencilla.

<div></div>
{:.salto .no-mostrar}

# Problemas opcionales (o parte A)

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-1</span>

Sean \\( p \\) y \\( q \\) números primos distintos entre si. ¿Cuántos divisores positivos tiene \\( p^2\cdot q^2 \\)?

>**a.** 2&#8195;
>**b.** 4&#8195;
>**c.** 8&#8195;
>**d.** 7&#8195;
>**e.** 9

#### Solución
{: .no_toc}

Dado que los números que dividen a \\( p^2\cdot q^2 \\) sólo pueden tener como factores primos a \\( p \\) y \\( q \\), cun un exponente menor o igual a 2, podemos escribir fácilmente todas las soluciones:

$$
\begin{array}{ccc}
  p^0q^0&p^0q^1&p^0q^2\\
  p^1q^0&p^1q^1&p^1q^2\\
  p^2q^0&p^2q^1&p^2q^2
\end{array}
$$

Lo cual podemos entender de la siguiente manera: Dado que el exponente de \\( p \\) es a lo más 2 y el exponente de \\( q \\) es a lo más 2, los exponentes posibles para \\( p \\) y \\( q \\) son 0, 1 y 2. Es decir, para el primer exponente tenemos tres posibilidades, y para el segundo también, lo cual nos da como resultado 9 divisores.

Aplicando el mismo razonamiento, podemos aplicar esta idea a un caso más general: si tienes varios números primos distintos entre sí \\( p_1, p_2,\dots p_k\\), y el número \\( n \\) se puede expresar de la forma:

$$
n=p_1^{\alpha_1}\cdot p_2^{\alpha_2}\dots p_k^{\alpha_k}
$$

Donde para cada valor de \\( i \\), \\( \alpha_i \\) es un número entero no negativo.

El número de divisores de \\( n \\), es decir, \\( d(n) \\), satisface la siguiente igualdad:

$$
d(n)=(a_1+1)(a_2+1)\cdots(a_k+1)
$$


### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-2</span>

Un tonel esta lleno \\( \frac{1}{4} \\) de lo que no esta lleno ¿Qué fracción del tonel queda vacío, si se vacía \\( \frac{1}{3} \\) de lo que no se vacía?

>**a.** \\( \frac{11}{20} \\)&#8195;
>**b.** \\( \frac{3}{4} \\)&#8195;
>**c.** \\( \frac{17}{20} \\)&#8195;
>**d.** \\( \frac{3}{5} \\)&#8195;
>**e.** \\( \frac{1}{20} \\)&#8195;

#### Solución
{:.no_toc}

Para entender este problema, podemos cambiar las fracciones fácilmente:

> **La parte que está vacía del tonel es cuatro veces mayor a la que está llena.**

Esto quiere decir que la parte llena es una quinta parte de la capacidad del tonel.

Ahora, analizaremos la siguiente parte del problema:

> **Lo que se quedó de la parte llena es tres veces mayor a lo que se vació.**

Esto quiere decir que lo que se quedó de la parte llena es tres cuartas partes de la parte llena.

La fracción llena que queda al final en el tonel es \\( \frac{1}{5}\cdot\frac{3}{4}=\frac{3}{20}\\), y la fracción vacía es \\( 1-\frac{3}{20}=\frac{17}{20}\\)

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-3</span>

¿Cuál es la suma de los números comprendidos entre 10 y 30 solo tienen dos divisores?

>**a.** 8&#8195;
>**b.** 100&#8195;
>**c.** 112&#8195;
>**d.** 121&#8195;
>**e.** 211&#8195;

#### Solución
{:.no_toc}

Los números que tienen dos divisores son los números primos. Dado que los números primos comprendidos entre 10 y 30 son 11, 13, 17, 19, 23 y 27, la respuesta es:

$$
11+13+17+19+23+29=112
$$
{:.math .grid}

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-4</span>

¿Cuántos rectángulos hay en esta figura?

<div class="geo-100"><div id="ProblemaRectangulos1"></div></div>

>**a.** 8&#8195;
>**b.** 9&#8195;
>**c.** 10&#8195;
>**d.** 11&#8195;
>**e.** 12

#### Solución
{:.no_toc}

Podemos analizar cada vértice en la figura, sistemáticamente, de arriba a abajo y de izquierda a derecha, para verificar si es el vértice superior izquierdo de un rectángulo. 

<div class="geo-100"><div id="ProblemaRectangulosSolucion1"></div></div>

De esta manera, obtenemos que hay 11 rectángulos posibles en la figura.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-5 2A-5 3A-3</span>

Un ocho son dos círculos del mismo tamaño y tangentes entre sí. ¿Cuántos ochos hay en este dibujo?

<div class="geo-100"><div id="ProblemaOchos1"></div></div>

>**a.** 25&#8195;
>**b.** 28&#8195;
>**c.** 30&#8195;
>**d.** 50&#8195;
>**e.** 60

#### Solución
{:.no_toc}

Podemos hacer lo siguiente: para cada círculo, contamos cuántos círculos son tangentes a él. Los círculos de los vértices tienen dos círculos tangentes, los que están en los bordes tienen cuatro círculos tangentes, y cualquier círculo en el interior tiene 6. Ahora, dados dos círculos que forman un 8, a los cuales nombraremos \\( A \\) y \\( B \\), se tiene que hemos contado que el círculo \\( A \\) es tangente al círculo \\( B \\), y viceversa. Es decir, que la suma de los círculos tangentes a cada círculo es el doble que el número de *ochos*. Podemos concluir que el número de ochos es exactamente

$$
\frac{3\cdot2+3\cdot4(n-2)+6\frac{(n-3)(n-2)}{2}}{2},\;\;\;\;n > 2
$$
{:.math .grid}

Donde \\( 3\cdot 2\\) es el número de círculos tangentes a los círculos en los vértices; \\( 3\cdot4(n-2) \\) el número de círculos tangentes a los círculos de los bordes y \\( 6\frac{(n-3)(n-2)}{2} \\) el número de círculos tangentes a los círculos interiores. Con \\( n=5 \\), se obtienen 30 ochos posibles.

Es necesario aclarar que la ecuación sólo tiene sentido para \\( n>2 \\)

#### Solución alternativa
{:.no_toc}

Una solución alternativa es la siguiente. Cuente todos los círculos excepto los de la última hilera. A todos esos círculos, se les asignará un ocho, de manera que las rectas que pasa por el centro de los dos círculos que forman todos estos ochos tienen la misma dirección. Usted puede rotar la figura \\( 120^\circ \\) y contar los ochos rotados. 

<div class="geo-100"><div id="ProblemaOchosSolucionRotacion1"></div></div>

El número de círculos que hay sin contar los de la última hilera es \\( \frac{(n-1)n}{2}\\). Como se cuentan las tres rotaciones de cada ocho, el número de ochos es:

$$
3\cdot \frac{(n-1)n}{2},\;\;\;\;n\in\mathbb{N}
$$
{:.math .grid}

Y cuando \\( n=5 \\), hay 30 ochos.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-6 2A-1</span>&nbsp;

La secuencia de Fibonacci está definida por \\(F_1=F_2=1 \\) y \\( F_{n+2}=F_{n+1}+F_n\\). 

¿Cuál es el residuo que se obtiene al dividir

$$F_{2020}+F_{2019}+...+F_2+F_1$$
{:.math .grid}

entre 5?

>**a.** 0&#8195;
>**b.** 1&#8195;
>**c.** 2&#8195;
>**d.** 3&#8195;
>**e.** 4

#### Solución
{:.no_toc}

Basta con ver los primeros 20 residuos al dividir entre 5 de la secuencia:

$$
1,1,2,3,0,3,3,1,4,0,4,4,3,2,0,2,2,4,1,0
$$
{:.math .grid}

Vemos que, cada 20 términos, la secuencia repite sus residuos. Finalmente:

$$
 \begin{align*}
   F_{2020}+F_{2019}+\dots+F_2+F_1&\equiv 101(1+1+2+3+\cdots +2+4+1+0) \mod{5}\\
   &\equiv 1+1+2+3+0+3+3+1+4+0\\
   &\phantom{\equiv 1\;}+4+4+3+2+0+2+2+4+1+0 \mod{5}\\
   &\equiv 0 \mod{5}
 \end{align*}
$$
{:.math .grid}


### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-7 2A-8 3A-6</span>

En el lado \\( BC \\) de un triángulo \\( ABC \\) se ubica el punto \\( P \\) de manera que \\( AC + CP = PB \\). Sea R el punto medio de \\( AB \\). Si \\( \angle RPB = 43^\circ \\), encuentra la medida del ángulo \\( \angle ACB \\).

>**a.** \\( 43^\circ\\)&#8195;
>**b.** \\( 90^\circ-43^\circ\\)&#8195;
>**c.** \\( 30^\circ+43^\circ\\)&#8195;
>**d.** \\( 2\cdot 43^\circ\\)&#8195;
>**e.** \\( 45^\circ+43^\circ\\)

#### Solución
{:.no_toc}

Trace un punto \\( A^\prime \\) sobre el rayo \\( \overrightarrow{BC} \\) tal que \\( AC=A^\prime C\\). Dado que \\( A^\prime P=PB \\) y \\( \frac{PB}{A^\prime P}=\frac{BR}{AR} \\), por el Teorema de Tales se tiene que \\( PR\parallel A^\prime A\\).
<div class="geo-100"><div id="Problema43GradosSolucion1"></div></div>

Esto implica que \\( \angle AA^\prime C=\angle A^\prime AC= 43^\circ\\). En conclusión

$$\angle ACB=86^\circ$$

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-8 2A-3 3A-1</span>

Las soluciones de la ecuación \\( x^2-63x+k=0 \\) son números primos. El número de posibles valores de \\( k \\) es

>**a.** 0&#8195;
>**b.** 1&#8195;
>**c.** 2&#8195;
>**d.** 3&#8195;
>**e.** 4 o más

#### Solución
{:.no_toc}

Sean \\( a \\) y \\( b \\) las soluciones de la ecuación (recuerde que ambas soluciones son números primos). Vemos que:

$$
\begin{align*}
  x^2-63x+k&=0\\
  &=(x-a)(x-b)\\
  &=x^2-(a+b)x+ab
\end{align*}
$$
{:.math .grid}

Los coeficientes de las ecuaciones cuadráticas \\( x^2-63x+k \\) y \\( x^2-(a+b)x+ab \\) deben coincidir, es decir, \\( a+b=63 \\). Dado que ambos números no pueden tener la misma paridad, al menos uno es par y primo, por lo que \\( a=2 \\) y \\( b=61 \\), o \\( a=61 \\) y \\( b=2 \\). Finalmente, \\( k=ab \\), y en ambos casos este valor es único.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-9 2A-4 3A-2</span>

Un piso rectangular es cubierto totalmente con mosaicos cuadrados de igual tamaño, sin recortar o traslapar ningún mosaico y sin que éstos rebasen el borde del piso. Los mosaicos en el borde son rojos, y los demás son blancos. Si hay igual cantidad de mosaicos rojos y blancos, ¿cuántos mosaicos se necesitan para cubrir el piso?

>**a.** 45 o 56&#8195;
>**b.** 48 o 56&#8195;
>**c.** 48 o 60 &#8195;
>**d.** 56 o 60&#8195;
>**e.** 60 o 72

#### Solución
{:.no_toc}

Sean \\( a \\) y \\( b \\) las dimensiones del piso (en mosaicos). Vemos que \\( a,b>1 \\), pues en caso contrario, todos los mosaicos serían rojos. Con esta condición, los mosaicos rojos son exactamente \\( 2(a+b)-4 \\) y los demás mosaicos son \\( (a-2)(b-2) \\), lo cual plantea la siguiente igualdad:

$$
\begin{align*}
  2(a+b)-4&=(a-2)(b-2)\\
  2a+2b-4&=ab+-2a-2b+4\\
  0&=ab-4a-4b+8\\
  8&=ab-4a-4b+16\\
  8&=(a-4)(b-4)\\
\end{align*}
$$
{: .math .grid}

Dado que \\( a-4 \\) y \\( b-4 \\) son enteros, tenemos varios casos

1. \\( a-4 \\) o \\( b-4 \\) son ambos negativos.
   En este caso, notamos que no se cumple la condición \\( a,b>1 \\)
2. \\( a-4=1 \\) o \\( b-4=8 \\) y viceversa.
   En este caso \\( a=5 \\) y \\( b = 12 \\) (y viceversa), por lo que el total de mosaicos sería \\( ab=60 \\).
3. \\( a-4=2 \\) o \\( b-4=4 \\) y viceversa.
   En este caso \\( a=6 \\) y \\( b = 8 \\) (y viceversa), por lo que el total de mosaicos sería \\( ab=48 \\).

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-10 2A-9 3A-7</span>

Diez personas se encuentran en una fila. 

La primera persona en la fila, se mueve al final y la siguiente persona se sienta, de manera que la tercera persona en la fila, ahora es la primera de la fila que está de pie. 

Ahora, esta persona se va al final del fila y la siguiente se sienta. 

Este proceso se repite hasta que solo una persona permanece de pie. ¿Cuál era la posición original de esta última persona?

>**a.** 1&#8195;
>**b.** 5&#8195;
>**c.** 9&#8195;
>**d.** 7&#8195;
>**e.** 10

#### Solución
{:.no_toc}

Dada la mecánica, podemos ver que el siguiente proceso dará el mismo resultado:

1. Colocar a todos en un círculo
2. Sentar de forma alternada y cíclica a las personas que sigan de pie, dejando a la primera persona de pie inicialmente.

El resultado es 9.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-11 2A-6 3A-4</span>

Considera un tablero de 3\\( \times \\)3, donde todas las casillas inicialmente tienen un cero.

$$
\begin{array}{cc}
0&0&0\\
0&0&0\\
0&0&0
\end{array}
$$
{:.math .grid}

Para alterar los números del tablero, solo se permite la siguiente operación: escoger un subtablero de 2\\( \times \\)2 formado por casillas adyacentes, y sumar 1 a todos los números del subtablero. ¿Cuál de los siguientes tableros se puede obtener?

>**a.**&#8195;
  $$\begin{array}{cc}
  5&6&1\\
  9&16&8\\
  4&8&5
  \end{array}
  $$
  &#8195;
>**b.**&#8195;
  $$\begin{array}{cc}
  5&6&1\\
  9&15&6\\
  4&9&5
  \end{array}
  $$
  &#8195;

<br>

>**c.**&#8195;
  $$\begin{array}{cc}
  6&11&5\\
  4&10&7\\
  5&1&2
  \end{array}
  $$
  &#8195;
>**d.**&#8195;
  $$\begin{array}{cc}
  6&12&5\\
  11&8&7\\
  5&2&2
  \end{array}
  $$

#### Solución
{:.no_toc}

Es fácil verificar que los cuatro subtableros tiene una única casilla que no pertenece a ningún otro subtablero. Esas cuatro casillas son las esquinas del tablero. Basta con realizar la operación el número de veces indicado por cada esquina en el subtablero al que pertenece. Se observará que el único tablero que puede obtenerse es:

$$\begin{array}{cc}
5&6&1\\
9&15&6\\
4&9&5
\end{array}
$$
{:.math .grid}

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-12</span>
{: .no_toc}

Alexis tiene 2020 fichas, numeradas del 1 al 2020. Debe distribuirlas en tres cajas, de modo que en ninguna caja queden dos fichas numeradas con números consecutivos. ¿De cuántas formas se puede hacer esto?

>**a.** \\( 3^{1010}\cdot 2^{1010} \\)

>**b.** \\( 3\cdot 2^{2019} \\)

>**c.** \\( 2020!-\binom{2020}{2} \\)

>**d.** \\( 3\cdot2019!-\binom{2019}{2} \\)

>**e.** \\( 2^{2020}-\binom{2020}{2} \\)

#### Solución
{:.no_toc}

Para este problema, colocaremos los números en cada caja en orden. El número 1 tiene 3 posibilidades. Los demás números tienen dos posibilididades: las cajas en las que no se colocó el número anterior. En total, hay \\( 3\cdot 2^{2019}\\) posibilidades.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-13 2A-7 3A-5</span>

Cinco números no negativos \\( a \\), \\( b \\), \\( c \\), \\( d \\) y \\( n \\) satisfacen las ecuaciones 

$$ a+b+c+d=100 $$
{:.math .grid}
    
y

$$a+n=b-n=c\cdot n= \frac{d}{n}$$
{:.math .grid}

¿Cuántas tuplas \\( (a,b,c,d,n) \\) satisfacen las condiciones anteriores?

>**a.** 0&#8195;
>**b.** 1&#8195;
>**c.** 2&#8195;
>**d.** 3&#8195;
>**e.** 4 o más

#### Solución
{:.no_toc}

Podemos expresar todo en términos de \\( c \\) y \\( n \\):

$$
\begin{align*}
  a&=cn+n\\
  b&=cn-n\\
  d&=cn^2
\end{align*}
$$
{:.math .grid}

Es decir:

$$
\begin{align*}
 2cn+c+cn^2&=a+b+c+d\\
 c(n+1)^2&=10^2.
\end{align*}
$$
{:.math .grid}

Esto implica que \\( c \\) es un cuadrado perfecto que divide a \\( 10^2 \\), por lo que analizaremos los siguientes casos:

1. \\(c=1 \\)
   
   En este caso \\( n=9 \\). Pero \\( a=cn-n= 0 \\), es decir, \\( a \\) no es un entero positivo y no hay tuplas válidas.

2. \\(c=4 \\)
   
   En este caso \\( n=4 \\). Las demás variables toman los siguientes valores:
   
   $$
   \begin{align*}
   a&=cn+n\\
   &=20\\
   b&=cn-n\\
   &=12\\
   d&=cn^2\\
   &=64
   \end{align*}
   $$
   {:.math .grid}
   
   La tupla que satisface las condiciones en este caso es \\( (20,12,4,64,4) \\).

3. \\(c=25 \\)
   
   En este caso \\( n=1 \\). Las demás variables toman los siguientes valores:
   
   $$
   \begin{align*}
   a&=cn+n\\
   &=26\\
   b&=cn-n\\
   &=24\\
   d&=cn^2\\
   &=25
   \end{align*}
   $$
   {:.math .grid}
   
   La tupla que satisface las condiciones en este caso es \\( (26,24,25,25,1) \\).

4. \\(c=100 \\)
   
   En este caso \\( n=0 \\), es decir, \\( n \\) no es un entero positivo y no hay tuplas válidas.

Por lo tanto, existen solamente dos tuplas que satisfacen las condiciones planteadas.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-14 2A-11 3A-10</span>

Sea \\( n \\) el entero positivo más pequeño que es múltiplo de 75 y tiene exactamente 75 divisores (incluyendo 1 y \\( n \\)). Encuentra la suma de todos los cuadrados perfectos que dividen a \\( n \\)

>**a.** 48696&#8195;
>**b.** 48966&#8195;
>**c.** 49668&#8195;
>**d.** 49686&#8195;
>**e.** 49866&#8195;

#### Solución
{:.no_toc}

Si \\( n=p_1^{\alpha_1}\cdots p_k^{\alpha_k} \\), siendo \\( p_1,\cdots, p_k \\) números primos distintos y \\( \alpha_1,\cdots, \alpha_k \\) números naturales, entonces el número de divisores satisface la siguiente igualdad:

$$
d(n)=(\alpha_1+1)\cdots(\alpha_k+1)=75
$$
{:.math .grid}
  
Como 75 es impar, \\( \alpha_i \\) debe ser un número par para todo \\( i< k \\), es decir, \\( \alpha_i\ge 2\\). 

Podemos realizar los siguientes casos

1. \\(k\ge 4\\)
   
   $$
   \begin{align*}
     d(n)&=(\alpha_1+1)\cdots(\alpha_k+1)\ge 3\times\dots\times 3\ge 3^4\\
     \implies d(n)&>75
   \end{align*}
   $$
   {:.math .grid}
   
   por lo que no hay enteros \\( n \\) con al menos 4 divisores primos distintos tales que \\( d(n)=75\\).

2. \\(k=3 \\)
   
   En este caso, la única forma de tener tres factores distintos de 1 es cuando \\( \alpha_1 \\), \\(\alpha_2\\) y \\(\alpha_3 \\) son  \\( 4 \\), \\( 4 \\) y \\( 2 \\), respectivamente.

   Tomando los tres números primos más pequeños, el menor valor de \\( n \\) posible en este caso es \\( 2^4\cdot 3^4\cdot 5^2 \\).

3. \\(k=2 \\)
   
   En este caso, las únicas opciones son: \\( \alpha_1=2 \\) y \\( \alpha_2=24 \\); \\( \alpha_1=4 \\) y \\( \alpha_2=14 \\); Tomando los dos números primos más pequeños, el menor valor de n posible en este caso es \\( 2^{14} \cdot 3^4\\).

4. \\( k =1 \\)
   
   La única posibilidad para que \\( d(n)=75 \\) se da cuando \\( \alpha_1 = 74 \\). El número primo más pequeño es 2, por lo que el menor valor de \\( n \\) posible en este caso es \\( 2^{74} \\).

Finalmente:

$$
   \begin{align*}
     2^{14}\cdot 3^4&=2^4 \cdot 3^4 \cdot 2^{10}&2^{74}&=2^4 \cdot 2^7 \cdot 2^5 \cdot 2^{58}\\
     &> 2^4 \cdot 3^4 \cdot 5^2&&> 2^4 \cdot 3^4 \cdot 5^2 \cdot 2^{58}\\
     &&&> 2^4 \cdot 3^4 \cdot 5^2
   \end{align*}
$$
{:.math .grid}

El menor valor de \\( n \\) en todos los casos es \\( 2^4\cdot 3^4 \cdot 5^2 \\), y la suma de los cuadrados perfectos será la siguiente:

$$
   \begin{align*}
     \left(2^0+2^2+2^4\right)\left(3^0+3^2+3^4\right)\left(5^0+5^2\right)&=21\cdot 91 \cdot 26\\
     &=49686
   \end{align*}
$$
{:.math .grid}

La cual puede interpretarse de la siguiente manera: Sólo pueden elegirse los exponentes pares menores o iguales a los exponentes de los factores primos respectivos de \\( n \\).

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1A-15 2A-12 3A-12</span>

¿Cuántos números primos \\( x \\) existen tales que \\( 2^x + x^2 \\) es un número primo?

>**a.** 0&#8195;
>**b.** 1&#8195;
>**c.** 2&#8195;
>**d.** 3&#8195;
>**e.** 4 o más

#### Solución
{:.no_toc}

Sólo es necesario realizar tres casos:

1. \\(x=2 \\)
   
   Este valor no cumple.

2. \\( x=3 \\)
   
   \\( 2^x+x^2 = 17 \\). 

3. \\( x>3 \\)
   
   En este caso, como \\( x>2 \\), \\( x \\) es impar. Esto implica \\( 2^x+x^2\equiv 0 \mod{3} \\), que a su vez implica \\( 2^x+x^2=3 \\). Lo anterior es imposible porque \\( 2^x+x^2>2^3+3^2=17 \\)

Finalmente, existe un único valor de \\( x \\) que satisface las condiciones planteadas.


### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">2A-2</span>

 Roberto para el estreno de su película quiere saber cuántas personas cabrán en el auditorio. Él sabe, que no caben más de 1000 personas. Si intercambia los dígitos de las centenas con las decenas o de las unidades, el número es múltiplo de 11. Y si intercambia el dígito de las unidades con las decenas el número es múltiplo de 2. ¿Cuántas posibilidades hay de cupo en el auditorio?

>**a.** 9&#8195;
>**b.** 18&#8195;
>**c.** 27&#8195;
>**d.** 36&#8195;
>**e.** 45

#### Solución
{:.no_toc}

Sea \\( n=\overline{abcd} \\) el aforo del auditorio. Se cumple que \\( \overline{acbd} \\) y \\( \overline{adcb} \\) son múltiplos de 11, es decir:

$$
\begin{align*}
  a+b-c-d&\equiv 0 \mod{11}\wedge a+c-b-d\equiv 0 \mod{11}\\
\implies 2(a-d)&\equiv 0 \mod{11}\\
a-d&\equiv 0 \mod{11}
\end{align*}
$$
{:.math .grid}

Dado que \\( a \\) y \\( d \\) son cifras, y su diferencia es múltiplo de 11, la única posibilidad es \\( a=d \\).

Retomando las congruencias:

$$
\begin{align*}
  a+b-c-d&\equiv 0 \mod{11}\\
\implies b-c&\equiv 0 \mod{11}\\
\implies b&= c
\end{align*}
$$
{:.math .grid}

Es decir, \\( n=\overline{abba} \\). Como \\( b \\) debe ser par para que \\( \overline{abab} \\) sea múltiplo de 2, y \\( a\ne 0 \\) para que la primera cifra no sea nula, el número de posibles valores de \\( n \\) es 9\\( \times \\)5=45.


### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">2A-10 3A-9</span>

¿Cuál es el residuo que se obtiene cuando 

$$ \binom{15}{0}^2+\binom{15}{1}^2+\dots+\binom{15}{15}^2 $$
{:.math .grid}

es dividido por 100?

>**a.** 10&#8195;
>**b.** 20&#8195;
>**c.** 30&#8195;
>**d.** 40&#8195;
>**d.** Ninguna de las anteriores.&#8195;

#### Solución
{:.no_toc}

Se tiene que

$$ \binom{15}{0}^2 + \binom{15}{1}^2 + \dots + \binom{15}{15}^2 = \binom{30}{15} $$
{:.math .grid}

Desarrollando \\( \binom{30}{15}\\):

$$ \binom{30}{15} = \frac{ 30\cdot 29\ldots\cdot 17 \cdot 16}{15 \cdot 14\cdot \ldots \cdot 9 \cdot 8 \cdot 7!}$$
{:.math .grid}

En el denominador, todos los factores (excepto \\( 7! \\)) pueden ser cancelados con su doble en el numerador. Así, la expresión se reduciría sistemáticamente:

$$
\begin{align*}
  \binom{30}{15} &= \frac{2^8 \cdot 29 \cdot 27 \cdot 25 \cdot 23 \cdot21 \cdot 19 \cdot 17}{7\cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot2}\\[0.5em]
  &=2^4 \cdot 29 \cdot 9 \cdot 5 \cdot 23 \cdot 19 \cdot 17\\
  &=10 \cdot 2^3 \cdot 29 \cdot 9 \cdot 23 \cdot 19 \cdot 17
\end{align*}
$$
{:.math .grid}

Dado que al tener un factor 10, la última cifra será igual a 0, sólo basta con encontrar la cifra de las decenas, la cual será el residuo de todos los demás factores en módulo 10:

$$
\begin{align*}
  2^3 (29 \cdot 9) [ 23 \cdot 19 \cdot 17]&\equiv 8 (1) [-1] \mod{10}\\
  &\equiv 2 \mod{10}
\end{align*}
$$
{:.math .grid}

Concluimos que:

$$ 
\binom{30}{15} \equiv 20 \mod{100}
$$
{:.math .grid}

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">3A-8</span>

Encuentra la suma de todos los valores positivos de \\( n \\) tales que:

$$
n^2 + 2 | n^6 + 206
$$
{:.math .grid}

>**a.** 28&#8195;
>**b.** 29&#8195;
>**c.** 30&#8195;
>**d.** 31&#8195;
>**e.** Ninguna de las anteriores.

#### Solución
{:.no_toc}

Como \\( n^6+8 = (n^2+2)(n^4-2n^2+4) \\), se tiene que \\( n^2+2 &#124; 198 \\). 

Esto quiere decir que \\( n^2+2 \\) es un divisor (positivo) de 198. Para resumir, los únicos divisores \\( d \\) que satisfacen \\( n^2+2=d \\), con n un número entero, son 3,6,11,18,66 y 198. En cada caso, \\( n \\) adquiere los valores 1,2,3,4,8 y 14. Entonces, la suma de todos los valores posibles de 1+2+3+4+8+14=32.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">3A-11</span>

Encuentra la suma

$$
\begin{array}{c}
\phantom{+}\frac{1}{\sqrt[3]{1}+\sqrt[3]{2}+\sqrt[3]{4}}\\
+\;\;\frac{1}{\sqrt[3]{4}+\sqrt[3]{6}+\sqrt[3]{9}}\\
+\frac{1}{\sqrt[3]{9}+\sqrt[3]{12}+\sqrt[3]{16}}\\
\phantom{+}\vdots\\
+\frac{1}{\sqrt[3]{2019^2}+\sqrt[3]{2019\left(2020\right)}+\sqrt[3]{2020^2}}
\end{array}
$$
{:.math .grid}

>**a.** \\( \sqrt[3]{2020}-\sqrt[3]{2019} \\)&#8195;
>**b.** \\( \sqrt[3]{2019}-1 \\)&#8195;
>**c.** \\( \sqrt[3]{2019}+1 \\)&#8195;
>**d.** \\( \sqrt[3]{2020}-1 \\)&#8195;
>**e.** \\( \sqrt[3]{2020}+1 \\)&#8195;

#### Solución
{:.no_toc}

Para ello, es necesario recordar que \\( (a-b)(a^2+ab+b^2)=a^3-b^3 \\). Así, podemos racionalizar los denominadores de cada término de la siguiente manera:

$$
\begin{array}{c}
\phantom{+}\frac{\sqrt[3]{1}-\sqrt[3]{2}}{\left(\sqrt[3]{1}-\sqrt[3]{2}\right)\left(\sqrt[3]{1}+\sqrt[3]{2}+\sqrt[3]{4}\right)}\\
+\;\;\frac{\sqrt[3]{2}-\sqrt[3]{3}}{\left(\sqrt[3]{2}-\sqrt[3]{3}\right)\left(\sqrt[3]{4}+\sqrt[3]{6}+\sqrt[3]{9}\right)}\\
\phantom{+}\vdots\\
+\frac{\sqrt[3]{2019}-\sqrt[3]{2020}}{\left(\sqrt[3]{2019}-\sqrt[3]{2020}\right)\left(\sqrt[3]{2019^2}+\sqrt[3]{2019\left(2020\right)}+\sqrt[3]{2020^2}\right)}
\end{array}
$$
{:.math .grid}

Que es igual a:

$$
\frac{\sqrt[3]{1}-\sqrt[3]{2}}{-1}+\frac{\sqrt[3]{2}-\sqrt[3]{3}}{-1}+\cdots+\frac{\sqrt[3]{2019}-\sqrt[3]{2020}}{-1}
$$
{:.math .grid}

Asignando el signo a cada término para no expresarlo con denominador, tenemos la siguiente suma

$$
-\sqrt[3]{1}+\sqrt[3]{2}-\sqrt[3]{2}+\sqrt[3]{3}-\cdots-\sqrt[3]{2019}+\sqrt[3]{2020}
$$
{:.math .grid}

Cuyo valor es claramente \\( \sqrt[3]{2020}-1 \\)

<div> </div>
{:.salto .no-mostrar}

# Problemas demostrativos (o parte B)

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">2B-1</span>

Sobre los lados \\( AB \\) y \\( BC \\) del cuadrado \\( ABCD \\) se encuentran los puntos \\( E \\) y \\( F \\), respectivamente, de manera que \\( BE=BF \\). Sea \\( P \\) el pie de la altura del triángulo \\( BCE \\) por \\( B \\). Demuestra que \\( \angle FPD=90^\circ \\).

#### Solución
{:.no_toc}

Sea \\( \angle PEF=\alpha\\). Se tiene que:

$$
\begin{align*}
  \angle PEF&= 45^\circ-\angle FCE\\
  &=45^\circ-(90^\circ-\angle PBC)\\
  &=-45^\circ+(\angle PBD + 45^\circ)\\
  &=\angle PBD
\end{align*}
$$
{:.math .grid}

Además, \\(\angle EBC=\angle EPB=90^\circ \implies \\triangle EPB\cong\triangle EBC\\), por lo que las siguientes igualdades se cumplen (al final, se aplica el Teorema de Pitágoras en \\( \triangle BCD \\) y \\( \triangle EBF \\)):

$$
\begin{align*}
  \frac{EP}{EB}&= \frac{PB}{BC}\\[0.5em]
  \implies\frac{EP}{PB}&= \frac{EB}{BC}\\[0.5em]
  &= \frac{EB\sqrt{2}}{CD\sqrt{2}}\\[0.5em]
  &= \frac{EF}{BD}
\end{align*}
$$
{:.math .grid}

Como \\( \angle PEF=\angle PBD \\) y \\( \frac{EP}{PB}=\frac{EF}{BD} \\), por criterio **LAL** \\( \triangle EPF\cong \triangle PBD \\). 

<div class="geo-100"><div id="ProblemaCuadradoLALSolucion1"></div></div>

Esto significa que:

$$
\begin{align*}
  \angle EPF&= \angle BPD\\
  \angle EPB+\angle BPF&= \angle BPF+\angle FPD\\
  \implies \angle FPD&= \angle EPB\\
  &=90^\circ
\end{align*}
$$
{:.math .grid}

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">2B-3 3B-1</span>

Encuentra las soluciones reales de la ecuación:

$$(x+2010)^4+(x+2030)^4=22408$$
{:.math .grid}

#### Solución
{:.no_toc}

Sea \\( y=x+2020 \\). La ecuación puede reescribirse como:

$$
\begin{align*}
(y-10)^4+(y+10)^4&=22408\\
2y^4+12y^2\cdot 10^2+2\cdot10^4&=22408\\
y^4+600y^2+10^4&=11204\\
\implies y^4+600y^2-1204&=0\\
\end{align*}
$$
{:.math .grid}

Si \\( a=y^2 \\), la ecuación cuadrática se resuelve:

$$
\begin{align*}
a&=\frac{-600\pm\sqrt{600^2-4(1)(1204)}}{2}\\
&=\frac{-600\pm\sqrt{360000+4816}}{2}\\
&=\frac{-600\pm\sqrt{604^2}}{2}\\
&=\frac{-600\pm604}{2}\\
a_1&=2\\
a_2&=-1204\\
\end{align*}
$$
{:.math .grid}

Dado que \\( y\in\mathbb{R}\implies y^2>0 \\), \\( a_1 \\) es la única solución válida. Luego \\( y=\pm 2 \\) y los únicos valores reales de \\( x \\) son

$$
\begin{align*}
x&=\left\{\begin{array}{l}
+\sqrt{2}-2020\\
-\sqrt{2}-2020
\end{array}\right.
\end{align*}
$$
{:.math .grid}

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">2B-2 3B-2</span>

Sean \\( a \\) y \\( b \\) dos enteros tales que \\( a>b>0 \\). Si \\( ab-1 \\) y \\( a+b \\) son primos relativos, y también \\( ab+1 \\) y \\( a-b \\), demuestra que

$$
(ab+1)^2+(a-b)^2
$$

no es un cuadrado perfecto.

#### Solución
{:.no_toc}

Supongamos que \\( (ab + 1)^2 + (a − b)^2  = c^2 \\)para algún entero c. Entonces,

$$
c^2 = a^2b^2 + a^2 + b^2 + 1 = (a^2 + 1)(b^2 + 1).
$$
{:.math .grid}

Demostraremos que \\( a^2 + 1 \\) y \\( b^2 + 1 \\) son primos relativos. Supongamos lo contrario y
sea \\( p \\) un número primo tal que \\( p | a^2 + 1\\) y \\( p | b^2 + 1 \\). Entonces \\( p | a^2 − b^2\\) y de aquí, \\( p | a − b \\) o \\( p | a + b \\).

Si \\(p | a−b\\), entonces \\( p | ab−b^2 \\) y como \\( p | b^2+1\\) se sigue que \\( p | ab+1\\), lo que
es una contradicción ya que \\( ab + 1 \\) y \\( a − b \\) son primos relativos. De manera análoga,
si \\( p | a + b \\) entonces \\(p | ab − 1 \\), que es una contradicción. Por lo tanto, \\( a^2 + 1 \\) y
\\( b^2 +1 \\) son primos relativos y su producto es un cuadrado. De aquí, \\( a^2 +1\\) y \\( b^2 +1 \\) son ambos cuadrados, lo cual no puede ser ya que \\(a^2+1 = m^2 \implies 1 = (m−a)(m+a)\\) \\(\implies \\)
\\( m− a = \pm 1\\) y \\( m+ a = \pm 1\\) \\(\implies\\) \\( a = 0\\). De manera análoga, \\( b^2 + 1 = k^2 \implies b = 0\\).
Por lo tanto, \\( (ab + 1)^2 + (a − b)^2 \\) no es un cuadrado.

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">3B-3</span>

Considera todas las ternas \\( (x,y,p) \\) de enteros positivos donde \\( p \\) es un número primo, tales que:

$$
4x^2+8y^2+(2x-3y)p-12xy=0
$$
{:.math .grid}

Demuestra que \\( 4y+1 \\) es un cuadrado perfecto para cada terna \\( (x,y,p) \\).

#### Solución
{:.no_toc}

Reescribimos la ecuación cuadrática respecto a \\( x \\) de la siguiente manera:

$$
4x^2+(2p-12y)x+8y^2-3yp=0
$$
{:.math .grid}

El discriminante de dicha ecuación es

$$
(2p-12y)^2-4(4)(8y^2-3yp)=16y^2+4p^2
$$
{:.math .grid}

Si \\( x \\) es un entero positivo, \\( 16y^2+4p^2\\) es un cuadrado perfecto par. Es decir:

$$
k^2=16y^2+4p^2 \implies (k+4y)(k-4y)=4p^2
$$
{:.math .grid}

Para algún entero \\( k \\) divisible por 2.

Tenemos dos factores pares en el lado derecho de la implicación porque \\( k \\) es par, lo que presenta dos casos, donde \\( k+4y \\) y \\( k-4y \\) son divisores pares de \\( 4p^2 \\):

1. \\(k+4y=2p^2>k-4y=2\\).
    
   La diferencia entre los factores es \\( (k+4y)-(k-4y)=2p^2-2\\).

   Finalmente \\( 4y+1=p^2\\).

2. \\(k+4y=k-4y=2p\\).
   
   Este caso es imposible porque \\( y \\) es un entero positivo.

Sólo es necesario aclarar que ambos casos pueden ser aplicados si \\( p=2 \\) para finalizar.

<script type="text/javascript">
				function perspective(p){
					updateHelp(p);
					ggbApplet.setPerspective(p);
				}
                var parametersRectangulos = {
                        "id":"ProblemaRectangulos",
                        "material_id":"kvkua2qu",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-100",
                        "allowUpscale":true
                        };
                        var parametersOchos = {
                        "id":"ProblemaOchos",
                        "material_id":"cr2hdcbk",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-100",
                        "allowUpscale":true
                        };
                        var parametersOchosSolucionRotacion = {
                        "id":"ProblemaOchosSolucionRotacion",
                        "material_id":"mmt96y8v",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-100",
                        "allowUpscale":true
                        };
                        var parametersCuadradoLALSolucion = {
                        "id":"ProblemaCuadradoLALSolucion",
                        "material_id":"fb7bkr93",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-100",
                        "allowUpscale":true
                        };
                        var parameters43GradosSolucion = {
                        "id":"Problema43GradosSolucion",
                        "material_id":"u85bzqms",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-100",
                        "allowUpscale":true
                        };
                        var parametersRectangulosSolucion= {
                        "id":"ProblemaRectangulosSolucion",
                        "material_id":"s9gnjwan",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-100",
                        "allowUpscale":true
                        };
                var appletRectangulos = new GGBApplet(parametersRectangulos, '5.0', 'ProblemaRectangulos');
                var appletOchos = new GGBApplet(parametersOchos, '5.0', 'ProblemaOchos');
                var appletOchosSolucionRotacion = new GGBApplet(parametersOchosSolucionRotacion, '5.0',
                 'ProblemaOchosSolucionRotacion');
                 var appletCuadradoLALSolucion = new GGBApplet(parametersCuadradoLALSolucion, '5.0',
                 'ProblemaCuadradoLALSolucion');
                 var applet43GradosSolucion = new GGBApplet(parameters43GradosSolucion, '5.0', 'Problema43GradosSolucion');
                 var appletRectangulosSolucion = new GGBApplet(parametersRectangulosSolucion, '5.0', 'ProblemaRectangulosSolucion');
                window.onload = function() { 
                  appletRectangulos.inject('ProblemaRectangulos1');
                appletOchos.inject('ProblemaOchos1');
                appletOchos.inject('ProblemaOchos2');
                appletOchos.inject('ProblemaOchos3');
                appletOchosSolucionRotacion.inject('ProblemaOchosSolucionRotacion1');
                appletCuadradoLALSolucion.inject('ProblemaCuadradoLALSolucion1');
                applet43GradosSolucion.inject('Problema43GradosSolucion1');
                appletRectangulosSolucion.inject('ProblemaRectangulosSolucion1');
                }
</script>