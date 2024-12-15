SPIDER LAB GIFTS
================
Juan Jesús Oteros Rojas y Zaira Moreno Martín
2024-12-15

- [1. Introducción](#1-introducción)
- [2. Materiales y Métodos](#2-materiales-y-métodos)
- [3. Hipótesis y Resultados](#3-hipótesis-y-resultados)
- [4. Conclusión](#4-conclusión)
- [5. Bibliografía](#5-bibliografía)

<img src="Logo_UCO.png" style="width:10.0%" />

<!-- Para generar títulos, subtítulos etc se usa #, el número de # determina el estilo y el formato del texto -->

## 1. Introducción

<div style="text-align: justify;">

En la especie de araña *Pisaura mirabilis*, las arañas machos se casan
con las arañas hembras para que se apareen dándoles regalos envueltos en
seda. Los regalos nupciales, que consisten en donaciones de sustancias
nutritivas por parte de los machos hacia las hembras. Estos regalos
pueden tener varias funciones: atraer a las hembras, asegurar la
transferencia de esperma e incluso actuar como inversión parental a
través de los recursos nutricionales proporcionados.  
En esta especie en concreto se observa que a veces las arañas machos
hacen trampa. En lugar de envolver la comida en seda, envuelven algo
más, como trozos de una planta o un exoesqueleto de insecto vacío del
que ya han comido permitiendo a los machos ahorrar energía para su
propio beneficio reproductivo.[^1]

</div>

## 2. Materiales y Métodos

<!-- cargar las librerias que vamos a utilizar, queremos que el código se ejecute, pero no que aparezca en el documento final, también excluímos los avisos y mensajes -->
<!-- Leer los datos desde el fichero que está en la misma carpeta que el proyecto -->

Los datos de este proyecto fueron descargados desde
[kaggle](https://www.kaggle.com/datasets/mexwell/spider-lab-gifts/data).
En el proyecto se usaron 27 individuos macho de la especie *Pisaura
mirabilis*. La tabla original presentaba 13 columnas, nosotros hemos
seleccionado las columnas presentadas en la tabla 1.

<!--Creamos una tabla con los datos que se van a utilizar para tener una visión general-->

| FOOD.TREATMENT | SILK.WEIGHT..mg. | TOT.WRAPPING.DURATION..sec. | MALE.CEPH.WIDTH..mm. | MALE.MASS.BEFORE.TRIAL..mg. |
|:--:|:--:|:--:|:--:|:--:|
| WF | 0.111 | 169 | 4.580 | 135 |
| LF | 0.044 | 187 | 3.023 | 64 |
| LF | 0.043 | 150 | 3.570 | 68 |
| WF | 0.084 | 249 | 3.330 | 51 |
| WF | 0.185 | 576 | 4.790 | 144 |
| WF | 0.094 | 351 | 4.110 | 95 |
| WF | 0.140 | 529 | 3.666 | 90 |
| WF | 0.067 | 208 | 3.666 | 82 |
| WF | 0.123 | 456 | 3.520 | 74 |
| LF | 0.143 | 331 | 4.330 | 113 |

Tabla 1: Vista general datos

**Variable cualitativa -\>**  
FOOD.TREATMENT, que presenta dos dietas:  
**- WF:** Alta alimentación (2 arañas por semana)  
**- LF:** Baja alimentacion (1 araña por semana)

**Variables cuantitativas -\>**  
SILK.WEIGHT..mg.: Peso de la seda utilizada para envolver el regalo
(miligramos)  
TOT.WRAPPING.DURATION..sec.: Tiempo total que el macho pasó envolviendo
el regalo (segundos)  
MALE.CEPH.WIDTH..mm.: Ancho del cefalotórax de la araña macho
(milímetros)  
MALE.MASS.BEFORE.TRIAL..mg.: Masa de la araña macho antes de la prueba
(miligramos)

## 3. Hipótesis y Resultados

**H0: Afecta la dieta al tiempo de envoltura total.**  
**H1: No afecta al tiempo de envoltura la dieta.**.

![](ProyectoSpider_files/figure-gfm/Relacion%20entre%20dieta%20y%20tiempo%20de%20envoltura-1.png)<!-- -->

En este caso se acepta **la hipótesis alternativa**, la dieta no afecta
al tiempo de envoltura porque vemos que el dato de la **mediana** es
similar en ambas dietas, la alta alimentacion presenta **mayor
dispersión** ya que presenta valores mas extremos y por eso observamos
que la caja es de mayor tamaño.

<!-- insertar nueva página -->
**H0: Cambia la masa corporal masculina antes del experimento con las
diferentes dietas**  
**H1: No cambia la masa corporal masculina antes del experimento con las
diferentes dietas**

![](ProyectoSpider_files/figure-gfm/Relación%20entre%20masa%20corporal%20masculina%20antes%20del%20experimento%20y%20dieta-1.png)<!-- -->

En este caso se acepta **la hipótesis nula**, la dieta afecta a la masa
corporal del macho antes del experimento, porque vemos que el dato de la
**mediana** es mas bajo en la baja alimentacion (LF), por lo que los
individuos con alta alimentacion presentan **mayor masa corporal**.

**H0: Cambia el ancho del céfalotorax con el tipo de dieta**  
**H1: No Cambia el ancho del céfalotorax con el tipo de dieta**

![](ProyectoSpider_files/figure-gfm/Relación%20entre%20en%20ancho%20del%20céfalotorax%20y%20la%20dieta-1.png)<!-- -->

En este caso se acepta **la hipótesis alternativa**, la dieta no afecta
al ancho del cefalotórax del macho porque vemos que el dato de la
**mediana** es similar en ambas dietas, la alta alimentacion presenta
**mayor dispersión** ya que presenta valores mas extremos y por eso
observamos que la caja es de mayor tamaño.

**H0: El tiempo de envoltura es mayor cuanto mayor peso tiene la
seda**  
**H1: El peso de la seda no influye en el tiempo de envoltura**  
![](ProyectoSpider_files/figure-gfm/Relación%20entre%20el%20tiempo%20de%20envoltura%20y%20el%20peso%20de%20la%20seda-1.png)<!-- -->
<!-- Hemos realizado un modelo de regresión lineal para obtener datos estadísticos, que apoyen el gráfico pero que no se muestren completos en el documento de salida. En concreto nos interesa el p-Value -->

En este caso hemos realizado un modelo de regresión lineal, donde hemos
obtenido el **p-value: 0.009821**, sabiendo que si el valor es **p-Value
\< 0,05**, la relación entre el peso de la seda y el tiempo de envoltura
es significativa por lo que se acepta **la hipótesis nula**, el tiempo
de envoltura es mayor cuanto mayor peso tiene la seda.

**H0: La dieta afecta al peso de la seda**  
**H1: La dieta no afecta al peso de la seda**  
![](ProyectoSpider_files/figure-gfm/Relación%20entre%20la%20dieta%20y%20el%20peso%20de%20la%20seda-1.png)<!-- -->

En este caso se acepta **la hipótesis nula**, la dieta afecta al peso de
la seda, porque vemos que el dato de la **mediana** es mas bajo en la
baja alimentacion (LF), por lo que los individuos con alta alimentacion
presentan **mayor peso de al seda**.

Para llevar a cabo el análisis usamos R ([R Core Team
2024](#ref-R-base)) con las librerias dplyr ([Wickham et al.
2023](#ref-R-dplyr)) y ggplot ([Wickham et al. 2024](#ref-R-ggplot2);
[Wickham 2016](#ref-ggplot22016)). Para la creación de este informe
hemos utilizado el paquete knitr ([Xie 2024](#ref-R-knitr),
[2015](#ref-knitr2015), [2014](#ref-knitr2014)) y pandoc y para crear
PDFs tinytex ([Xie 2019](#ref-tinytex2019))

## 4. Conclusión

Una vez obtenidos todos los datos, podemos observar que la dieta no
afecta al tiempo de envoltura total ni al ancho del cefalotórax de los
machos, ya que son datos que no se ven afectados por el tipo de dieta
pero si por el desarrollo individual de cada macho antes de comenzar con
el experimento.  
Sin embargo la dieta si que afecta a la masa corporal y al peso de la
seda producida, lo que tiene sentido ya que los que presentan una alta
alimentacion, tendran mayor masa corporal y producción de seda.  
Por último, vemos que la duracion de la envoltura es mayor cuanto mayor
es el peso de la seda, como era de esperar ya que si la seda pesa mas,
es porque se ha dedicado mas tiempo a la envoltura.

## 5. Bibliografía

<div id="refs" class="references csl-bib-body hanging-indent"
entry-spacing="0">

<div id="ref-R-base" class="csl-entry">

R Core Team. 2024. *R: A Language and Environment for Statistical
Computing*. Vienna, Austria: R Foundation for Statistical Computing.
<https://www.R-project.org/>.

</div>

<div id="ref-ggplot22016" class="csl-entry">

Wickham, Hadley. 2016. *Ggplot2: Elegant Graphics for Data Analysis*.
Springer-Verlag New York. <https://ggplot2.tidyverse.org>.

</div>

<div id="ref-R-ggplot2" class="csl-entry">

Wickham, Hadley, Winston Chang, Lionel Henry, Thomas Lin Pedersen,
Kohske Takahashi, Claus Wilke, Kara Woo, Hiroaki Yutani, Dewey
Dunnington, and Teun van den Brand. 2024. *Ggplot2: Create Elegant Data
Visualisations Using the Grammar of Graphics*.
<https://ggplot2.tidyverse.org>.

</div>

<div id="ref-R-dplyr" class="csl-entry">

Wickham, Hadley, Romain François, Lionel Henry, Kirill Müller, and Davis
Vaughan. 2023. *Dplyr: A Grammar of Data Manipulation*.
<https://dplyr.tidyverse.org>.

</div>

<div id="ref-knitr2014" class="csl-entry">

Xie, Yihui. 2014. “Knitr: A Comprehensive Tool for Reproducible Research
in R.” In *Implementing Reproducible Computational Research*, edited by
Victoria Stodden, Friedrich Leisch, and Roger D. Peng. Chapman;
Hall/CRC.

</div>

<div id="ref-knitr2015" class="csl-entry">

———. 2015. *Dynamic Documents with R and Knitr*. 2nd ed. Boca Raton,
Florida: Chapman; Hall/CRC. <https://yihui.org/knitr/>.

</div>

<div id="ref-tinytex2019" class="csl-entry">

———. 2019. “TinyTeX: A Lightweight, Cross-Platform, and Easy-to-Maintain
LaTeX Distribution Based on TeX Live.” *TUGboat* 40 (1): 30–32.
<https://tug.org/TUGboat/Contents/contents40-1.html>.

</div>

<div id="ref-R-knitr" class="csl-entry">

———. 2024. *Knitr: A General-Purpose Package for Dynamic Report
Generation in r*. <https://yihui.org/knitr/>.

</div>

</div>

[^1]: Ghislandi PG, Beyer M, Velado P, Tuni C (2017). La envoltura de
    seda de los regalos nupciales ayuda al comportamiento engañoso en
    las arañas masculinas. Ecología conductual 28 (3), 744-749.
    <https://doi.org/10.1093/beheco/arx028>
