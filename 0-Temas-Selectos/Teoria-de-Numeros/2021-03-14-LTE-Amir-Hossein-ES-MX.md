---
layout: default
search_exclude: true
tema: Arcoiris
tema_oscuro: ArcoirisOscuro
title: LTE por Amir Hossein
nav_order: 2021-03-14
description: "Lema Lifting the Exponent."
last_modified_date: 2021-03-14T15:14:15+9265
parent: Teoría de Números
grand_parent: Temas Selectos
---
<!--
1. [<span>Definitions and Notation</span>{:.deg-sitio-1 .deg-sitio-texto}](#definiciones-y-notacion)
2. [<span>Two Important and Useful Lemmas</span>{:.deg-sitio-2 .deg-sitio-texto}](#dos-lemas-utiles-e-importantes)
   1. [<span>Lemma 1</span>{:.deg-sitio-3 .deg-sitio-texto}](#lema1)
   2. [<span>Lemma 2</span>{:.deg-sitio-4 .deg-sitio-texto}](#lema2)
3. [<span>Lifting The Exponent Lemma (LTE)</span>{:.deg-sitio-5 .deg-sitio-texto}](#lifting-the-exponentlemma-lte)
   1. [<span>Theorem 1 First Form of LTE</span>{:.deg-sitio-6 .deg-sitio-texto}](#teorema1primera-forma-de-lte)
   2. [<span>Theorem 2 Second Form of LTE</span>{:.deg-sitio-7 .deg-sitio-texto}](#teorema1segunda-forma-de-lte)
4. [<span>What about&nbsp;<span>\\(p=2\\)</span>?</span>{:.deg-sitio-8 .deg-sitio-texto}](#que-pasa-si-p2)
   1. [<span>Theorem 3 LTE for the case&nbsp;<span>\\(p=2\\)</span></span>{:.deg-sitio-9 .deg-sitio-texto}](#teorema3lte-para-el-caso-p2)
   2. [<span>Theorem 4</span>{:.deg-sitio-10 .deg-sitio-texto}](#teorema4)
5. [<span>Summary</span>{:.deg-sitio-11 .deg-sitio-texto}](#resumen)
6. [<span>Problems with solutions</span>{:.deg-sitio-12 .deg-sitio-texto}](#problemas-con-soluciones)
   1. [<span>Problem 1 Russia 1996</span>{:.deg-sitio-11 .deg-sitio-texto}](#problema1rusia-1996)
   2. [<span>Problem 2 Balkan 1993</span>{:.deg-sitio-10 .deg-sitio-texto}](#problem2balcanes-1993)
   3. [<span>Problem 3</span>{:.deg-sitio-9 .deg-sitio-texto}](#problema3)
   4. [<span>Problem 4</span>{:.deg-sitio-8 .deg-sitio-texto}](#problema4)
7. [<span>Challenge Problems</span>{:.deg-sitio-7 .deg-sitio-texto}](#problemas-desafiantes)
8. [<span>Hints and Answers to Selected Problems</span>{:.deg-sitio-6 .deg-sitio-texto}](#algunas-pistas-y-soluciones-a-los-problemas-desafiantes)
9. [<span>Original sources</span>{:.deg-sitio-5 .deg-sitio-texto}](#fuentes-originales)
10. [<span>References</span>{:.deg-sitio-4 .deg-sitio-texto}](#referencias)

<div> </div>
{:.salto .no-mostrar}

&#x2060;<span>$$a_nx^n+\cdots+a_0$$</span>{:.math .deg-sitio-1 .deg-sitio .deg-sitio-texto}

&#x2060;<span>\\(\ldots\\)</span>{:.math .deg-sitio-1 .deg-sitio .deg-sitio-texto .fs-6}

&#x2060;<span>\\(-\ldots\\)</span>{:.math .deg-sitio-1 .deg-sitio .deg-sitio-texto .fs-2}-->

# Lifting The Exponent Lemma<br><span>(LTE)</span>{:.deg-sitio .deg-sitio-texto .deg-sitio-2}
{:.no_toc}

Amir Hossein Parvardi
{:.fs-6 .fw-300}

**Versión&nbsp;<span>6</span>{:.deg-sitio-3 .deg-sitio-texto} Traducción al español**<br/>
14 de marzo de 2021

El lema *Lifting The Exponent* es una técnica poderosa para resolver ecuaciones diofantinas exponenciales. Es popular en el *folclor* olímpico (ver **Referencia&nbsp;[<span>3</span>{:.deg-sitio-4 .deg-sitio-texto}](#referencias)**) considerando que sus orígenes son difíciles de trazar. Matemáticamente, está íntimamente relacionado con el clásico Lema de Hensel (ver **Referencia&nbsp;[<span>2</span>{:.deg-sitio-5 .deg-sitio-texto}](#referencias)**) en Teoría de Números (tanto en el enunciado como en la idea tras su demostración). En este artículo analizaremos esta técnica y presentaremos algunas de sus aplicaciones.

Podemos utilizar el lema *Lifting The Exponent* (es un nombre largo... ¡sólo llámalo **LTE**!) en una gran cantidad de problemas que involucren ecuaciones exponenciales, especialmente cuando están relacionadas con números primos (en algunos casos, el problema “sale” inmediatamente). El lema indica cómo encontrar la mayor potencia de un número primo \\(p\\) —usualmente \\(\ge 3\\)— que divide a \\(a^n+b^n\\), para algunos enteros positivos \\(a\\) y \\(b\\). Las demostraciones de los teoremas y lemas en en este artículo no son demasiado complejas y todas ellas usan matemáticas elementales. Entender el significado y la forma de aplicar cada teorema es más importante para ti que recordar detalladamente su demostración.

Agradezco a Fedja, darij grinberg (Darij Grinberg), makar y ZetaX (Daniel) por sus comentarios sobre mi artículo. De manera especial, aprecio la ayuda de JBL (Joel) y Fedja con los inconvenientes de \\(\TeX\\).


## Definiciones y notación

Dados dos enteros \\(a\\) y \\(b\\), decimos que  \\(a\\) es divisible por \\(b\\) y escribimos \\(b\|a\\) sí y sólo sí existe un entero \\(q\\) tal que \\(a=qb\\).

Definimos \\(v_p(x)\\) como la máxima potencia de un número primo \\(p\\) que divide a \\(x\\); es decir, si \\(v_p(x)=\alpha\\) entonces \\(p^\alpha\|x\\) y \\(p^{\alpha+1}\nmid x\\). Escribimos \\(p^\alpha \\\|x\\), sí y sólo sí \\(v_p(x)=\alpha\\). Es fácil notar que \\(v_p(xy)=v_p(x)+v_p(y)\\) y \\(v_p(x+y)\ge\\) \\(\text{min}\\{v_p(x), v_p(y)\\}\\).

#### Ejemplo
{:.no_toc}

La mayor potencia de \\(3\\) que divide a \\(63\\) es \\(3^2\\), dado que \\(3^2=9\|63\\) y \\(3^3=27\nmid 63\\). Utilizando la notación descrita anteriormente, \\(3^2\\\|63\\) o \\(v_3(63)=2\\).

#### Ejemplo
{:.no_toc}

Es claro que si \\(p\\) y \\(q\\) son dos números primos distintos, entonces \\(v_p(p^\alpha q^\beta)=\alpha\\), lo cual es equivalente a \\(p^\alpha\\\|p^\alpha q^\beta\\).

**Nota**: Se tiene que \\(v_p(0)=\infty\\) para todos los números primos \\(p\\).

<div> </div>
{:.salto .no-mostrar}

## Dos lemas útiles e importantes

### Lema&nbsp;<span>1</span>{:.deg-sitio-6 .deg-sitio-texto}
Sean \\(x\\) y \\(y\\) dos enteros (no necesariamente positivos), y sea \\(n\\) un número natural. Para cualquier número primo \\(p\\) tal que \\(\text{MCD}(n,p)=1\\), \\(p\|x−y\\) y \\(x\\) y \\(y\\) no son divisibles por \\(p\\) (es decir, \\(p\nmid x\\) y \\(p\nmid y\\)), se cumple que

$$v_p(x^n−y^n)=v_p(x−y).$$
{:.math}

#### Demostración
{:.no_toc}

Podemos utilizar la siguiente propiedad

$$x^n−y^n=(x−y)\left(x^{n−1}+x^{n−2}y+x^{n−3}
y^2+\cdots+y^{n−1}\right).$$
{:.math}

Si se demuestra que \\(p\nmid x^{n−1}+x^{n−2}y\,+\\) \\(x^{n−3}y^2+\cdots+y^{n−1}\\), se concluye inmediatamente.

Para ello, se utiliza la condición \\(p\|x−y\\). Entonces \\(x−y\equiv 0\mod p\\),  lo cual es equivalente a \\(x\equiv y\mod p\\). Luego

$$\begin{align*}
x^{n−1}&+x^{n−2}y+x^{n−3}y^2+\cdots+y^{n−1}\\
&\equiv x^{n−1}+x^{n−2}\cdot x+x^{n−3}\cdot x^2+\cdots+x\cdot x^{n−2}+x^{n−1}\\
&\equiv nx^{n−1}\\
&\not\equiv 0\mod p.
\end{align*}$$
{:.math}

lo que completa la demostración.

### Lema&nbsp;<span>2</span>{:.deg-sitio-7 .deg-sitio-texto} 
Sean \\(x\\) y \\(y\\) dos enteros y \\(n\\) un número natural impar. Para cualquier número primo \\(p\\) tal que \\(\text{MCD}(n,p)=1\\), \\(p\|x+y\\) y \\(x\\) y \\(y\\) no son divisibles por \\(p\\), se cumple que

$$v_p(x^n+y^n)=v_p(x+y).$$
{:.math}

#### Demostración
{:.no_toc}

Como \\(x\\) y \\(y\\) pueden ser negativos, aplicando el **Lema [<span>1</span>{:.deg-sitio-8 .deg-sitio-texto}](#lema1)** se obtiene que

$$v_p(x^n−(−y)^n)=v_p(x−(−y))\implies v_p(x^n+y^n)=v_p(x+y).$$
{:.math}

Nótese que \\(n\\) es un número natural impar, por lo que se puede reemplazar \\((−y)^n\\) con \\(−y^n\\).

<div> </div>
{:.salto .no-mostrar}

## Lema&nbsp;<span>Lifting The Exponent</span>{:.deg-sitio-9 .deg-sitio-texto} (LTE)

### Teorema&nbsp;<span>1</span>{:.deg-sitio-10 .deg-sitio-texto}&nbsp;Primera forma de LTE
Sean \\(x\\) y \\(y\\) dos enteros, \\(n\\) un número natural, y \\(p\\) número primo impar tal que \\(p\|x−y\\) y  \\(x\\) y \\(y\\) no son divisibles por \\(p\\) (es decir, \\(p\nmid x\\) y \\(p\nmid y\\)), se cumple que

$$v_p(x^n−y^n)=v_p(x−y)+v_p(n).$$
{:.math}

#### Demostración
{:.no_toc}

Se puede utilizar inducción sobre \\(v_p(n)\\). Primero, probaremos la siguiente igualdad:

$$v_p(x^p−y^{\,p})=v_p(x−y)+1. \tag{1}\label{eq:1}$$
{:.math}

Para ello, se demostrará que

$$p | x^{p−1}+x^{p−2}y+\cdots+xy^{\,p−2}+y^{\,p−1}\;\tag{2}\label{eq:2}$$
{:.math}

y

$$p^2\nmid x^{p−1}+x^{p−2}y+\cdots+xy^{p−2}+y^{\,p−1}.\;\tag{3}\label{eq:3}$$
{:.math}

Para verificar \\(\style{color:#5c5962;}{\eqref{eq:2}}\\), se tiene que

$$x^{p−1}+x^{p−2}y+\cdots+xy^{\,p−2}+y^{\,p−1}\equiv px^{p−1}\equiv 0\mod  p.$$
{:.math}

Sea \\(y=x+kp\\), con \\(k\\) entero. Para algún entero \\(t\\) tal que \\(1\le t< p\\) se cumple que

$$
\begin{align*}
y^{t}x^{p−1−t}&\equiv(x+kp)^{t}x^{p−1−t}\\
&\equiv x^{p−1−t}\left(x^t+t(kp)\left(x^{t−1}\right)+\frac{t(t-1)}{2}(kp)^2\left(x^{t−2}\right)+\cdots\right)\\
&\equiv x^{p−1−t}\left(x^t+t(kp)\left(x^{t-1}\right)\right) \\
&\equiv x^{p-1}+tkpx^{p-2}\mod  p^2
\end{align*}
$$
{:.math}

lo que implica

$$y^tx^{p−1−t}\equiv x^{p−1}+tkpx^{p−2}\mod  p^2,\;\;t=1, 2,3,4,\ldots,p−1.$$
{:.math}

Utilizando dicha propiedad, se tiene que

$$
\begin{align*}
x^{p−1}&+x^{p−2}y+\cdots+xy^{p−2}+y^{p−1}\\
&\equiv x^{p−1}+(x^{p−1}+kpx^{p−2})+(x^{p−1}+2kpx^{p−2})+\cdots+(x^{p−1}+(p-1)kpx^{p−2})\\
&\equiv px^{p−1}+(1+2+\cdots+p-1)kpx^{p−2}\\[0.5em]
&\equiv px^{p−1}+\frac{p(p-1)}{2}kpx^{p−2}\\[0.5em]
&\equiv px^{p−1}+\frac{p-1}{2}kp^2x^{p−1}\\[0.5em]
&\equiv px^{p−1}\\
&\not\equiv 0\mod  p^2.\\
\end{align*}
$$
{:.math}

Hasta ahora se ha demostrado \\(\style{color:#5c5962;}{\eqref{eq:3}}\\) y \\(\style{color:#5c5962;}{\eqref{eq:1}}\\). Volvamos al enunciado inicial. Se quiere demostrar que

$$v_p(x^n−y^n)=v_p(x−y)+v_p(n).$$
{:.math}

Supóngase que \\(n=p^\alpha b\\), de manera que \\(\text{MCD}(p,b)=1\\). entonces

$$
\begin{align*}
v_p(x^n−y^n)&=v_p\left(\left(x^{p^\alpha}\right)^b−\left(y^{\,p^\alpha}\right)^b\right)\\
&=v_p\left(x^{p^\alpha}−y^{\,p^\alpha}\right)=v_p\left(\left(x^{p^{\alpha-1}}\right)^p−\left(y^{\,p^{\alpha-1}}\right)^p\right)\\
&=v_p\left(x^{p^{\alpha-1}}−y^{\,p^{\alpha-1}}\right)+1=v_p\left(\left(x^{p^{\alpha-2}}\right)^p−\left(y^{\,p^{\alpha-2}}\right)^p\right)+1\\
&=v_p\left(x^{p^{\alpha-2}}−y^{\,p^{\alpha−2}}\right)+2\\
&\:\;\vdots\\
&=v_p\left(x^{p^1}−y^{\,p^1}\right)+\alpha−1=v_p(x-y)+\alpha\\
&=v_p(x-y)+v_p(n).
\end{align*}
$$
{:.math}

Nótese que se ha utilizado la siguiente propiedad: si \\(p\|x−y\\), entonces \\(p\|x^k−y^k\\), dado que \\(x−y\|x^k−y^k\\) para todo entero positivo \\(k\\). La demostración está hecha.

<div> </div>
{:.salto .no-mostrar}

### Teorema&nbsp;<span>2</span>{:.deg-sitio-11 .deg-sitio-texto}&nbsp;Segunda forma de LTE 
Sean \\(x\\), \\(y\\) dos enteros, \\(n\\) un número natural, y \\(p\\) un número primo impar tal que \\(p\|x+y\\) y \\(x\\) y \\(y\\) no son divisibles por \\(p\\). Se cumple que:

$$v_p(x^n+y^n)=v_p(x+y)+v_p(n).$$
{:.math}

#### Demostración
{:.no_toc}

Es claro aplicando el **Teorema&nbsp;[<span>1</span>{:.deg-sitio-12 .deg-sitio-texto}](#teorema1primera-forma-de-lte)**, con el truco utilizado en la demostración del **Lema&nbsp;[<span>2</span>{:.deg-sitio-11 .deg-sitio-texto}](#lema2)**.

<div> </div>
{:.salto .no-mostrar}

## ¿Qué pasa si \\(p=2\\)?

>**Pregunta:** ¿Por qué se ha asumido que \\(p\\) es un número primo impar, es decir, \\(p\ne 2\\)? ¿Por qué no se puede suponer que \\(p=2\\) en las demostraciones anteriores?
>
>**Pista:** \\(\frac{p−1}{2}\\) es un entero sólo cuando \\(p>2\\).

### Teorema&nbsp;<span>3</span>{:.deg-sitio-10 .deg-sitio-texto}&nbsp;LTE para el caso \\(p=2\\)
Sean \\(x\\) y \\(y\\) enteros impares tales que \\(4\| x−y\\). Entonces

$$v_2\left(x^n−y^n\right)=v_2(x−y)+v_2(n).$$
{:.math}

#### Demostración
{:.no_toc}

Se ha demostrado que para todo número primo \\(p\\) tal que \\(\text{MCD}(p,n)= 1\\), \\(p\|x−y\\) y \\(x\\) y \\(y\\) no son divisibles por \\(p\\), se cumple que

$$v_p(x^n-y^n)=v_p(x−y)$$
{:.math}

Sea \\(m\\) un entero impar y \\(k\\) un número natural tal que \\(n=m\cdot2^k\\). Entonces, basta con demostrar que

$$v_2\left(x^{2^k}−y^{2^k}\right) =v_2(x−y)+k.$$
{:.math}

Se puede factorizar de la siguiente manera:

$$x^{2^k}−y^{2^k}=\left(x^{2^{k−1}}+ y^{2^{k−1}}\right)\left(x^{2^{k−2}}+ y^{2^{k−2}}\right)\cdots(x^2+y^2)(x+y)(x-y)$$
{:.math}

Como \\(x\equiv y\equiv\pm 1\mod 4\\) se tiene que \\(x^{2^i}\equiv\\) \\(y^{2^i}\equiv 1\mod 4\\) para cualquier entero positivo \\(i\\), entonces \\(x^{2^i}+y^{2^i}\equiv 2\mod 4,\\) para \\(i=1,2,3,\ldots\\) Además, dado que \\(x\\) y \\(y\\) son impares  y \\(4\|x−y\\), se deduce que \\(x+y\equiv 2\mod 4\\). Es decir, la potencia de \\(2\\) en cada factor del producto anterior (excepto \\(x−y\\)) es \\(2^1\\), lo que concluyte la demostración.

### Teorema&nbsp;<span>4</span>{:.deg-sitio-9 .deg-sitio-texto}
Sean \\(x\\) y \\(y\\) dos enteros impares y sea \\(n\\) un número natural par. Se cumple que

$$v_2(x^n−y^n)=v_2(x−y)+v_2(x+y)+v_2(n)−1.$$
{:.math}

<div> </div>
{:.salto .no-mostrar}

#### Demostración
{:.no_toc}
El cuadrado de un entero impar siempre es de la forma \\(4k+1\\). Entonces, en el caso de  \\(x\\) y \\(y\\), \\(4\|x^2−y^2\\). Sea \\(m\\) un entero impar y \\(k\\) un número natural tal que \\(n=m\cdot2^k\\). Entonces

$$\begin{align*}
v_2(x^n−y^n)&=v_2\left(x^{m\cdot2^k}−y^{m\cdot2^k}\right)\\
&=v_2\left(\left(x^2\right)^{2^{k−1}}−\left(y^2\right)^{2^{k−1}}\right)\\
&\;\;\vdots\\
&=v_2\left(x^2−y^2\right)+k−1\\
&=v_2(x−y)+v_2(x+y)+v_2(n)−1.
\end{align*}$$
{:.math}

<div> </div>
{:.salto .no-mostrar}

## Resumen

Sea \\(p\\) un número primo  y sean \\(x\\) y \\(y\\) dos enteros (no necesariamente positivos) no divisibles por \\(p\\). Entonces:

>**a.** Para cualquier número natural \\(n\\)

>* si \\(p\ne 2\\) y \\(p\|x−y\\), entonces

$$v_p(x^n−y^n)=v_p(x−y)+v_p(n).$${:.math}

>* si \\(p=2\\) y \\(4\|x−y\\), se cumple que

$$v_2(x^n−y^n)=v_2(x−y)+v_2(n).$${:.math}

>* si \\(p=2\\), \\(n\\) es par, y \\(2\|x−y\\), se tiene que

$$v_2(x^n−y^n)=v_2(x-y)+v_2(x+y)+v_2(n)−1.$${:.math}

>**b.** Para cualquier número natural impar \\(n\\), si \\(p\|x+y\\), entonces

$$v_p(x^n+y^n)=v_p(x+y)+v_p(n).$${:.math}

>**c.** Para todo número natural \\(n\\) tal que \\(\text{MCD}(p,n)=1\\), si \\(p\|x−y\\), entonces

$$v_p(x^n-y^n)=v_p(x-y).$${:.math}

>Si \\(n\\) es impar, \\(\text{MCD}(p,n)=1\\), y \\(p\|x+y\\), se cumple que

$$v_p(x^n+y^n)=v_p(x+y).$${:.math}

**Nota:** El error más común al aplicar **LTE** es no verificar la condición \\(p\|x\pm y\\), así que... ¡Recuerda revisarla siempre! De no hacerlo, tu solución será errónea.

<div> </div>
{:.salto .no-mostrar}

## Problemas con soluciones

### Problema&nbsp;<span>1</span>{:.deg-sitio-1 .deg-sitio-texto}&nbsp;Rusia 1996

Encuentre todos los números naturales \\(n\\) para los cuales existen números naturales \\(x\\), \\(y\\) y \\(k\\) tales que \\(\text{MCD}(x,y)=1\\), \\(k>1\\) y \\(3^n=x^k+y^k\\).

#### Solución
{:.no_toc}

\\(k\\) debe ser un entero impar (pues si \\(k\\) es par, \\(x^k\\) y \\(y^k\\) son cuadrados perfectos, y es fácil verificar que para cualesquiera enteros \\(a\\), \\(b\\) se cumple que \\(3\|a^2+b^2\\) sí y sólo sí \\(3\|a\\) y \\(3\|b\\), lo cual es una contradicción porque \\(\text{MCD}(x,y)=1\\)).

Supóngase que existe un número primo \\(p\\) tal que \\(p\|x+y\\), el cual debe ser impar. Entonces \\(v_p(3^n)=v_p(x^k+y^k)\\), y por el **Teorema&nbsp;[<span>2</span>{:.deg-sitio-3 .deg-sitio-texto}](#teorema2segunda-forma-de-lte)**, \\(v_p(3^n)=\\) \\(v_p(x^k+y^k)=\\) \\(v_p(k)+v_p(x+y)\\). Pero \\(p\|x+y\\) implica \\(v_p(x+y)\ge 1>0\\) y entonces \\(v_p(3^n)=v_p(k)+v_p(x+y)>0\\), por lo que \\(p\|3^n\\). Es decir, \\(p=3\\). Esto significa que \\(x+y=3^m\\) para algún número natural \\(m\\). Nótese que \\(n=v_3(k)+m\\). Se tienen dos casos:

* \\(m>1\\)
  
  Se puede probar por inducción que \\(3^a\ge a+2\\) para todo número natural \\(a\\), lo que implica \\(v_3(k)\le k − 2\\) (¿Por qué?). Sea \\(M=\text{max}(x,y)\\). Dado que \\(x+y=3^m\ge 9\\), se cumple que \\(M\ge 5\\). Luego

  $$\begin{align*}
  M^{k-1}\ge 5^{k-1}&\land M\ge \frac{x+y}{2}=\frac{1}{2}\cdot 3^m\\[1em]
  x^k+y^k&\ge M^k=M\cdot M^{k-1}\\
  &\phantom{\ge}>\frac{1}{2}\cdot 3^m\cdot5^{k-1}\\
  &\phantom{\ge >}>3^m\cdot 5^{k-2}\\
  &\phantom{\ge >>}\ge 3^{m+k-2}\\
  &\phantom{\ge >>\ge}\ge 3^{m+v_3(k)}=3^n
  \end{align*}$$
  {:.math}
  
  lo cual es una contradicción.
* \\(m=1\\)
   
  y \\(x+y=3\\), lo que implica \\(x=1\\) y \\(y=2\\) (o \\(x=2\\) y \\(y=1\\)). Entonces \\(3^{1+v_3(k)}=1+2^k\\). Pero \\(3^{v_3(k)}\|k\\), y por ende \\(3^{v_3(k)}\le k\\). Luego
  
  $$1+2^k=3^{v_3(k)+1}=3\cdot3^{v_3(k)}\le 3k\implies 1+2^k\le 3k$${:.math}
  
  Es posible verificar que el único valor impar de \\(k>1\\) que satisface la desigualdad anterior es \\(k=3\\). Entonces \\((x,y,n,k)=\\) \\((1, 2, 2, 3)\\) o \\((2, 1, 2, 3)\\) en este caso.

Finalmente, la respuesta es \\(n=2\\).

### Problema&nbsp;<span>2</span>{:.deg-sitio-5 .deg-sitio-texto}&nbsp;Balcanes 1993

Sea \\(p\\) un número primo y \\(m>1\\) un número natural. Demuestre que si los números naturales \\(x>1\\) y \\(y>1\\) satisfacen la igualdad

$$\frac{x^p+y^{\,p}}{2}=\left(\frac{x+y}{2}\right)^m,$${:.math}

entonces \\(m=p\\).

#### Solución
{:.no_toc}

Se puede probar con inducción sobre \\(p\\) que \\(\frac{x^p+y^{\\!\\;p}}{2}\ge\left(\frac{x+y}{2}\right)^p\\) para todo número natural \\(p\\). Dado que \\(\frac{x^p+y^{\\!\\;p}}{2}=\left(\frac{x+y}{2}\right)^m\\), se debe cumplir que \\(m\ge p\\). Sea \\(d=\text{MCD}(x,y)\\), entonces existen enteros \\(x_1\\) y \\(y_1\\) tales que \\(\text{CDC}(x_1,y_1)=1\\), \\(x=dx_1\\), \\(y=dy_1\\) y \\(2^{m−1}(x^p_1+y^{\\,p}_1)=d^{m−p}(x_1+y_1)^m\\). Se tienen dos casos:

* \\(p\\) es impar.
  
  Sea \\(q\\) cualquier divisor primo de \\(x_1+y_1\\) y \\(v=v_q(x_1+y_1)\\). Si \\(q\\) es impar, se cumple que \\(v_q(x^{p}_1+y^{\\,p}_1)=v+v_q(p)\\) y \\(v_q(d^{m−p}(x_1+y_1)^m)\ge mv\\) (dado que \\(q\\) puede ser un factor de \\(d\\)). Entonces \\(m\le 2\\) y \\(p\le 2\\), lo cual es una contradicción. Si \\(q=2\\), entonces \\(m-1+v\ge mv\\), por lo que \\(v\le 1\\) y \\(x_1+y_1=2\\), luego \\(x=y\\), y este resultado implica \\(m=p\\).
* \\(p=2\\). 
  
  Si \\(x+y\ge 4\\) se tiene que \\(\frac{x^2+y^2}{2}<\\) \\(2\left(\frac{x+y}{2}\right)^2\le\\) \\(\left(\frac{x+y}{2}\right)^3\\), entonces \\(m=2\\).

### Problema&nbsp;<span>3</span>{:.deg-sitio-7 .deg-sitio-texto} 
Encuentre todos los números naturales \\(a\\), \\(b\\) mayores que \\(1\\) que satisfacen

$$b^a|a^b−1.$${:.math}

#### Solución
{:.no_toc}

Sea \\(p\\) el menor número primo que divide a \\(b\\). Sea \\(m\\) el menor número natural tal que \\(p\|a^m−1\\). Se cumple que \\(m\|b\\) y \\(m\|p−1\\), entonces cualquier número primo que divide a \\(m\\) tamibén divide a \\(b\\) y es menor que \\(p\\). Para evitar una contradicción, \\(m=1\\). Luego, si \\(p\\) es impar, \\(av_p(b)\le v_p(a − 1)+v_p(b)\\), lo que implica \\((a−1)\\) \\(\le (a−1)v_p(b)\\) \\(\le v_p(a−1)\\), lo cual es imposible. Ahora, si \\(p=2\\), \\(b\\) es par, \\(a\\) es impar y \\(av_2(b)\le v_2(a−1)\\,+\\,\\)&#x200B;\\(v_2(a+1)+v_2(b)−1\\) donde \\(a\le\\) \\((a−1)v_2(b)+1\le\\) \\(v_2(a − 1)\\,+\\,\\)&#x200B;\\(v_2(a+1)\\), pero eso es posible sólo si \\(a=3\\) y \\(v_2(b)=1\\). Entonces \\(b=2B\\), donde \\(B\\) es un número impar, lo cual permite reescribir la condición planteada de la siguiente manera: \\(2^3B^3\|3^{2B}−1\\). Sea \\(q\\) el menor número primo que divide a \\(B\\) (el cual es, sin duda alguna, impar). Sea \\(n\\) el menor número natural tal que \\(q\|3^n−1\\). Entonces \\(n\|2B\\) y \\(n\|q−1\\) , por lo que \\(n\\) debe ser \\(1\\) o \\(2\\) (o \\(B\\) tendría un divisor primo menor), lo que implica \\(q\|3−1=2\\) o \\(q\|3^2−1=8\\), lo que es una contradicción.

Finalmente, \\(B=1\\) y \\(b=2\\).

<div> </div>
{:.salto .no-mostrar}

### Problema&nbsp;<span>4</span>{:.deg-sitio-9 .deg-sitio-texto} 
Encuentre todas las soluciones en los números naturales a la ecuación \\(x^{2009}+y^{2009}=7^z\\).

#### Solución
{:.no_toc}

Al factorizar \\(2009\\), se obtiene que \\(2009=7^2\cdot 41\\). Como \\(x+y\|x^{2009}+y^{2009}\\) y \\(x+y>1\\), se cumple que \\(7\| x+y\\). Cancelando la mayor potencia de \\(7\\) que divide a \\(x\\) y \\(y\\) (¿Por qué?), se obtiene una solución de la ecuación donde \\(7\nmid x,y\\). Verificaremos si existe dicha solución. En tal caso, \\(v_7(x^{2009}+y^{2009})=\\) \\(v_7(x+y)+\\) \\(v_7(2009)=\\) \\(v_7(x+y)+2\\), entonces \\(x^{2009}+y^{2009}=\\) \\(49\cdot k\cdot(x+y)\\) donde \\(7\nmid k\\). Pero \\(x^{2009}+y^{2009}=7^z\\), es decir, el único factor primo de \\(x^{2009}+y^{2009}\\) es \\(7\\), entonces \\(k=1\\). Luego \\(x^{2009}+y^{2009}=\\) \\(49(x+y)\\). Pero la cantidad del lado izquierdo es considerablemente mayor cuando \\(\text{max}(x,y)>1\\), además, es claro que \\((x,y)=(1,1)\\) no es una solución. Entonces, la ecuación no tiene soluciónes en el conjunto de los números naturales.

<div> </div>
{:.salto .no-mostrar}

## Problemas desafiantes

### Problema&nbsp;<span>1</span>{:.deg-sitio-1 .deg-sitio-texto .deg-sitio-1}
{:.no_toc}

Sea \\(k\\) un número natural. Encuentre todos los números naturales \\(n\\) tales que \\(3^k\|2^n−1\\).

### Problema&nbsp;<span>2</span>{:.deg-sitio-2 .deg-sitio-texto} UNESCO Competition 1995
{:.no_toc}

Sean \\(a\\) y \\(n\\) dos números naturales y \\(p\\) un número primo impar tal que

$$a^p\equiv 1\mod {p^n}$${:.math}

Demuestre que

$$a\equiv 1\mod {p^{n-1}}$${:.math}

### Problema&nbsp;<span>3</span>{:.deg-sitio-3 .deg-sitio-texto} Iran Second Round 2008
{:.no_toc}

Demuestre que el único número natural \\(a\\) para el cual \\(4(a^n+1)\\) es un cubo perfecto para todo número natural \\(n\\), es \\(1\\).

### Problema&nbsp;<span>4</span>{:.deg-sitio-4 .deg-sitio-texto}
{:.no_toc}

Sea \\(k>1\\) un entero. Demuestre que existen infinitos números naturales \\(n\\) tales que

$$n|1^n+2^n+3^n+\cdots+k^n.$${:.math}

### Problema&nbsp;<span>5</span>{:.deg-sitio-5 .deg-sitio-texto} Irlanda 1996
{:.no_toc}

Sea \\(p\\) un número primo, y sean \\(a\\) y \\(n\\) números naturales. Demuestre que si

$$2^p+3^p=a^n$${:.math}

entonces \\(n=1\\).

### Problema&nbsp;<span>6</span>{:.deg-sitio-6 .deg-sitio-texto} Rusia 1996
{:.no_toc}

Sean \\(x\\), \\(y\\), \\(p\\), \\(n\\) y \\(k\\) números naturales tales que \\(n\\) impar y \\(p\\) es un número primo impar. Demuestre que si \\(x^n+y^n=p^k\\), entonces \\(n\\) es una potencia de \\(p\\).

### Problema&nbsp;<span>7</span>{:.deg-sitio-7 .deg-sitio-texto}
{:.no_toc}

Encuentre la suma  de todos los divisores \\(d\\) de \\(N=19^{88}−1\\) que son de la forma \\(d=2^a3^b\\), con \\(a,b\in\mathbb{N}\\).

### Problema&nbsp;<span>8</span>{:.deg-sitio-8 .deg-sitio-texto}
{:.no_toc}

Sea \\(p\\) un número primo. Encuentre las soluciones naturales de la ecuación \\(a^{p}−1 =p^k\\).

### Problema&nbsp;<span>9</span>{:.deg-sitio-9 .deg-sitio-texto}
{:.no_toc}

Encuentre todas las soluciones naturales de la ecuación 

$$(n−1)!+1=n^m$${:.math}

### Problema&nbsp;<span>10</span>{:.deg-sitio-10 .deg-sitio-texto} Bulgaria 1997
{:.no_toc}

Para algún número natural \\(n\\), se cumple que \\(3^n−2^n\\) es una potencia perfecta de un número primo. Demuestre que \\(n\\) es un número primo.

### Problema&nbsp;<span>11</span>{:.deg-sitio-11 .deg-sitio-texto}
{:.no_toc}

Sean \\(m\\), \\(n\\) y \\(b\\) tres números naturales tales que \\(m\ne n\\) y \\(b>1\\). Demuestre que si \\(b^n−1\\) y \\(b^m−1\\) tienen los mismos divisores primos, entonces \\(b+1\\) es una potencia de \\(2\\).

### Problema&nbsp;<span>12</span>{:.deg-sitio-12 .deg-sitio-texto} IMO ShortList 1991
{:.no_toc}

Encuentre la máxima potencia \\(k\\) de \\(1991\\) tal que \\(1991^k\\) divide a

$$1990^{1991^{1992}}+1992^{1991^{1990}}.$${:.math}

### Problem&nbsp;<span>13</span>{:.deg-sitio-12 .deg-sitio-texto}
{:.no_toc}

Pruebe que \\(a^{a−1}−1\\) nunca es libre de cuadrados para todo entero \\(a>2\\).

### Problema&nbsp;<span>14</span>{:.deg-sitio-11 .deg-sitio-texto} Checoslovaquia 1996
{:.no_toc}

Encuentre todos los números naturales \\(x\\) y \\(y\\) tales que \\(p^x−y^{\\,p}=1\\), donde \\(p\\) es un número primo.

### Problema&nbsp;<span>15</span>{:.deg-sitio-10 .deg-sitio-texto}
{:.no_toc}

Sean \\(x\\) y \\(y\\) dos números racionales positivos tales que para infinitos números naturales \\(n\\), \\(x^n−y^n\\) es un número natural. Muestre que \\(x\\) y \\(y\\) son números naturales.

### Problema&nbsp;<span>16</span>{:.deg-sitio-9 .deg-sitio-texto} IMO 2000
{:.no_toc}

¿Existe un número natural \\(n\\) tal que \\(n\\) tenga exactamente \\(2000\\) divisores primos y \\(n\\) divida a \\(2^n+1\\)?

### Problema&nbsp;<span>17</span>{:.deg-sitio-8 .deg-sitio-texto} China Western Mathematical Olympiad 2010
{:.no_toc}

Suponga que \\(m\\) y \\(k\\) son enteros no negativos, y \\(p=2^{2^{m}}+1\\) es un número primo. Muestre que

* \\(2^{2^{m+1}p^k}\equiv 1\mod  p^{k+1}\\)
* \\(2^{m+1}p^k\\) es el menor entero positivo \\(n\\) que satisface la congruencia \\(2^n\equiv 1\mod  p^{k+1}\\).

<div> </div>
{:.salto .no-mostrar}

### Problema&nbsp;<span>18</span>{:.deg-sitio-7 .deg-sitio-texto}
{:.no_toc}

Sea \\(p\ge 5\\) un número primo. Encuentre el máximo número natural \\(k\\) tal que

$$p^k|(p−2)^{2(p−1)}−(p−4)^{p−1}.$${:.math}

### Problema&nbsp;<span>19</span>{:.deg-sitio-6 .deg-sitio-texto}
{:.no_toc}

Sean \\(a\\) y \\(b\\) números reales distintos tales que los números

$$a−b,a^2−b^2,a^3−b^3,\ldots$${:.math}

son enteros. Demuestre que \\(a\\) y \\(b\\) son enteros.

### Problema&nbsp;<span>20</span>{:.deg-sitio-5 .deg-sitio-texto} MOSP 2001
{:.no_toc}

Encuentre todas las 4-tuplas de números naturales \\((x,r,p,n)\\) tales que \\(p\\) es un número primo, \\(n,r>1\\) y \\(x^r−1=p^n\\).

### Problema&nbsp;<span>21</span>{:.deg-sitio-4 .deg-sitio-texto} China TST 2009
{:.no_toc}

Sean \\(a>b>1\\) números naturales con \\(b\\) impar, y sea \\(n\\) un número natural. Si \\(b^n\|a^n−1\\), demuestre que \\(a^b>\frac{3^n}{n}\\).

### Problema&nbsp;<span>22</span>{:.deg-sitio-3 .deg-sitio-texto} Romanian Junior Balkan TST 2008
{:.no_toc}

Sea \\(p\\) un número primo distinto de \\(3\\), y sean \\(a\\) y \\(b\\) enteros tales que \\(p\|a+b\\) y \\(p^2\|a^3+b^3\\). Muestre que \\(p^2\|a+b\\) o \\(p^3\|a^3+b^3\\).

### Problema&nbsp;<span>23</span>{:.deg-sitio-2 .deg-sitio-texto}
{:.no_toc}

Sean \\(m\\) y \\(n\\) números naturales. Muestre que para cada número natural impar \\(b\\) existen infinitos números primos \\(p\\) tales que \\(p^n\equiv 1\\!\\!\mod  b^m\\) implica \\(b^{m−1}\|n\\).

### Problema&nbsp;<span>24</span>{:.deg-sitio-1 .deg-sitio-texto} IMO 1990
{:.no_toc}

Determine todos los enteros \\(n>1\\) tales que

$$\frac{2^{n} + 1}{n^2}$${:.math}

es un entero.

<div> </div>
{:.salto .no-mostrar}

### Problema&nbsp;<span>25</span>{:.deg-sitio-1 .deg-sitio-texto}
{:.no_toc}

Encuentre todos los números naturales \\(n\\) tales que

$$\frac{2^{n-1} + 1}{n}$${:.math}

es un entero.

### Problema&nbsp;<span>26</span>{:.deg-sitio-2 .deg-sitio-texto}
{:.no_toc}

Encuentre todos los números primos \\(p\\) y \\(q\\) tales que \\(\dfrac{(5^p−2^p)(5^q−2^q)}{pq}\\) es un entero.

### Problema&nbsp;<span>27</span>{:.deg-sitio-3 .deg-sitio-texto}
{:.no_toc}

Para cada número natural \\(n\\) sea \\(a\\) el mayor número natural para el cual \\(5^n−3^n\\) es divisible por \\(2^a\\). Sea \\(b\\) el mayor número natural tal que \\(2^b\le n\\). Demuestre que \\(a\le b+3\\).

### Problema&nbsp;<span>28</span>{:.deg-sitio-4 .deg-sitio-texto}
{:.no_toc}

Determine todos los conjuntos de enteros no negativos \\(x\\), \\(y\\) y \\(z\\) que satisfacen la ecuación

$$2^x+3^y=z^2.$${:.math}

### Problema&nbsp;<span>29</span>{:.deg-sitio-5 .deg-sitio-texto} IMO ShortList 2007
{:.no_toc}

Encuentre todas las funciones subyectivas \\(f : \mathbb{N}\rightarrow \mathbb{N}\\) tales que para todo \\(m,n\in\mathbb{N}\\) y todo número primo \\(p\\), \\(f(m+n)\\) es divisible por \\(p\\) sí y sólo sí \\(f(m)+f(n)\\) es divisible por \\(p\\).

### Problema&nbsp;<span>30</span>{:.deg-sitio-6 .deg-sitio-texto} Romania TST 1994
{:.no_toc}

Sea \\(n\\) un número natural impar. Demuestre que \\(\left((n−1)^n+1\right)^2\\) divide a \\(n(n−1)^{(n−1)^n+1}+n\\).

### Problema&nbsp;<span>31</span>{:.deg-sitio-7 .deg-sitio-texto}
{:.no_toc}

Encuentre todos los números naturales \\(n\\) tales que \\(3^n−1\\) es divisible por \\(2^n\\).

### Problema&nbsp;<span>32</span>{:.deg-sitio-8 .deg-sitio-texto} Romania TST 2009
{:.no_toc}

Sean \\(a,n\ge 2\\) dos enteros con la siguiente propiedad: Existe un entero \\(k\ge 2\\) tal que \\(n\\) divide a \\((a−1)^k\\). Demuestre que \\(n\\) divide a 

$$a^{n−1}+a^{n−2}+\cdots+a+1.$${:.math}

### Problema&nbsp;<span>33</span>{:.deg-sitio-9 .deg-sitio-texto}
{:.no_toc}

Encuentre todos los números naturales \\(a\\) tales que \\(\frac{5^a+1}{3^a}\\) es un número natural.

<div> </div>
{:.salto .no-mostrar}

## Algunas pistas y soluciones para los Problemas desafiantes
### Problema [<span>1</span>{:.deg-sitio-1 .deg-sitio-texto}](#problema1)
{:.no_toc}

Respuesta: \\(n=2\cdot 3^{k−1}s\\) para algún \\(s\in\mathbb{N}\\).

### Problema [<span>2</span>{:.deg-sitio-2 .deg-sitio-texto}](#problema2-unesco-competition-1995)
{:.no_toc}

Demuestre que \\(v_p(a−1)=v_p(a^p−1)−1\ge\\)\\(n−1\\).

### Problema [<span>3</span>{:.deg-sitio-3 .deg-sitio-texto}](#problema3-iran-second-round-2008)
{:.no_toc}

Si \\(a>1\\), \\(a^2+1\\) no es potencia de \\(2\\) (porque es \\(> 2\\) y congruente con \\(1\\) o \\(2\\) módulo \\(4\\)). Sea \\(p\\) un número primo impar tal que \\(p\|a^2+1\\). Para cualquier \\(n=2m\\) con \\(m\\) impar se cumple que \\(v_p(4(a^n+1))=\\) \\(v_p(a^2+1)+v_p(m)\\) pero \\(v_p(m)\\) puede tener cualquier congruencia en módulo \\(3\\).

### Problema [<span>5</span>{:.deg-sitio-4 .deg-sitio-texto}](#problema5-irlanda-1996)
{:.no_toc}

\\(2^p+3^p\\) no es un cuadrado perfecto, además, \\(v_5(2^p+3^p)=\\) \\(1+v_5(p) \le 2\\).

### Problema [<span>8</span>{:.deg-sitio-5 .deg-sitio-texto}](#problema8)
{:.no_toc}

Considere dos casos: \\(p=2\\) y \\(p\\) es un número primo impar. El último caso no tiene soluciones.

### Problema [<span>9</span>{:.deg-sitio-6 .deg-sitio-texto}](#problema9)
{:.no_toc}

\\((n,m)=(2,1)\\) es una solución. En otros casos, demuestre que \\(n\\) es un número primo impar y \\(m\\) es par. La otra solución es \\((n,m)=(5,2)\\).

### Problema [<span>12</span>{:.deg-sitio-7 .deg-sitio-texto}](#problema12-imo-shortlist-1991)
{:.no_toc}

Respuesta: \\(\text{max}(k)=1991\\).

### Problema [<span>13</span>{:.deg-sitio-8 .deg-sitio-texto}](#problema13)
{:.no_toc}

Tome cualquier número primo impar \\(p\\) tal que \\(p\|a−1\\). Es claro que \\(p^2\|a^{a−1}−1\\).

### Problema [<span>14</span>{:.deg-sitio-9 .deg-sitio-texto}](#problema14-Checoslovaquia-1996)
{:.no_toc}

Respuesta: \\((p,x,y)=(2, 1, 1),\\) \\((3, 2, 1)\\).

### Problema [<span>18</span>{:.deg-sitio-10 .deg-sitio-texto}](#problema18)
{:.no_toc}

Sea \\(p−1=2^sm\\). Demuestre que \\(v_p(2^{s−1}m)=0\\). El máximo valor de \\(k\\) es \\(1\\).

### Problema [<span>19</span>{:.deg-sitio-11 .deg-sitio-texto}](#problema19)
{:.no_toc}

Intente demostrar el **Problema [<span>15</span>{:.deg-sitio-12 .deg-sitio-texto}](#problema15)** primero.

### Problema [<span>20</span>{:.deg-sitio-11 .deg-sitio-texto}](#problema20-mosp-2001)
{:.no_toc}

Demuestre que \\(p=2\\) y \\(r\\) es un número natural par.

### Problema [<span>22</span>{:.deg-sitio-10 .deg-sitio-texto}](#problema22-romanian-junior-balkan-tst-2008)
{:.no_toc}

Si \\(p\|a\\) y \\(p\|b\\), entonces \\(p^3\|a^3+b^3\\). En caso contrario, se puede aplicar **LTE** y \\(v_p(a+b)=\\) \\(v_p(a^3+b^3)\ge 2\\).

### Problema [<span>24</span>{:.deg-sitio-9 .deg-sitio-texto}](#problema24-imo-1990)
{:.no_toc}

Respuesta: \\(n=1\\) or \\(n=3\\).

### Problema [<span>26</span>{:.deg-sitio-8 .deg-sitio-texto}](#problema26)
{:.no_toc}

Respuesta: \\((p,q)=(3,3),(3,13)\\).

### Problema [<span>27</span>{:.deg-sitio-7 .deg-sitio-texto}](#problema27)
{:.no_toc}

Si \\(n\\) es impar, entonces \\(a=1\\). Si \\(n\\) es par, se tiene que \\(a=v_2(5^n−3^n)=\\) \\(v_2(5−3)+v_2(5+3)+v_2(n)−1=\\) \\(3+v_2(n)\\). Pero \\(b\ge v_2(n)\\).

### Problema [<span>30</span>{:.deg-sitio-6 .deg-sitio-texto}](#problema30-romania-tst-1994)
{:.no_toc}

\\(n\|(n−1)^n+1\\), entonces para todo \\(p\\) tal que \\(p\|(n−1)^n+1\\), se cumple que

$$\begin{align*}
v_p\left((n−1)^{(n−1)^n+1}+1\right)&= v_p((n − 1)^n+1)+v_p\left(\frac{(n−1)^{n+1}+1}{n}\right)\\
&=2v_p((n−1)^n+1)−v_p(n)
\end{align*}
$${:.math}

lo que concluye la demostración.

### Problema [<span>31</span>{:.deg-sitio-5 .deg-sitio-texto}](#problema31)
{:.no_toc}

\\(n\le v_2(3^n−1)\le 3+v_2(n)\\), entonces \\(n\le 4\\).

### Problema [<span>33</span>{:.deg-sitio-4 .deg-sitio-texto}](#problema33)
{:.no_toc}

\\(a\\) debe ser impar (o el numerador sería congruente con \\(2\mod 3\\)). Entonces \\(a\le v_3(5^a+1)=\\) \\(1+v_3(a)\\) lo que da como única solución \\(a=1\\).

<div> </div>
{:.salto .no-mostrar}

## Fuentes originales

¡Visita el sitio web de Amir [<span>aquí!</span>{:.deg-sitio-1 .deg-sitio-texto}](https://parvardi.com)<br/>
<span>https://parvardi.com</span>{:.deg-sitio-1 .deg-sitio-texto .no-mostrar}

Descarga el [<span>Archivo PDF (211 KB)</span>{:.deg-sitio-2 .deg-sitio-texto}](https://services.artofproblemsolving.com/download.php?id=YXR0YWNobWVudHMvNS8wLzgyODNhOGNhOWQ4OWM1NDk5NTY1MGQyNWVlYWNlMzE1OGYxMDM0&rn=TGlmdGluZyBUaGUgRXhwb25lbnQgLSBWZXJzaW9uIDYucGRm) original, publicado en abril de 2011.<br/>
<span>https://services.artofproblemsolving.com/download.php?id=YXR0YWNobWVudHMvNS8wLzgyODNhOGNhOWQ4OWM1NDk5NTY1MGQyNWVlYWNlMzE1OGYxMDM0&rn=TGlmdGluZyBUaGUgRXhwb25lbnQgLSBWZXJzaW9uIDYucGRm</span>{:.deg-sitio-2 .deg-sitio-texto .no-mostrar}

## Referencias

**<span>1.</span>{:.deg-sitio-3 .deg-sitio-texto}**&#x2007;Sepehr Ghazi Nezami, **[<span>Leme Do Khat</span>{:.deg-sitio-3 .deg-sitio-texto}](http://imo09.blogfa.com/page/2khat.aspx)** (en inglés: *Lifting The Exponent
Lemma*), publicado en octubre de 2009.

**<span>2.</span>{:.deg-sitio-4 .deg-sitio-texto}**&#x2007;Kurt Hensel, **[<span>Hensel’s lemma</span>{:.deg-sitio-4 .deg-sitio-texto}](http://en.wikipedia.org/wiki/Hensel's_lemma)**, WikiPedia.

**<span>3.</span>{:.deg-sitio-5 .deg-sitio-texto}**&#x2007;Santiago Cuellar, Jose Alejandro Samper, *A nice and tricky lemma (lifting the exponent)*, Mathematical Reflections 3 - 2007.

**<span>4.</span>{:.deg-sitio-6 .deg-sitio-texto}**&#x2007;Amir Hossein Parvardi, Fedja et al., **[<span>AoPS topic #393335</span>{:.deg-sitio-6 .deg-sitio-texto}](http://www.artofproblemsolving.com/Forum/viewtopic.php?t=393335)**, *Lifting The Exponent Lemma (Contiene un archivo PDF)*.

**<span>5.</span>{:.deg-sitio-7 .deg-sitio-texto}**&#x2007;Orlando Doehring et al., **[<span>AoPS topic #214717</span>{:.deg-sitio-7 .deg-sitio-texto}](https://artofproblemsolving.com/community/c6h214717)**, *Number \\(\mod \;(f(m+n), p)=0\\) iff \\(\mod \;(f(m) + f(n), p)=0\\)*.

**<span>6.</span>{:.deg-sitio-8 .deg-sitio-texto}**&#x2007;Fang-jh et al., **[<span>AoPS topic #268964</span>{:.deg-sitio-8 .deg-sitio-texto}](https://artofproblemsolving.com/community/h268964)**, *China TST, Quiz 6, Problem 1*.

**<span>7.</span>{:.deg-sitio-9 .deg-sitio-texto}**&#x2007;Valentin Vornicu et al., **[<span>AoPS topic #57607</span>{:.deg-sitio-9 .deg-sitio-texto}](https://artofproblemsolving.com/community/h268964)**, *exactly 2000 prime divisors
(IMO 2000 P5)*.

**<span>8.</span>{:.deg-sitio-10 .deg-sitio-texto}**&#x2007;Orlando Doehring et al., **[<span>AoPS topic #220915</span>{:.deg-sitio-10 .deg-sitio-texto}](https://artofproblemsolving.com/community/c6h220915)**, *Highest degree for 3-layer
power tower*.

**<span>9.</span>{:.deg-sitio-11 .deg-sitio-texto}**&#x2007;Sorush Oraki, Johan Gunardi, **[<span>AoPS topic #368210</span>{:.deg-sitio-11 .deg-sitio-texto}](https://artofproblemsolving.com/community/h368210)**, *Prove that \\(a=1\\) if
\\(4(a^n+1)\\) is a cube for all \\(n\\)*.
