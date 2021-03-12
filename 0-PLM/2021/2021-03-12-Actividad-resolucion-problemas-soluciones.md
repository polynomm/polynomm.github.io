---
layout: default
search_exclude: true
tema: Verde
tema_oscuro: VerdeOscuro
title: Soluciones
nav_order: 2021-03-12
description: "Soluciones de la actividad."
last_modified_date: 2021-03-04T10:00:00+0000
parent: PLM 2021
grand_parent: PLM
---

# Actividad de Resolución de&nbsp;<span class="deg-sitio deg-sitio-texto">problemas</span>
{:.fs-9}

12 de marzo de 2021
{:.fs-6 .fw-300}

## Opción múltiple

### Problema&nbsp;<span class="deg-sitio deg-sitio-texto">1</span>
Tenemos un rectángulo \\(A\\) tal que la suma de su base y su altura es igual a 27. Si se construye un rectángulo \\(B\\) con base tres unidades menor, y altura tres unidades mayor, el área no cambia. Se construye un rectángulo  \\(C\\) con base 4 unidades menor y altura cuatro unidades mayor respecto al rectángulo \\(A\\). ¿Cuál es el valor del área de \\(A\\) menos el área de \\(C\\)?

#### Solución

La manera más intuitiva de resolver este problema es proponer que el rectángulo \\(B\\) sea igual al rectángulo \\(A\\), pero ahora la base de \\(A\\) será la altura de \\(B\\), y la altura de \\(A\\) será la base de \\(B\\). 

Luego, la base de \\(A\\) y la base de \\(B\\) deben sumar 27, y la base de \\(B\\) es tres unidades menor a la base de \\(A\\), por lo que la base de \\(A\\) debe medir 15 y la base de \\(B\\) debe medir 12. Luego, la altura de \\(A\\) es 12 y su área es 180.

Finalmente, la base del rectángulo \\(C\\) mide 19 y su altura mide 8, por lo que su área es igual a 152. Es decir, el valor del área de \\(A\\) menos el área de \\(C\\) es igual a 28.

#### Solución alternativa

Sean \\(b\\) y \\(h\\) la base y la altura del rectángulo \\(A\\). Entonces:

$$
\begin{align*}
bh&=(b-3)(h+3)\\
bh&=bh+3b-3h-9\\
0&=-3(h-b)-9\\
3(h-b)&=-9\\
b-h&=3\\
\end{align*}
$${:.math}

Luego, se resuelve el siguiente sistema de ecuaciones:

$$
\begin{cases}
b-h=3\\
b+h=27
\end{cases}
$${:.math}

Cuya solución es \\(b=15\\) y \\(h=12\\).

Luego, el área de \\(A\\) es \\(15(12)=180\\) y el área de \\(C\\) es \\(19(8)=152\\). Es decir, la diferencia entre las áreas es igual a 28.

### Problema&nbsp;<span class="deg-sitio deg-sitio-texto">2</span>

Encuentra el valor de

$$\frac{1}{8}+\frac{1}{15}+\frac{1}{24}+\frac{1}{35}+\frac{1}{48}+\frac{1}{63}+\frac{1}{80}$${:.math}

#### Solución

La suma anterior se puede expresar como:

$$\frac{1}{2(4)}+\frac{1}{3(5)}+\frac{1}{4(6)}+\frac{1}{5(7)}\frac{1}{6(8)}+\frac{1}{7(9)}+\frac{1}{8(10)}$${:.math}

Sólo queda notar que:

$$\frac{1}{n(n+2)}=\frac{1}{2}\left(\frac{1}{n}-\frac{1}{n+2}\right)$${:.math}

Si vemos la suma de los elementos con denominador par:

$$\frac{1}{2(4)}+\frac{1}{4(6)}+\frac{1}{6(8)}+\frac{1}{8(10)}$${:.math}

obtenemos

$$\frac{1}{2}\left(\frac{1}{2}-\frac{1}{4}+\frac{1}{4}-\frac{1}{6}+\frac{1}{6}-\frac{1}{8}+\frac{1}{8}-\frac{1}{10}\right)$${:.math}

es decir, \\(\frac{1}{2}\left(\frac{1}{2}-\frac{1}{10}\right)=\frac{1}{5}\\).

Con los elementos impares:

$$\frac{1}{3(5)}+\frac{1}{5(7)}+\frac{1}{7(9)}$${:.math}

obtenemos

$$\frac{1}{2}\left(\frac{1}{3}-\frac{1}{5}+\frac{1}{5}-\frac{1}{7}+\frac{1}{7}-\frac{1}{9}\right)$${:.math}

es decir, \\(\frac{1}{2}\left(\frac{1}{3}-\frac{1}{9}\right)=\frac{1}{9}\\).

Finalmente, \\(\frac{1}{5}+\frac{1}{9}=\frac{14}{45}\\)

### Problema&nbsp;<span class="deg-sitio deg-sitio-texto">3</span>

Cuando \\(12^{18}\\) es dividido entre \\(18^{12}\\), se obtiene un número de la forma \\(\left(\frac{m}{n}\right)^3\\), donde \\(m\\) y \\(n\\) son números naturales que no tienen factores en común. ¿Cuál es el valor de \\(m-n\\)?

#### Solución

Sólo es necesario utilizar las leyes de los exponentes:

$$
\begin{align*}
\frac{12^{18}}{18^{12}}&=\left(\frac{12^6}{18^4}\right)^3\\
&=\left(\frac{3^6\cdot 4^6}{2^4\cdot 9^4}\right)^3\\
&=\left(\frac{3^6 \cdot2^{12}}{2^4\cdot 3^8}\right)^3\\
&=\left(\frac{2^8}{3^2}\right)^3\\
\end{align*}
$${:.math}

Como \\(2^8\\) y \\(3^2\\) no tienen factores en común, \\(m=256\\) y \\(n=9\\), es decir, \\(m-n=247\\).


### Problema&nbsp;<span class="deg-sitio deg-sitio-texto">4</span>

Aldo y Beto juegan con sus equipos su propia versión del básquetbol. Si un equipo encesta en la canasta ubicada en la sombra, gana 3 puntos. Si encesta en la canasta ubicada en el sol, gana 5 puntos. El equipo de Aldo acumuló al final 25 puntos, pero no anotaron en orden los puntajes que obtuvieron con cada canasta.

¿Cuántas listas de puntajes puede escribir el equipo de Aldo, sin alterar su puntaje?

#### Solución

Es necesario notar que el número de canastas a la sombra es múltiplo de 5 (dado que el total de puntos, y los puntos por cada canasta en el sol son múltiplos de 5). Luego: el equipo de Aldo encesta siempre en sol, o encestó 5 veces en la sombra.

Si encesta siempre en el sol, sólo hay una posibilidad (5 canastas de 5).

Si encesta 5 veces a la sombra, encestó dos veces bajo el sol. Luego, el problema consiste en ordenar una secuencia de 7 canastas, cinco de 3 puntos y dos de 5 puntos, es decir, esto puede suceder de \\(\binom{7}{2}=21\\) maneras distintas.

Si se prefiere escribir las listas posibles, puede realizar un diagrama como el siguiente.

$$
\begin{array}{ccccccc}
3&3&3&3&3&5&5\\
3&3&3&3&5&3&5\\
3&3&3&3&5&5&3\\
3&3&3&5&3&3&5\\
3&3&3&5&3&5&3\\
3&3&3&5&5&3&3\\
3&3&5&3&3&3&5\\
3&3&5&3&3&5&3\\
3&3&5&3&5&3&3\\
3&3&5&5&3&3&3\\
3&5&3&3&3&3&5\\
3&5&3&3&3&5&3\\
3&5&3&3&5&3&3\\
3&5&3&5&3&3&3\\
3&5&5&3&3&3&3\\
5&3&3&3&3&3&5\\
5&3&3&3&3&5&3\\
5&3&3&3&5&3&3\\
5&3&3&5&3&3&3\\
5&3&5&3&3&3&3\\
5&5&3&3&3&3&3\\
\end{array}
$${:.math}

Finalmente, en total hay 22 maneras distintas de escribir dicha lista.

## Demostración

Crea un archivo PDF con tu demostración.

### Problema&nbsp;<span class="deg-sitio deg-sitio-texto">5</span>

Muestre que, para todo número primo \\(p\\) mayor que 3, existe un número natural \\(n\\) tal que \\(p=\sqrt{24n+1}\\).

#### Solución

Se obtiene directamente que \\(p^2=24n+1\\), es decir, \\(p^2-1=24n\\). Lo anterior es equivalente a demostrar que si \\(p>3\\), entonces \\(p^2-1\\) es múltiplo de 24.

Pero \\(p^2>3\\) implica que 6 y \\(p\\) no tienen factores en común, es decir, \\(p\\) no es par ni múltiplo de 3. En consecuencia, \\(p^2\equiv 1\mod 3\\) y \\(p^2\equiv 1\mod 8\\), es decir, \\(p^2\equiv 1\mod 24\\). Luego, \\(p^2-1=24n\\) para algún entero \\(n\\). Dado que \\(p^2-1>0\\) por ser \\(p>3\\) y \\(24>0\\), se tiene que \\(n>0\\), por lo que \\(n\\) es un número natural.


<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfuGCR0cYlg-Pk0DKH83ExG5J_Q5DPHqGs73HRiW4cO2wZuKg/viewform?embedded=true" width="100%" height="360" margin="auto" frameborder="0" marginheight="0" marginwidth="0">Cargando…</iframe>
{:.no-imprimir}