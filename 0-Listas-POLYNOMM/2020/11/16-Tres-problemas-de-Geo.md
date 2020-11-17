---
layout: default
title: Tres problemas de Geo
nav_order: 2020-11-16
description: "Tres problemas PolynOMM de Geometría"
last_modified_date: 2020-09-28T13:00:00+0000
grand_parent: Listas POLYNOMM
parent: POLYNOMM 2020
---

<link rel="stylesheet" href="{{ '/assets/css/just-the-docs-degNaranja.css' | absolute_url }}">
<script>
    jtd.setTheme('degNaranja');
</script>

# Tres problemas de <span class="deg-sitio deg-sitio-texto">Geo</span><i class="jpa-anim-rel-jack_o_lantern jpa-2em"></i>
{:.fs-9 .no-toc}

Una pequeña lista de problemas de Geometría creados por escritores de POLYN<span class="deg-sitio deg-sitio-texto">OMM</span>.
{:.fs-6 .fw-300}

16 de noviembre de 2020.

Geometría
{:.label .deg-geometria .deg-geometria-fondo}


### Problema &nbsp;<span class="deg-sitio deg-sitio-texto">1</span>
{: .no_toc}
<!--Diseñado por Alexis J.D.V.-->

Al interior de cada lado del triángulo \\(ABC\\) se trazan dos puntos que dividen al lado en tres segmentos de igual longitud. Sean \\(P\\) y \\(Q\\) los puntos marcados sobre el segmento \\(BC\\). A partir de los 6 puntos marcados, se divide el triángulo en  15 regiones como se muestra en la figura, donde a excepción de la región central (delimitada por los dos  segmentos paralelos a \\(BC\\), \\(PA\\) y \\(QA\\)), las regiones se pintan de naranja o negro, de manera que no haya dos regiones que compartan un lado del mismo color. Sea \\(A_1\\) el área total de las regiones coloreadas de naranja y \\(A_2\\) el área total de las regiones coloreadas de negro.

Encuentre \\(\frac{A_1}{A_2}\\).

<div class="geo-100"><div id="Problema1"></div></div>

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

<div class="geo-100"><div id="Problema2"></div></div>

Nota: *El valor de \\(\frac{A_iA_{i+1}}{A_{i+1}B_i}\\), que puede ser \\(\frac{1}{2}\\) o \\(2\\), no es necesariamente igual al valor de \\(\frac{A_jA_{j+1}}{A_{j+1}B_j}\\) para enteros no negativos distintos \\(i,j\\) .*

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
{:.math }

Encuentra la medida del ángulo \\(\angle PQR\\) en cada caso.


<script type="text/javascript">
				function perspective(p){
					updateHelp(p);
					ggbApplet.setPerspective(p);
				}
                var parametersProblema1 = {
                        "id":"Problema1",
                        "material_id":"dgx9ysex",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-100",
                        "allowUpscale":true
                        };
                var appletProblema1 = new GGBApplet(parametersProblema1, '5.0', 'Problema1');
                var parametersProblema2 = {
                        "id":"Problema2",
                        "material_id":"qgg493sv",
                        "appName":"geometry",
                        "width":800,
                        "height":450,
                        "autoHeight":true,
                        "scaleContainerClass":"geo-100",
                        "allowUpscale":true
                        };
                var appletProblema2 = new GGBApplet(parametersProblema2, '5.0', 'Problema2');
                window.onload = function() { 
                  appletProblema1.inject('Problema1');
                  appletProblema2.inject('Problema2');
                }
</script>