---
layout: default
title: Soluciones Tres problemas de Geo
nav_order: 2020-11-16
description: "Soluciones de la lista Tres problemas POLYNOMM de Geometría"
last_modified_date: 2020-09-29T13:00:00+0000
grand_parent: Listas POLYNOMM
parent: POLYNOMM 2020
---

<link rel="stylesheet" href="{{ '/assets/css/just-the-docs-degNaranja.css' | absolute_url }}">
<script>
    jtd.setTheme('degNaranja');
</script>

# Soluciones de la lista Tres problemas de <span class="deg-sitio deg-sitio-texto">Geo</span><i class="jpa-anim-rel-jack_o_lantern jpa-2em"></i>
{:.fs-9 .no-toc}

Esperamos que les hayan gustado los problemas...
{:.fs-6 .fw-300}

16 de noviembre de 2020.

Geometría
{:.label .deg-geometria .deg-geometria-fondo}


### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1</span>
{: .no_toc}
<!--Diseñado por Alexis J.D.V.-->

Al interior de cada lado del triángulo \\(ABC\\) se trazan dos puntos que dividen al lado en tres segmentos de igual longitud. Sean \\(P\\) y \\(Q\\) los puntos marcados sobre el segmento \\(BC\\). A partir de los 6 puntos marcados, se divide el triángulo en  15 regiones como se muestra en la figura, donde a excepción de la región central (delimitada por los dos  segmentos paralelos a \\(BC\\), \\(PA\\) y \\(QA\\)), las regiones se pintan de naranja o negro, de manera que no haya dos regiones que compartan un lado del mismo color. Sea \\(A_1\\) el área total de las regiones coloreadas de naranja y \\(A_2\\) el área total de las regiones coloreadas de negro.

Encuentre \\(\frac{A_1}{A_2}\\).

<div class="geo-app"><div id="P1"></div></div>

#### Solución

En la siguiente figura, los pares puntos marcados en \\(AB\\) y \\(AC\\) son \\(P_1\\) y \\(P_3\\), y \\(Q_1\\) y \\(Q_3\\),respectivamente, de manera que \\(\frac{AP_1}{P_1B}=\frac{AQ_1}{Q_1C}=\frac{1}{2}\\). \\(P_2\\) y \\(Q_2\\) son las intersecciones de \\(AP\\) y \\(AQ\\) con \\(P_1Q_1\\); \\(P_4\\) y \\(Q_4\\) son las intersecciones de \\(PP_1\\) y \\(QQ_1\\) con \\(P_3Q_3\\); \\(P_5\\) y \\(Q_5\\) son las intersecciones de \\(AP\\) y \\(AQ\\) con \\(P_3Q_3\\), respectivamente.

<div class="geo-app"><div id="P1_S1_1"></div></div>

Sea \\(k\\) la recta paralela a \\(BC\\) por \\(A\\).

Como \\(\frac{AP_1}{P_1B}=\frac{AQ_1}{Q_1C}\\), y \\(\frac{AP_3}{P_3B}=\frac{AQ_3}{Q_3C}\\), por el **Teorema de Tales**, la recta \\(\ell\\) que pasa por \\(P_1\\) y \\(Q_1\\), y la recta \\(m\\) que pasa por \\(P_3\\) y \\(Q_3\\), son paralelas a la recta \\(n\\) que pasa por \\(B\\) y \\(C\\). Ahora, trazamos la altura del triángulo \\(ABC\\) que pasa por \\(A\\), la cual intersecta a \\(\ell\\), \\(m\\) y \\(n\\) en \\(X\\), \\(Y\\) y \\(Z\\), respectivamente. Si \\(Z\ne B\\), por el **Teorema de Tales**, se tiene que \\(\frac{AP_1}{P_1P_3}=\frac{AX}{XY}=1\\) y \\(\frac{P_1P_3}{P_3B}=\frac{XY}{YZ}=1\\). Si \\(Z=B\\), \\(P_1=X\\) y \\(P_3=Y\\). En ambos casos, resulta que la distancia entre \\(k\\) y \\(\ell\\), entre \\(\ell\\) y \\(m\\), y entre \\(m\\) y \\(n\\), es la misma.

<div class="geo-app"><div id="P1_S1_2"></div></div>

Para finalizar, utilizaremos una propiedad que cumplen las rectas paralelas:

> Dadas dos rectas paralelas, la distancia entre cualquier punto en una de aquella rectas a la otra recta es constante.

Así, podemos el problema se resuelve de la siguiente manera:

Sea \\(h\\) la longitud de \\(AX\\).

Dado que \\(P_1Q_1\parallel P_3Q_3\parallel BC\\), \\(\triangle AP_2Q_2\sim\triangle AP_5Q_5\sim\\) \\(\triangle APQ\\), resulta que \\(P_2Q_2=\frac{PQ}{3}\\) y \\(P_5Q_5=\frac{2PQ}{3}\\). Entonces:

$$
\begin{align*}
(AP_2Q_2)+(QP_5Q_5)&=\frac{h(P_2Q_2)}{2}+\frac{h(P_5Q_5)}{2}\\[0.5cm]
&=\left(P_2Q_2+P_5Q_5\right)\left(\frac{h}{2}\right)\\[0.5cm]
&=PQ\left(\frac{h}{2}\right)\\[0.5cm]
&=(Q_3QC)
\end{align*}
$$
{:.math }

Como puede observarse, el valor de la suma de áreas de dos regiones coloreadas de negro: \\((AP_2Q_2)+(QP_5Q_5)\\), es igual al área de una región naranja: \\((Q_3QC)\\). Sucede que, con el resto de regiones que integran la totalidad de la superficie coloreada del triángulo, se pueden crar pares de regiones naranjas y negras con la misma área, como se muestra a continuación:

$$
\begin{align*}
(AP_1P_2)&=\frac{h(P_1P_2)}{2}&(AQ_1Q_2)&=\frac{h(Q_1Q_2)}{2}\\[0.5cm]
&=(P_5P_1P_2)&&=(Q_5Q_1Q_2)\\[1cm]
(PP_4P_5)&=\frac{h(P_4P_5)}{2}&(QQ_4Q_5)&=\frac{h(Q_4Q_5)}{2}\\[0.5cm]
&=(P_1P_4P_5)&&=(Q_1Q_4Q_5)\\[1cm]
\end{align*}
$$
{:.math }

$$
\begin{align*}
(P_1P_3P_4)&=\frac{h(P_3P_4)}{2}&(Q_1Q_3Q_4)&=\frac{h(Q_3Q_4)}{2}\\[0.5cm]
&=(PP_3P_4)&&=(QQ_3Q_4)\\[1cm]
(P_3BP)&=\frac{h(BP)}{2}&&\\[0.5cm]
&=\frac{h(PQ)}{2}&&\\[0.5cm]
&=(P_5PQ)&&
\end{align*}
$$
{:.math }

Esto indica que  \\(A_1=A_2\\), es decir \\(\frac{A_1}{A_2}=1\\)

<div></div>
{:.salto .no-mostrar}

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">2</span>
{: .no_toc}

<!--Diseñado por Alexis J.D.V.-->

Sea \\(A_0B_0C_0\\) un triángulo equilátero de lado 1. Para cada entero \\(k\ge0\\), se definen \\(A_{k+1}\\), \\(B_{k+1}\\) y \\(C_{k+1}\\), que son puntos sobre \\(A_kB_k\\), \\(B_kC_k\\) y \\(C_kA_k\\), respectivamente, tales que:

$$
\frac{A_kA_{k+1}}{A_{k+1}B_k}=\frac{B_kB_{k+1}}{B_{k+1}C_k}=\frac{C_kC_{k+1}}{C_{k+1}A_k}
$$
{:.math }

y

$$
\frac{A_kA_{k+1}}{A_{k+1}B_k}=
\begin{cases}
\frac{1}{2}\\[0.5cm]
2
\end{cases}
$$
{:.math }

Encuentre, en todos los casos:

* el área de \\(A_nB_nC_n\\) para todo entero no negativo \\(n\\).
* todos los enteros no negativos \\(n\\) para los cuales \\(A_nB_nC_n\\) tiene lados paralelos a los lados de \\(A_0B_0C_0\\).

<div class="geo-app"><div id="P2"></div></div>

Nota: *El valor de \\(\frac{A_iA_{i+1}}{A_{i+1}B_i}\\), que puede ser \\(\frac{1}{2}\\) o \\(2\\), no es necesariamente igual al valor de \\(\frac{A_jA_{j+1}}{A_{j+1}B_j}\\) para enteros no negativos distintos \\(i,j\\) .*

<div></div>
{:.salto .no-mostrar}

Es necesario ver algunas propiedades en la construcción para solucionar el problema de manera sencilla, para todo entero no negativo \\(k\\).

> **1.** En los tres pares de segmentos \\(A_kA_{k+1}\\) y \\(AC_{k+1}\\); \\(B_kB_{k+1}\\) y \\(BA_{k+1}\\); \\(C_kC_{k+1}\\) y \\(CB_{k+1}\\), se cumple que el mayor dobla la longitud del menor, y el ángulo que forman es de \\(60^\circ\\), en ambos casos. 
> 
> Además, \\(A_kA_{k+1}\\)\\(=A_kA_{k+1}\\)\\(=A_kA_{k+1}\\) y \\(AC_{k+1}\\)\\(=CB_{k+1}\\)\\(=BA_{k+1}\\).
   
Al profundizar en esta propiedad, surgen las siguientes propiedades:

> **2.** El triángulo \\(A_{k+1}B_{k+1}C_{k+1}\\) es equilátero (y por tanto es semejante al triángulo  \\(A_kB_kC_k\\)), dado que \\(A_kA_{k+1}C_{k+1}\\), \\(B_kB_{k+1}A_{k+1}\\) y \\(C_kC_{k+1}B_{k+1}\\) son congruentes por criterio \\(LAL\\).
> 
> **3.** Cada lado del triángulo \\(A_{k+1}B_{k+1}C_{k+1}\\) es perpendicular a exactamente un lado del triángulo \\(A_kB_kC_k\\), dado que \\(A_kA_{k+1}C_{k+1}\\), \\(B_kB_{k+1}A_{k+1}\\) y \\(C_kC_{k+1}B_{k+1}\\) son triángulos rectángulos.

>**4.** Ningún lado del triángulo \\(A_{k+1}B_{k+1}C_{k+1}\\) es paralelo a un lado del triángulo \\(A_kB_kC_k\\), debido a que cada lado de \\(A_{k+1}B_{k+1}C_{k+1}\\), al ser perpendicular a exactamente un lado de \\(A_kB_kC_k\\), es paralelo a una de las alturas de \\(A_kB_kC_k\\), las cuales claramente intersectan a los tres lados del triángulo.

Las propiedades 2 y 3 nos permiten aplicar el **Teorema de Pitágoras** en el triángulo \\(A_kA_{k+1}C_{k+1}\\), obteniendo que 

$$
\begin{align*}
A_{k+1}B_{k+1}^2&=\frac{4\cdot A_kB_k^2}{9}\\[0.5cm]
\implies \frac{A_{k+1}B_{k+1}^2}{A_kB_k^2}&=\frac{4}{9}\\[0.5cm]
\end{align*}
$$
{:.math}

Finalmente, como el cuadrado de la razón de semejanza es la razón entre las áreas de dos triángulos semejantes, y \\(A_{k+1}B_{k+1}C_{k+1}\sim A_kB_kC_k\\), se tiene que

$$
\frac{\left(A_{k+1}B_{k+1}C_{k+1}\right)}{\left(A_kB_kC_k\right)}=\frac{4}{9}\\[0.5cm]
$$
{:.math}

Donde los paréntesis simbolizan el área del polígono representado en su interior.

La primera parte del problema se resuelve fácilmente notando que

$$
\begin{align*}
\left(A_0B_0C_0\right)&=\frac{A_0B_0^2\sqrt{3}}{4}\\[0.5cm]
&=\frac{\sqrt{3}}{4}\\[0.5cm]
&=\frac{\sqrt{3}}{4}\left(\frac{4}{9}\right)^0
\end{align*}
$$
{:.math}

Y, para todo \\(n\ge 1\\)

$$
\begin{align*}
\left(A_nB_nC_n\right)&=(A_0B_0C_0)\displaystyle\prod_{i=0}^{n-1}\frac{\left(A_{n-i}B_{n-i}C_{n-i}\right)}{\left(A_{n-i-1}B_{n-i-1}C_{n-i-1}\right)}\\[0.5cm]
&=(A_0B_0C_0)\underbrace{\frac{\left(A_{n}B_{n}C_{n}\right)}{\left(A_{n-1}B_{n-1}C_{n-1}\right)}
\frac{\left(A_{n-1}B_{n-1}C_{n-1}\right)}{\left(A_{n-2}B_{n-2}C_{n-2}\right)}
\cdots \frac{\left(A_{1}B_{1}C_{1}\right)}{\left(A_{0}B_{0}C_{0}\right)}}_{\text{n factores}}
\\[0.5cm]
&=\frac{\sqrt{3}}{4}\left(\frac{4}{9}\right)^n
\end{align*}
$$
{:.math}

Entonces la primera parte del problema queda resuelta: *Para todo entero no negativo \\(n\\), el área de \\(A_nB_nC_n\\) es igual a*

$$
\frac{\sqrt{3}}{4}\left(\frac{4}{9}\right)^n
$$
{:.math}

Para la segunda parte del problema, al utilizar la propiedad 3, resulta que *cada lado del triángulo \\(A_{k+2}B_{k+2}C_{k+2}\\) es perpendicular a exactamente un lado del triángulo \\(A_{k+1}B_{k+1}C_{k+1}\\)*, además, *cada lado del triángulo \\(A_{k+1}B_{k+1}C_{k+1}\\) es perpendicular a exactamente un lado del triángulo \\(A_kB_kC_k\\)*. Por lo tanto, **cada lado del triángulo \\(A_{k+2}B_{k+2}C_{k+2}\\) es paralelo a exactamente un lado del triángulo  \\(A_kB_kC_k\\)**. Lo anterior, sumado a la propiedad 4, implica que cada lado del triángulo \\(A_iB_iC_i\\) es paralelo a un lado del triángulo \\(A_jB_jC_j\\) cuando \\(i\equiv j\mod{2}\\). Por lo tanto, los valores de \\(n\\) para los cuales el triángulo \\(A_nB_nC_n\\) tiene sus lados paralelos a los del triángulo \\(A_0B_0C_0\\) son los enteros pares no negativos.

<div></div>
{:.salto .no-mostrar}

### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">3</span>
{: .no_toc}

<!-- Problema diseñado por Alexis J.D.V. -->

Dos circunferencias de radio positivo con centros \\(O_1\\) y \\(O_2\\) son tangentes a una recta \\(\ell\\) en dos puntos distintos \\(P\\) y \\(Q\\), respectivamente, y son tangentes entre sí en el punto \\(R\\). Si se cumple que:

$$
\frac{PO_1}{QO_2}=
\begin{cases}
\frac{PO_2}{QO_1}\\[0.5cm]
\frac{QO_1}{PO_2}
\end{cases}
$$
{:.math}

Encuentra la medida del ángulo \\(\angle PQR\\) en cada caso.

#### Solución

Utilizaremos dos propiedades para resolver este problema:

* Para cualquier punto sobre una circunferencia, el radio y la recta tangente que pasan por dicho punto son perpendiculares.
* El **Teorema de Pitágoras**.

La primera propiedad implica que los ángulos \\(\angle O_1PQ\\) y \\(\angle O_2PQ\\) son rectos, por lo que podemos aplicar directamente el Teorema de Pitágoras en los triángulos \\(PQO_1\\) y \\(PQO_2\\):

<div class="geo-app"><div id="P3_S1_1"></div></div>

$$
\begin{align*}
PQ^2+PO_1^2&=QO_1^2&PQ^2+QO_2^2&=PO_2^2
\end{align*}
$$
{:.math}

En base a lo anterior, podemos analizar dos casos:

1. \\(\frac{PO_1}{QO_2}=\frac{PO_2}{QO_1}\\)
   
   Elevamos al cuadrado y sustituimos:
   
   $$
   \begin{align*}
   \frac{PO_1^2}{QO_2^2}&=\frac{PO_2^2}{QO_1^2}\\[0.5cm]
   &=\frac{PQ^2+QO_2^2}{PQ^2+PO_1^2}
   \end{align*}
   $$
   {:.math}
   
   Entonces, tenemos tres posibilidades:
   
   > **a)** \\(PO_1< QO_2\\)
   >
   >> Esto implica 
   
   $$\frac{PO_1^2}{QO_2^2}<1<\frac{PQ^2+QO_2^2}{PQ^2+PO_1^2}$$
   {:.math}
   
   >>lo cual es falso, dado que 
   
   $$\frac{PO_1^2}{QO_2^2}=\frac{PQ^2+QO_2^2}{PQ^2+PO_1^2}$$
   {:.math}

   > **b)** \\(PO_1> QO_2\\)
   >
   >> De manera análoga al caso anterior, esto implica 
   
   $$\frac{PO_1^2}{QO_2^2}>1>\frac{PQ^2+QO_2^2}{PQ^2+PO_1^2}$$
   {:.math}
   
   >>lo cual es falso, dado que 
   
   $$\frac{PO_1^2}{QO_2^2}=\frac{PQ^2+QO_2^2}{PQ^2+PO_1^2}$$
   {:.math}

   > **c)** \\(PO_1=QO_2\\)
   >
   >>En este caso no se presenta ninguna contradicción.

2. \\(\frac{PO_1}{QO_2}=\frac{QO_1}{PO_2}\\)
   
   Basta con realizar unas cuantas operaciones para obtener que...

   $$
   \begin{align*}
   \frac{PO_1^2}{QO_2^2}&=\frac{PQ^2+PO_1^2}{PQ^2+QO_2^2}\\[0.5cm]
   \implies PO_1^2\left(PQ^2+QO_2^2\right)&=QO_2^2\left(PQ^2+PO_1^2\right)\\[0.5cm]
   \implies PO_1^2\left(PQ^2\right)&=QO_2^2\left(PQ^2\right)\\[0.5cm]
   \implies PO_1^2&=QO_2^2\\[0.5cm]
   \implies PO_1&=QO_2
   \end{align*}
   $$  
   {:.math}

Es decir, la condición planteada en el problema se cumple si \\(PO_1=QO_2\\).

Podemos finalizar de la siguiente manera: \\(PO_1\parallel QO_2\\) y \\(PO_1\perp PQ\\) implican que \\(PQO_2O_1\\) es un rectángulo y \\(PQ\parallel O_1O_2\\). Como las circunferencias son tangentes en \\(R\\), \\(R\\) pertenece al segmento \\(O_1O_2\\). Esto significa que \\(\angle QO_2R=90^\circ\\). Adicionalmente \\(O_2Q=O_2R\\), por lo que \\(\angle QRO_2=45^\circ\\). Como \\(PQ\parallel O_1O_2\\), se tiene que \\(\angle QRO_2=\\) \\(\angle PQR=45^\circ\\)




<script type="text/javascript">
				function perspective(p){
					updateHelp(p);
					ggbApplet.setPerspective(p);
				}
                var P1 = {
                        "id":"P1",
                        "material_id":"dgx9ysex",
                        "appName":"geometry",
                        "width":800,
                        "height":300,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-app",
                        "allowUpscale":true
                        };
                var Applet_P1 = new GGBApplet(P1, '6.0', 'P1');
                var P1_S1_1 = {
                        "id":"P1_S1_1",
                        "material_id":"hvhpngtr",
                        "appName":"geometry",
                        "width":800,
                        "height":300,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-app",
                        "allowUpscale":true
                        };
                var Applet_P1_S1_1 = new GGBApplet(P1_S1_1, '6.0', 'P1_S1_1');
                var P1_S1_2 = {
                        "id":"P1_S1_2",
                        "material_id":"g987kdwu",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-app",
                        "allowUpscale":true
                        };
                var Applet_P1_S1_2 = new GGBApplet(P1_S1_2, '6.0', 'P1_S1_2');
                var P2 = {
                        "id":"P2",
                        "material_id":"qgg493sv",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-app",
                        "allowUpscale":true
                        };
                var Applet_P2 = new GGBApplet(P2, '6.0', 'P2');
                var P3_S1_1 = {
                        "id":"P3_S1_1",
                        "material_id":"gcrsqbxh",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-app",
                        "allowUpscale":true
                        };
                var Applet_P3_S1_1 = new GGBApplet(P3_S1_1, '6.0', 'P3_S1_1');
                window.onload = function() { 
                  Applet_P1.inject('P1');
                  Applet_P1_S1_1.inject('P1_S1_1');
                  Applet_P1_S1_2.inject('P1_S1_2');
                  Applet_P2.inject('P2');
                  Applet_P3_S1_1.inject('P3_S1_1');
                }
</script>