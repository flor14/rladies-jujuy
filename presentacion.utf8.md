---
title: "Produciendo mi próximo artículo científico con R"
subtitle: "Compendios de Investigación, Reproducibilidad e Interactividad en las publicaciones académicas"  
author: 
  - "Dra. Florencia D'Andrea"
date: '21/12/2020'
output:
  xaringan::moon_reader:
    seal: false # saco filmina de inicio
    lib_dir: libs
    css: xaringan-themer.css
    nature:
      highlightStyle: github
      highlightLines: true
      countIncrementalSlides: false
      beforeInit: "https://platform.twitter.com/widgets.js"
---







class: inverse, middle, center

<!--html_preserve--><div class="countdown" id="timer_5fdf892c" style="right:0;bottom:0;" data-warnwhen="0">
<code class="countdown-time"><span class="countdown-digits minutes">05</span><span class="countdown-digits colon">:</span><span class="countdown-digits seconds">00</span></code>
</div><!--/html_preserve-->

### Empezamos en 5 minutos
Tenes tiempo para irte a buscar el ☕ o preparar el agua para el 🧉

---

class: inverse, center, middle

### ¡Hola R-Ladies Jujuy!

![](https://media.giphy.com/media/3oge7Ve0gmIOhJkhOg/giphy.gif)

Felicitaciones por el primer meetup


---

class: middle

.pull-left[


Dra. y Prof. Cs. Biológicas

Instructora RStudio

Instructora The Carpentries

ReproHack core-team

R-Ladies global team

]
.pull-right[

<img src="https://res.cloudinary.com/flor/image/upload/v1608466115/template_primary_wahkz0.jpg" width="250" />

]
---

background-image: url(imagenes/jujuy-colores.png)
background-size: cover
class: bottom, inverse

### Produciendo mi próximo artículo científico con R 
#### Compendios de Investigación, Reproducibilidad e Interactividad en las publicaciones académicas



 .large[Florencia D'Andrea | R-Ladies Jujuy | 21 de Diciembre de 2020 
]

---

class: center, middle

### Licencia

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Licencia de Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Este obra está bajo una <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">licencia de Creative Commons Reconocimiento 4.0 Internacional</a>

---

class: inverse, middle, center

## ⚠
### ¡Atención! 
#### El foco de esta charla esta en el software y los datos 

---

<img src="imagenes/ResearchCycle.jpg" width="700" style="display: block; margin: auto;" />

.footnote[[Imagen: The Turing Way Community, & Scriberia (2020). ](http://doi.org/10.5281/zenodo.3695300)]
---

## Desafío
#### Código y datos disponibles

.bg-washed-green.b--dark-green.ba.bw2.br3.shadow-5.ph4.mt5[
#### **Ciencia abierta** práctica de dejar "los resultados primarios de investigaciones financiados con fondos públicos, los artículos y los datos sean accesibles al público en formato digital sin restricciones o con una restricción mínima".]


.footnote[[The Turing Way Community (2019)](https://the-turing-way.netlify.app/reproducible-research/open/open-resources.html) / 
[OECD (2015)](https://www.fct.pt/dsi/docs/Making_Open_Science_a_Reality.pdf)]

---

## Principios FAIR
#### Buenas prácticas para la gestión y administración de datos científicos

.pull-left[

<img src="imagenes/FAIRPrinciples.jpg" width="700" style="display: block; margin: auto;" />
]
.pull-rigth[


**"Acceso tan abierto como sea posible, tan cerrado como sea necesario" (abierto por defecto)**

Se requiere claridad y transparencia en torno a las condiciones que rigen el acceso y la reutilización.

]

#### **F**indable | **A**ccesible | **I**nteroperable | **R**eusable

.footnote[
[Mons *et al.* (2017)](https://content.iospress.com/articles/information-services-and-use/isu824) / [Imagen: The Turing Way Community, & Scriberia. (2020). ](http://doi.org/10.5281/zenodo.3695300)
]

---

<img src="imagenes/ReproducibleJourney.jpg" width="700" style="display: block; margin: auto;" />


.footnote[[Imagen: The Turing Way Community, & Scriberia (2020)]( http://doi.org/10.5281/zenodo.3695300)]

---

## Datos
 Son hechos u observaciones que proporcionan **evidencia**. 
 
--

## Software 
Es el resultado de un proceso creativo que **proporciona una herramienta** para hacer algo, por ejemplo, con datos.

> El software es ejecutable.

> El software a menudo se desarrolla usando otro software.

--

.footnote[[Lamprecht *et al.* (2020)](https://content.iospress.com/articles/data-science/ds190026)]

---

# **{**Definición**}**
### Software para investigación

.bg-washed-green.b--dark-green.ba.bw2.br3.shadow-5.ph4.mt5[
#### Es que se utiliza para generar, procesar o analizar los resultados para una **publicación** (ya sea en una revista, resumen para congreso, monografía, libro o tesis)
#### Puede comprender desde unas **pocas líneas de código** (...), hasta un paquete de software desarrollado profesionalmente.]

.footnote[[Hettrick *et al.* (2014)](https://doi.org/10.5281/zenodo.608046)]

---

---

### Diez argumentos en contra de la **ciencia abierta...**


####1. ... **no** es siempre abierta.

####2. ...**históricamente ha carecido de diversidad** y exhibido una cultura no inclusiva.

####3. ...se basa en el **pensamiento occidental**.

--

####4. La política de **mi instituto** nunca me permitiría compartir mi trabajo abiertamente.

####5. Mi trabajo no es lo **suficientemente** bueno para compartir.

.footnote[[Ten arguments against Open Science that you can win - Malvika Sharan](https://www.software.ac.uk/blog/2020-12-17-ten-arguments-against-open-science-you-can-win)]

---

### Diez argumentos en contra de la **ciencia abierta...**

####6. Le doy ventaja a mis **competidores**.

####7. Escribí este código **solo para mis datos**.

--

####8. **No puedo mantenerlo**, ¿por qué molestarme en compartirlo?

####9. ¿Qué pasa si la gente **juzga** mi código (...)?

####10. Mi trabajo **no será reconocido** y eso no va a ayudar a mi carrera.

--

###**... que puedes ganar:** 

[**Ten arguments against Open Science that you can win** - Malvika Sharan](https://www.software.ac.uk/blog/2020-12-17-ten-arguments-against-open-science-you-can-win)

---

<img src="imagenes/openresearch.jpg" width="700" style="display: block; margin: auto;" />

.footnote[[Imagen: The Turing Way Community, & Scriberia (2020)]( https://zenodo.org/record/4323154)]


---
## Los datos y el software se citan

**¿Sos autor/a de un artículo?**

* Incluí citas a datos y software en el manuscrito

* Publica tu propios datos y software y citalos también

<img src="imagenes/data_available.png" width="800" style="display: block; margin: auto;" />
.footnote[Más formas de citar datos en [The Turing Way Community (2019) - Credit for reproducible research](https://the-turing-way.netlify.app/reproducible-research/credit.html?highlight=cite%20data)]

---

class: middle, center

<blockquote class="twitter-tweet" data-lang="es"><p lang="es" dir="ltr">When authors say they will "make data available upon request"

'#OpenScienceGif </p>&mdash; Heidi Seibold (@HeidiBaya) <a href="https://twitter.com/HeidiBaya/status/1335897311931740163?s=20">7 December 2020</a></blockquote>




---

## Los datos y el software se citan
### Para quienes generan datos y software

* Depositalo/s en un repositorio "estable" (ej. Zenodo, Figshare, etc)

* Obtené una URLs permanente al repositorio como un `Digital Object Identifier (DOI)`

* Incluí un ejemplo de cómo citarlo en el README o documentación

<img src="imagenes/pwc.png" width="300" style="display: block; margin: auto;" />

.footnote[[The Turing Way Community (2019)](https://the-turing-way.netlify.app/reproducible-research/credit.html?highlight=cite%20data) / [Zenodo - DOI versioning](https://help.zenodo.org/#versioning)]

---

<img src="imagenes/DOI.jpg" width="800" style="display: block; margin: auto;" />

.footnote[[Imagen: The Turing Way Community, & Scriberia (2020)]( http://doi.org/10.5281/zenodo.3695300)]
---

<img src="imagenes/zenodo_versioning.png" width="900" style="display: block; margin: auto;" />
.footnote[[Zenodo Blog - Zenodo now supports DOI versioning!](https://blog.zenodo.org/2017/05/30/doi-versioning-launched/)]

---
class: inverse, middle, center

### Demo 1
### Zenodo

---

class: middle, inverse

### 👉 **Reproducibilidad** 

### Compendio de investigación

### Interactividad


---
class: center, middle



#fill: #FEFEFF
#lineWidth: 1
#zoom: 4
#direction: right

# direction: down | center 
#.resaltado: fill=#8f8 title=bold

[Reproducibilidad] -> [Empírica]
[Reproducibilidad] -> [<resaltado> Computacional]
[Reproducibilidad] -> [Estadística]
FALSETRUEFALSEFALSEFALSETRUE

.footnote[[Stodden (2014)](https://www.edge.org/response-detail/25340)]

---

class: center, middle, inverse

### En mi computadora pude reproducir mis resultados ...
### ¿puedo considerar que mi trabajo es reproducible? 

---

## ¿Qué pasa de acá a 10 años?

<img src="imagenes/nature1.png" width="500" style="display: block; margin: auto;" />

.footnote[[Artículo de Nature](https://www.nature.com/articles/d41586-020-02462-7)]

---

class: center, middle, inverse

## ¿Es suficiente compartir el código y los datos para que otros puedan reproducir mis análisis?

---

class: center, middle

<blockquote class="twitter-tweet" data-lang="es"><p lang="es" dir="ltr">Te pasan un código, preparate para gastar de 3 a 4 horas resolviendo todos los bugs para que funcione. 😒 </p>&mdash; Roxana Villafañe (@data_datum) <a href="https://twitter.com/data_datum/status/1338926940443521031?s=19">15 de Diciembre 2020</a></blockquote>


---
## Ejemplo


[`tidyr v1.0.0`](https://github.com/tidyverse/tidyr/releases) breaking changes 

* Aparecen las funciones `pivot_*()` que reemplazan a `gather()` y `spread()`

<img src="imagenes/tidyr.png" width="200" style="display: block; margin: auto;" />

.footnote[Logo de `tidyr` por [RStudio](https://rstudio.com/)]

---
class: inverse, middle, center

### Demo 2
### [Versiones](https://github.com/tidyverse/tidyr)
---
class: middle, center
## Reproducibilidad computacional
.bg-washed-green.b--dark-green.ba.bw2.br3.shadow-5.ph4.mt5[

#### Cuando se proporciona información detallada sobre software, hardware y detalles de implementación.

.tr[
 Stodden (2014)
]]

---
## Entorno computacional 

Características de una computadora que pueden afectar el comportamiento del trabajo realizado en ella, como:

* su **sistema operativo**

* qué **software** tiene instalado 

* las **versiones de paquetes** de software están instaladas

.footnote[[The Turing Way Community (2019)](https://the-turing-way.netlify.app/)]

---
class: middle, center

<img src="imagenes/ErrorManagement.jpg" width="500" style="display: block; margin: auto;" />
[Imagen: The Turing Way Community, & Scriberia. (2020)]( http://doi.org/10.5281/zenodo.3695300)

.bg-washed-green.b--dark-green.ba.bw2.br3.shadow-5.ph4.mt5[

#### "El software (...) con frecuencia se desarrolla para permitir el uso de otro software, lo que genera dependencias complejas, y **estos paquetes de software dependientes cambian a su vez con frecuencia**" 

.tr[[Katz *et al.* (2016)](https://doi.org/10.7287/peerj.preprints.2630v1)
]
]

---

## Hay varias formas de capturar entornos computacionales


* Sistemas de administración de paquetes (📦 `renv`)

* Binder

* Máquinas virtuales 

* Contenedores (ejemplo: [Docker](https://colinfay.me/docker-r-reproducibility/) 🐳 )


.footnote[[The Turing Way Community (2019)](https://www.turing.ac.uk/research/research-projects/turing-way-handbook-reproducible-data-science)]
---

# Paquete `renv`


-  🏁 `renv::init()` Se crea una librería asociada al proyecto dentro de la carpeta `renv`.

--

-  📸 `renv::snapshot()` Genera el archivo `renv.lock` con información de las dependencias al momento de hacer la instantánea (snapshot).

--

-  🌱 `renv::restore()` reproduce el entorno!
--


<img src="imagenes/renv.png" width="400" style="display: block; margin: auto;" />

.footnote[[* Lee más sobre `renv` aquí](https://environments.rstudio.com/snapshot.html#pre-requisite-steps)]

---
class: inverse, middle, center

### Demo 3
### `renv`

---

## Binder

[Post](https://florencia.netlify.app/es-es/2020/08/compartiendo-entornos-interactivos-y-reproducibles-en-r-con-binder.es-es/) sobre Binder en R-Ladies BA (incluye charla)

<iframe src="https://flor14.github.io/r_de_reproducibilidad/r_de_reproducibilidad.html#1" width="100%" height="400px"></iframe>


---

## Experiencia previa: publicación de código

<img src="imagenes/joss.png" width="500" />
.footnote[D’Andrea (2019). Journal of Open Source Software, 4(37), 785, https://doi.org/10.21105/joss.00785]

---

class: center, inverse, middle
# Ciencia **abierta** y **reproducible**

---

### Ventajas

* Fomenta las colaboraciones 🤝 (**GitHub/GitLab**)

* Permite seguir la historia de tu proyecto 📜 (Control de versiones **git**)

* Mejoras el flujo de trabajo ⚙️ (ej: `here`, trabajo con proyectos)

* Programación literaria ✍️ (`RMarkdown`)

---



---

## Ventajas

* Aumenta el impacto de las publicaciones 💥

* Algunas revistas lo solicitan 📰


---

## Desventajas 🥺

* Lleva **esfuerzo** preparar el código y las bases de datos para publicar

* Faltan incentivos

* Se crea una ventaja para los "competidores"

---

class: middle, center

.bg-washed-green.b--dark-green.ba.bw2.br3.shadow-5.ph4.mt5[
####"El hecho de que un análisis sea reproducible **no garantiza su calidad**, que este sea correcto o la validez de los resultados publicados" 

.tr[Peng (2011)
]

]


---

## ¿Un cambio cultural?

.pull-up[
<img src="imagenes/codecheck.png" width="400" style="display: block; margin: auto;" />
.footnote[[Codecheck](https://www.nature.com/articles/d41586-020-02462-7)]
 ]
 
.pull-down[
<img src="imagenes/codecheck2.png" width="700" style="display: block; margin: auto;" />

]

---
class: middle, center

## ¿Un cambio cultural?

<blockquote class="twitter-tweet" data-lang="ens"><p lang="en" dir="ltr">The advert asks for: 
"A commitment to following the best [..] practices in science, such as [..] sharing of computer code and writing reproducible research reports, [..]sharing of data whenever feasible"

Have you come across job descriptions asking for such a commitment before?</p>&mdash; ReproHack(@ReproHack) <a href="https://twitter.com/ReproHack/status/1296061566484385792?s=20">19 August 2020</a></blockquote>


.footnote[[Twitter ReproHack](https://twitter.com/ReproHack)]

---

## Reproducibilidad 

<img src="imagenes/CultureShift.jpg" style="display: block; margin: auto 0 auto auto;" />

.footnote[[Imagen: The Turing Way Community, & Scriberia. (2020)]( http://doi.org/10.5281/zenodo.3695300)]]


---


class: inverse, middle, center
# 🙌👩‍💻
# ¡Manos a la obra!

---
class: inverse, middle, center
## ¿En qué estoy trabajando?

---

## Postdoc 

> #### Desarrollo de herramientas informáticas para evaluar el riesgo de las aplicaciones de plaguicidas para los ecosistemas acuáticos



---
class: middle, center

> Mi trabajo implica usar **modelos** que simulan el destino ambiental de los **plaguicidas** luego de su aplicación. 

> En particular, el modelo que uso permite estimar concentraciones de plaguicidas en **cuerpos de agua superficiales**

<img src="imagenes/lagunas.png" width="859" style="display: block; margin: auto;" />
.footnote[Imagenes tomadas por [Julie Brodeur](https://twitter.com/julbrodeur)]
---

## Evaluación de Riesgo Ecotoxicológico (ERE)

* Riesgo de aplicaciones de **plaguicidas** sobre la **biota acuática**

* El riesgo se estima de la comparación ente ambas concentraciones


#fill: #FEFEFF
#lineWidth: 1
#zoom: 4
#direction: right

# direction: down | center 
#.resaltado: fill=#8f8 title=bold

[ERE] -> [<resaltado>caracterización de exposición | concentraciones de plaguicida]
[ERE] -> [caracterización de efecto | concentraciones relevantes toxicológicamente]
FALSETRUEFALSEFALSEFALSETRUE



---
## Mi próxima publicación  

.bg-washed-green.b--dark-green.ba.bw2.br3.shadow-5.ph4.mt5[

Statistically-based soil-climate scenarios for aquatic pesticide fate modelling and exposure assessment in the Pampa Region of Argentina.

]

---

# Bases de datos

Empleo distintas bases de datos:

* Suelo
* Fenología
* Hidrología
* Clima
* Propiedades de plaguicidas


#fill: #FEFEFF
#lineWidth: 1
#zoom: 4
#direction: right


# direction: down | center 
#.rlang: fill=#8f8 visual=ellipse title=bold

[base de datos 1] 
[base de datos 2] 
[base de datos n] FALSETRUEFALSEFALSEFALSETRUE



---

# Modelo

**Pesticide Water Calculator v1.52** (USEPA)
 
Automatización de corridas: 
117000 simulaciones =  30 años `*`  50 plaguicidas `*` 78 suelos - clima 



#fill: #FEFEFF
#lineWidth: 1
#zoom: 4
#direction: right


# direction: down | center 
#.high: fill=#8f8 title=bold

[base de datos 1] --> [<high>Modelo PWC]
[base de datos 2] --> [<high>Modelo PWC]
[base de datos n] --> [<high>Modelo PWC]FALSETRUEFALSEFALSEFALSETRUE

---

# Resultados

¡Una nueva base de datos!


#fill: #FEFEFF
#lineWidth: 1
#zoom: 4
#direction: right


# direction: down | center 
#.high: fill=#8f8 title=bold

[base de datos 1] --> [Modelo PWC]
[base de datos 2] --> [Modelo PWC]
[base de datos *n*] --> [Modelo PWC]
[Modelo PWC] -> [<high>Resultados]FALSETRUEFALSEFALSEFALSETRUE

---

# Las Figuras

Proceso los resultados con R. 


#fill: #FEFEFF
#lineWidth: 1
#zoom: 4
#direction: right


# direction: down | center 
#.rlang: fill=#8f8 visual=ellipse title=bold
#.high: fill=#8f8 title=bold

[base de datos clima] --> [Modelo PWC]
[base de datos suelo] --> [Modelo PWC]
[base de datos moléculas] --> [Modelo PWC]
[Modelo PWC] -> [Resultados]
[Resultados] - [<rlang> R]
[<rlang> R] -> [<high>Gráficos]
[<rlang> R] -> [<high>Tablas]
[<rlang> R] -> [<high>Mapas]
FALSETRUEFALSEFALSEFALSETRUE



---

class: inverse, middle, center

## ¿Y ahora? Publicar

---

class: middle, inverse

### Reproducibilidad

### 👉 **Compendio de investigación**

### Interactividad

---

## Compendio de investigación

.pull-left[

* **Organizar los archivos** de acuerdo a una convención prevalente.

* Proveer **separación entre los datos, métodos y resultados** expresando sin ambiguedades la relación entre las tres.

* Especificar el entorno (+ **reproducibilidad**).


]

.pull-right[
<img src="imagenes/ResearchCompendium.jpg" width="500" />
]

.footnote[[Marwick *et al.* (2018)](https://doi.org/10.1080/00031305.2017.1375986)]
---

## Compendio de investigación

.pull-left[

* **Convención**: Otra persona debería poder interpretar los nombres de los archivos y directorios. 

* **Marwick *et al.* (2018)** proponen utilizar la estructura de un paquete de R

* **El compendio puede tener distinta complejidad**
]

.pull-right[
<img src="imagenes/small_rc.png" width="400" />
]
.footnote[[Marwick *et al.* (2018)](https://doi.org/10.1080/00031305.2017.1375986)]
---

## ¿Que agrego cuando agrego un compendio de investigacion?


#fill: #FEFEFF
#lineWidth: 1
#zoom: 4
#direction: right


# direction: down | center 
#.rlang: fill=#8f8 visual=ellipse title=bold
#.high: fill=#8f8 title=bold

[base de datos clima] --> [Modelo PWC]
[base de datos suelo] --> [Modelo PWC]
[base de datos moléculas] --> [Modelo PWC]
[Modelo PWC] -> [Resultados]
[Resultados] - [<rlang> R]
[<rlang> R] -> [Gráficos]
[<rlang> R] -> [Tablas]
[<rlang> R] -> [Mapas]
[<rlang> R] -> [<high>Compendio de investigación]
FALSETRUEFALSEFALSEFALSETRUE

---

## Paquete `rrtools` 
#### Genera compendios de investigación en R

<img src="imagenes/rc-logo.png" width="100" />
[Paquete (no esta en CRAN)](https://github.com/benmarwick/rrtools)


.bg-washed-green.b--dark-green.ba.bw2.br3.shadow-5.ph4.mt5[
El objetivo de `rrtools` es proporcionar instrucciones, plantillas y funciones para hacer un compendio básico adecuado para escribir investigaciones reproducibles con R.]

.footnote[[Marwick *et al.* (2018)](https://doi.org/10.1080/00031305.2017.1375986)]
---

[Tutorial de Anna Krystalli, mejor recurso para aprender](https://annakrystalli.me/rrresearch/10_compendium.html)

✔️ Control de versiones

➕ Estructura de paquete de R

➕ Licencia

➕ Crear un README

➕ Agregar un DOI

➕ Agregar cómo se cita

✔️ Agregar una estructura de archivos `analysis/` y `data/`

✔️ Generar el manuscrito con código incluido en `RMarkdown` 

✔️️ Usar la plantilla del journal con el paquete `rticles`

✔️️ Manejar las dependencias 


---

### ¿Cómo compartir un Compendio de investigación?

.panelset[

.panel[.panel-name[Licencia]

* **Incluir un archivo con la licencia** indica a los demás cómo puede ser reutilizado tu trabajo.

<img src="imagenes/usethis.png" width="50" />

El paquete `usethis` incluye funciones que agregan la licencia que elijas a tu proyecto:


```r
library(usethis)
usethis::use_mit_license("Florencia D Andrea")
```
]

.panel[.panel-name[Control de versiones]

Sistemas de control de versiones como `Git` <ion-icon name="logo-octocat"></ion-icon> es la mejor manera de preservar el historial de cambios en el compendio de investigación.

* **Facilita la colaboración** privada entre colegas
sobre el proyecto 

* **Facilita la distribución y mantenimiento** del compendio en el futuro

]
.panel[.panel-name[Persistencia]

Asignarle una URLs permanente al repositorio como un `Digital Object Identifier (DOI)` <!--html_preserve--><i class="ai  ai-doi "></i><!--/html_preserve-->  

* osf.io <!--html_preserve--><i class="ai  ai-osf "></i><!--/html_preserve-->
 
* figshare.com  <!--html_preserve--><i class="ai  ai-figshare "></i><!--/html_preserve-->

* zenodo.org <i class="ai ai-zenodo ai-3x"></i>
]

]

.footnote[[Marwick *et al.* (2018)](https://doi.org/10.1080/00031305.2017.1375986)]


---

class: middle, inverse

### Compendio de investigación

### Reproducibilidad computacional

### 👉 **Interactividad**

---

## Comunicación de mis resultados

* Aplicación web (**shiny**)

* Gráficos interactivos (**plotly**)

* Papers interactivos y reproducibles (**artículo ejecutable**)

---


## Shiny

<img src="imagenes/shiny.jpg" width="100" />

[Ejemplo de shiny app parte de una publicación - Bernabeu et al (2017)](https://mybinder.org/v2/gh/pablobernabeu/Modality-switch-effects-emerge-early-and-increase-throughout-conceptual-processing/0a5542658914a6ed01cf8e96252c48bb5bcf8f18?urlpath=shiny/Shiny-app/)

Bernabeu, P (2017). Modality switch effects emerge early and increase throughout conceptual processing: Evidence from ERPs. Cognitive Science Society.

#### Ejemplos de Shiny apps publicadas en repositorios
EFSA. (2018, June 26). Shiny R tool for the automation of systematic reviews (Version v3). Zenodo. http://doi.org/10.5281/zenodo.1299654

---

# ¿Dónde publicar Software?

*[¿Dónde publicar Shiny apps?](https://community.rstudio.com/t/can-i-publish-a-shiny-app-in-a-scientific-journal-how-where/6306/8) - Hilo en el foro de  RStudio Community

* [In which journals should I publish my software?](https://www.software.ac.uk/which-journals-should-i-publish-my-software) By Neil Chue Hong. Software Sustainability Institute blog.


---

## Gráficos interactivos

<img src="imagenes/plotly.png" width="100" />

> "Los artículos científicos son cada vez más difíciles de leer; Si se usan adecuadamente, las figuras interactivas tienen el potencial de ayudar a contrarrestar esta tendencia. Esto es especialmente cierto para comunicar los hallazgos a los responsables políticos y al público en general en general" - [F1000 Research blog](https://blog.f1000.com/2017/07/19/so-long-static-we-now-support-interactive-ploty-figures-in-our-articles/)


## Artículo reproducible

[ELife Sciences / Artículo ejecutable](https://elifesciences.org/articles/30274/executable)

[stenci.la](https://stenci.la/)

---
class: inverse, middle, center

### Demo
### Artículo reproducible


---
class: inverse, middle, center

### Comunidades 



---
# ROpenSci


<img src="imagenes/ropensci.png" width="200" style="display: block; margin: auto;" />


[Web](https://ropensci.org/)

[Twitter de ROpenSci](https://twitter.com/rOpenSci)


---

# The Turing Way


<img src="imagenes/LogoDetailWithText.jpg" width="200" style="display: block; margin: auto;" />

Libro de [The Turing Way](https://the-turing-way.netlify.app/welcome)

[Twitter de The Turing Way](https://twitter.com/turingway)



---

# ReproHack

<img src="imagenes/reprohack.png" width="200" style="display: block; margin: auto;" />


[Twitter de ReproHack](https://twitter.com/ReproHack)

---

# ReproHack en [LatinR 2020](https://latin-r.com/blog/reprohack)

[Lista de reproducción con 6 charlas sobre reproducibilidad en español](https://www.youtube.com/playlist?list=PL9-E3cL2KgKliN3DFBWfUAUNXco_NOAMQ)

<!--html_preserve--><div class="shareagain" style="min-width:300px;margin:1em auto;">
<iframe src="https://flor14.github.io/latinr-reprohack/index.html#1" width="1600" height="900" style="border:2px solid currentColor;" loading="lazy" allowfullscreen></iframe>
<script>fitvids('.shareagain', {players: 'iframe'});</script>
</div><!--/html_preserve-->

---

<img src="imagenes/toronto.jpg" width="500" height="600" style="display: block; margin: auto;" />

---
class: inverse

## Recursos para consultar 📚💻

* [Canal de YouTube de R-Ladies](https://www.youtube.com/channel/UCDgj5-mFohWZ5irWSFMFcng)

* [R4DS en español - G. Grolemund y H. Wickham ](https://es.r4ds.hadley.nz/)

* [R Markdown: The Definitive Guide - Y. Xie, J. J. Allaire, G. Grolemund](https://bookdown.org/yihui/rmarkdown/)

* [Happy Git With R - J. Bryan, the STAT 545 TAs, J. Hester](https://happygitwithr.com/)

* [Mastering Shiny - H. Wickham](https://mastering-shiny.org/)

* [Become and R package developer! - M. Salmon](hhttps://new-r-dev.netlify.app/)

* [Interactive web-based data visualization with R, plotly, and shiny - C. Sievert](https://plotly-r.com/)

---

class: inverse

# Referencias

* Katz DS, Niemeyer KE, Smith AM, Anderson WL, Boettiger C, Hinsen K, Hooft R, Hucka M, Lee A, Löffler F, Pollard T, Rios F. 2016. [Software vs. data in the context of citation. PeerJ Preprints 4]( https://doi.org/10.7287/peerj.preprints.2630v1)

* Lamprecht, A. L., Garcia, L., Kuzak, M., Martinez, C., Arcila, R., Martin Del Pico, E., ... & McQuilton, P. (2020). Towards FAIR principles for research software. Data Science, 3(1), 37-59.

* [Lista de recursos sobre Research compendium](https://research-compendium.science/)

* [Library Carpentry: FAIR Data and Software](https://librarycarpentry.org/lc-fair-research/)

* Marwick, B., Boettiger, C., & Mullen, L. (2018). [Packaging data analytical work reproducibly using R (and friends). The American Statistician 72(1), 80-88.](https://doi.org/10.1080/00031305.2017.1375986)

* [OECD (2015), “Making Open Science a Reality”](https://www.fct.pt/dsi/docs/Making_Open_Science_a_Reality.pdf), OECD Science, Technology and Industry Policy Papers, No. 25,
OECD Publishing, Paris. http://dx.doi.org/10.1787/5jrs2f963zs1-en

---

class: inverse

# Referencias

* The Turing Way Community, Becky Arnold, Louise Bowler, Sarah Gibson, Patricia Herterich, Rosie Higman, … Kirstie Whitaker. (2019, March 25). [The Turing Way: A Handbook for Reproducible Data Science (Version v0.0.4). Zenodo. http://doi.org/10.5281/zenodo.3233986](https://the-turing-way.netlify.app/)

* Peng RD (2011), [Reproducible Research in Computational Science. Science 334(6060): 1226–1227](doi:10.1126/science.1213847)

* Stodden, V. (2014). [Online; accessed 27. May 2020]. URL: https://www.edge.org/response-detail/25340.

* Wilkinson, M., Dumontier, M., Aalbersberg, I. et al. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data 3, 160018 (2016). https://doi.org/10.1038/sdata.2016.18

* [Webpage Principios FAIR](https://www.go-fair.org/fair-principles/)

---

class: inverse

# Referencias
#### Herramientas en R / Charlas

* [Writing articles and reproducible documents R
Anna Quaglieri](https://rpubs.com/annaquagli/471405)

* [Reproducible Environments - RStudio](https://environments.rstudio.com/)

* [renv: Project Environments with R - RStudio blog](https://blog.rstudio.com/2019/11/06/renv-project-environments-for-r/)

* [Putting the R into Reproducible Research - Anna Krystalli](https://annakrystalli.me/talks/r-in-repro-research.html#1)

* [Improve your workflow for reproducible science - Mine Çetinkaya-Rundel](https://mine-cetinkaya-rundel.github.io/improve-repro-workflow-reproducibilitea-2020/slides/improve-repro-workflow-reproducibilitea-2020.pdf) 

#### Ilustraciones

* The Turing Way Community, & Scriberia. (2020, March 3). Illustrations from the Turing Way book dashes. Zenodo. http://doi.org/10.5281/zenodo.3695300

---

class: center, middle

## ¡Muchas gracias por su atención!

<br><br>
Dra. Florencia D'Andrea <br> **Investigadora postdoctoral** <br>
<!--html_preserve--><i class="fab  fa-github "></i><!--/html_preserve--> [@flor14]("http://github.com/flor14") <br>
<!--html_preserve--><i class="fab  fa-twitter "></i><!--/html_preserve--> [@cantoflor_87]("http://twitter.com/cantoflor_87")<br>
<!--html_preserve--><i class="fas  fa-link "></i><!--/html_preserve--> [florencia.netlify.app/es-es/]("https://florencia.netlify.app/es-es/")<br>

 <br> <br>

 Filminas disponibles [bit.ly/rladiesjujuy-1](https://flor14.github.io/rladies-jujuy/presentacion.html?panelset=licencia#1) 

---

background-image: url(imagenes/jujuy-colores.png)
background-size: cover

