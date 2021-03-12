# Guión de la práctica "Cuantificación de la competencia intraespecífica en la gestión forestal: el caso de los pinares de repoblación"


> + **_Versión_**: 1.0.
> + **_Asignatura (grado)_**: Ecología (CCAA)
> + **_Autor_**: Curro Bonet-García (fjbonet@uco.es)
>
>   



## Objetivos y contextualización ecológica

Esta práctica tiene los siguientes objetivos competenciales y operacionales:

 + Competenciales: Se refiere al conjunto de habilidades o conocimientos que se espera que adquieran los estudiantes durante el desarollo de esta actividad.
   +    Familiarizarse con el concepto de flujo de trabajo como herramienta básica para planificar los procedimientos de análisis de datos.
   +    Comprender la importancia de la competencia intraespecífica en un caso de estudio concreto y real: manejo de pinares de repoblación.
   +    Mejorar la destreza de los estudiantes en el manejo de herramientas informáticas.
   +    Evocar el conocimiento previamente adquirido sobre sistemas de información geográfica.
 +    Operacionales: Son los objetivos que nos planteamos satisfacer durante el desarrollo de la actividad. En este caso el objetivo es responder a la siguiente pregunta: ¿Qué lugares de la zona de estudio ocupados por pinares de repoblación pueden recibir tratamientos selvícolas (y reducir la competencia intraespecífica) para promover el crecimiento de la vegetación natural?

El abordaje de la pregunta anterior se sustenta en los siguientes conceptos ecológicos:

 +    Restauración de ecosistemas degradados: los pinares de repoblación se implantaron en la península ibérica a mediados del siglo XX con el objetivo principal de frenar la erosión que afectaba a buena parte del territorio. Estos procesos erosivos ocurrían como consecuencia de un uso intensivo del territorio en los siglos anteriores (deforestación, cultivo de tierras marginales, etc.). En toda España se plantaron más de 1.5 millones de hectáreas de estas formaciones.
 +    Competencia intraespecífica: Los mencionados pinares no recibieron el tratamiento forestal adecuado durante décadas, por lo que en la actualidad se han convertido en masas densas, monoespecíficas y coetáneas. Esto los convierte en un "antroposistema" en el que la competencia entre individuos de la misma especie es el principal factor que condiciona su funcionamiento. La gran densidad limita su crecimiento y su transformación en masas más diversas. Además tienen gran riesgo de incendio forestal, afección por plagas, etc.
 +    Naturalización de pinares de repoblación: Se define como el conjunto de procedimientos que permiten la transformación de los pinares de repoblación en formaciones vegetales más alineadas con las características del territorio (ej. encinares, matorrales mediterráneos, etc.). Este proceso pasa por reducir la competencia intraespecífica mediante el "aclarado" (thinning) de dichos pinares. La reducción de la competencia permite la entrada de propágulos de otras especies, así como el crecimiento de los pinos que quedan en la masa.

[Esta](https://github.com/fjbonet/teaching_intraspecific_competence/blob/master/presentations_schemes/generalidades_pinares_reboblacion_lowres.pdf) presentación resume alguno de los elementos descritos anteriormente.

## Zona de estudio
Esta práctica se desarrolla en Sierra Nevada. La razón fundamental es que en ese macizo montañoso abundan los pinares de repoblación. En concreto hay unas 40.000 Has de pinares de repoblación, que suponen aproximadamente la mitad de toda la superficie boscosa de este espacio protegido. 

Este mapa muestra la ubicación de Sierra Nevada. Los pinares de repoblación son las formaciones de color verde oscuro que hay en la vertiente norte de la montaña. 

<iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d210192.78378166418!2d-3.1976269316260746!3d37.09960213399416!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e1!3m2!1ses!2ses!4v1584982155696!5m2!1ses!2ses" width="600" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>



## Flujo de trabajo general

La siguiente figura muestra el flujo de trabajo que seguiremos durante el desarrollo de la actividad. Se trata de un documento dinámico creado con una herramienta llamada [draw.io](https://www.draw.io/) . Puedes acceder a [este](https://drive.google.com/file/d/1--LHT3pof0kQduS_CRljo4is__Eeo3EE/view?usp=sharing) enlace para descargar el flujo de trabajo o también estudiarlo con detalle abajo. En caso de que lo hayas descargado, lo podrás abrir desde [draw.io](https://www.draw.io/) .

<iframe frameborder="0" style="width:100%;height:1171px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=pine_plantations_workflow.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fa%2Fgo.ugr.es%2Fuc%3Fid%3D1--LHT3pof0kQduS_CRljo4is__Eeo3EE%26export%3Ddownload"></iframe>



Para empezar, recordemos la pregunta planteada: Queremos identificar zonas del territorio que estén ocupadas por pinares de repoblación que sean susceptibles de recibir tratamientos forestales de reducción de la competencia intraespecífica (aclarado de pinares) con objeto de maximizar la regeneración de la vegetación natural. Es decir, de alguna manera queremos identificar las áreas del territorio que reúnan unas condiciones más adecuadas para soportar dichos tratamientos. O dicho de otra manera más, vamos a asignar una "puntuación" a los distintos pinares en función de que satisfagan o no una serie de criterios que consideramos importantes.

Así que el primer paso es identificar las variables ambientales y los criterios de manejo con los que vamos a trabajar. En nuestro caso serán los siguientes:



### **Densidad del pinar**

La densidad del pinar es el principal factor a considerar, ya que esta variable es la que condiciona la intensidad de la competencia intraespecífica. Dado que nuestro objetivo es reducir dicha competencia, consideraremos que los sitios más adecuados para recibir tratamientos selvícola son aquellos que tienen mayor densidad. 

Todo lo que vamos a trabajar en esta práctica tiene una componente espacial evidente. Así que trabajaremos con mapas. En este caso, el mapa de densidad procede de una imagen de satélite. Concretamente ha sido generada por una infraestructura de investigación denominada [Copernicus](https://www.copernicus.eu/en), que suministra multitud de información ambiental procedente de sensores remotos. Concretamente vamos a usar una imagen denominada [TCD](https://www.copernicus.eu/en) (Tree cover density), que muestra la densidad de árboles expresada en porcentaje. La imagen cubre buena parte de Europa, así que yo la he recortado y reproyectado para que se ajuste a lo que necesitamos. Así, la imagen con la que trabajaremos en la práctica se llama [TCD\_ pines\_23030.tif"](https://drive.google.com/open?id=1cvTqmuoFk4bJybxAz-fqDPw11JNg-pcv).

La variable "densidad del pinar" ha de ser transformada en un criterio espacializable. En este caso asumimos que **a más densidad mayor idoneidad para recibir tratamientos forestales**. Es decir, hay una relación **directa** entre la distribución de la variable (densidad) y el criterio (aptitud desde el punto de vista de la densidad). Dado que la densidad se expresa en porcentaje (de 0 a 100%), es muy fácil transformarla en un mapa de aptitud desde el punto de vista de la densidad. Lo veremos más adelante.



### **Distancia a manchas donadoras de semillas**

El proceso mediante el cual los pinares de repoblación son "invadidos" por vegetación natural depende en buena medida de la disponibilidad de propágulos de otras especies. Hay varios artículos que justifican esta afirmación ([1](https://esajournals.onlinelibrary.wiley.com/doi/abs/10.1890/08-1656.1), [2](https://esajournals.onlinelibrary.wiley.com/doi/abs/10.1890/12-0459.1)). Un pinar que esté lejos de una mancha de vegetación natural que suministre semillas, será invadido con menor probabilidad. Es decir, la distancia de cada punto del territorio ocupado por pinares a las manchas de vegetación natural más cercana, es importante para nuestro objetivo. En este caso la variable es "distancia de cada pinar a la mancha de vegetación natural más cercana". Su transformación a criterio implica tener en cuenta que **cuanto más distancia haya, menos adecuado será un punto del territorio para albergar tratamientos selvícolas**. Es decir, en este caso, la transformación de variable a criterio requiere usar una función invertida (a valores más altos de la variable corresponden valores más bajos de idoneidad o aptidud).

Como veremos en las siguientes secciones, obtendremos el mapa de distancias a partir de un mapa de usos y coberturas vegetales del suelo. 



### **Capacidad del suelo para retener agua**

Las plantas toman del suelo el agua que necesitan para vivir. Por ello es muy importante que el suelo tenga cierta cantidad de humedad. Esto es especialmente importante en ambientes mediterráneos como el nuestro, donde la sequía estival reduce notablemente la disponibilidad de agua en el suelo. Tendremos en cuenta esta variable de una manera muy rudimentaria que tiene en cuenta únicamente la topografía. Los lugares cóncavos tienden a acumular más agua que los convexos. Así, el grado de convexidad-concavidad del terreno nos ayuda a simular cómo se almacenaría el agua en el suelo. En estos casos se dice que usamos una variable fácil de obtener (concavidad-convexidad del territorio) como *subrrogado* de otra más compleja de calcular (humedad del suelo). Afortunadamente la [REDIAM](http://www.juntadeandalucia.es/medioambiente/site/rediam) (Red de Información Ambiental de Andalucía) suministra una capa que muestra la distribución de la curvatura de toda la región. Puedes descargarla [aquí](https://descargasrediam.cica.es/repo/s/RUR?path=%2F01_CARACTERIZACION_TERRITORIO%2F07_BASES_REF_ELEV%2F05_CURVATURA%2F01_PROYECTOS_REGIONALES%2F2006_07_AND_100m_026V_c%2FInfGeografica%2FInfRaster%2FETRS89_30%2FTIFF). He recortado esta imagen para que se ajuste a nuestra zona de estudio. Así se obtiene una capa llamada [cti\_pines.tif](https://drive.google.com/open?id=1TdL0UO04jF6LGfG1wWbUOns_vLiDAj4j). Esta capa contiene valores que van desde -0.37 hasta 0.32. Los valores más altos corresponden con lugares más convexos, es decir, sitios en los que se acumula menos agua (cumbres de montañas, divisorias de aguas). Por contra, los valores más pequeños corresponden con lugares cóncavos (cauces, barrancos, etc.). Al igual que en el caso anterior, a valores más altos de la variable corresponden valores más bajos de aptitud. Es decir, a menor índice de humedad del suelo mayor idoneidad desde el punto de vista de los objetivos de este trabajo. 

## Material de partida.
Aunque se irán detallando y describiendo a lo largo del guión, aquí tienes la lista del material que necesitas para ejecutar esta práctica:

+ Mapa de usos y coberturas vegetales del suelo de Sierra Nevada. Usaremos esta capa para generar el mapa de distancias de los pinares a las manchas de vegetación natural más cercana. [Este](https://youtu.be/RNQ7qwG5UDQ) video describe su estructura de datos: [_MUCVA\_25\_multi\_snevada.zip_](https://github.com/fjbonet/teaching_intraspecific_competence/raw/master/input/MUCVA_25_multi_snevada.zip)

+ Mapa de densidad de los pinares, expreasada en porcentaje: [_TCD\_pines\_23030.tif_](https://github.com/fjbonet/teaching_intraspecific_competence/raw/master/input/TCD_pines_23030.tif)

+ Mapa de humedad potencial del suelo basada en la topografía: [_cti\_pines\_23030.tif_](https://github.com/fjbonet/teaching_intraspecific_competence/raw/master/input/cti_pines_23030.tif)

+ Mapa de distribución de los pinares de repoblación en Sierra Nevada: [_pine\_plantations\_23030.tif_](https://github.com/fjbonet/teaching_intraspecific_competence/raw/master/input/pine_plantations_23030.tif)

  

## Secuencia de acciones

Las siguientes acciones se describen con la misma numeración que se representa gráficamente en [este](https://drive.google.com/file/d/1--LHT3pof0kQduS_CRljo4is__Eeo3EE/view?usp=sharing) esquema. 

### Creación del mapa de distancia a formaciones de vegetación natural. 
Para generar este mapa necesitamos contar con la distribución de los pinares de repoblación y con la de las formaciones vegetales que actuarán como donadoras de propágulos. Obtendremos ambos mapas a partir del mapa de usos y coberturas vegetales de Andalucía, generado por la [REDIAM](http://www.juntadeandalucia.es/medioambiente/site/rediam). En [este](https://descargasrediam.cica.es/repo/s/RUR?path=%2F01_CARACTERIZACION_TERRITORIO%2F06_USOS_COBERTURAS%2F02_MUCVA_25000%2FMUCVA25_Multitemporal) enlace puedes descargar el mapa completo (Andalucía). Y [aquí](https://www.youtube.com/watch?v=RNQ7qwG5UDQ) tienes un video en el que te cuento cómo está estructurado. Para esta práctica mejor usa [este](https://github.com/fjbonet/teaching_intraspecific_competence/raw/master/input/MUCVA_25_multi_snevada.zip) fichero de formas.

De manera resumida haremos lo siguiente: Crearemos un campo nuevo en el mapa de usos y coberturas anterior y asignaremos los valores 1 a todos los polígonos que tengan pinares, mientras que pondremos el valor 2 a todos los que sean considerados como fuentes de semillas. 

El algoritmo de QGIS que permite calcular el mapa de distancias necesita un raster como capa de entrada. Así que rasterizaremos el fichero de formas anterior. Una vez hecho esto podremos calcular la distancia entre todos los píxeles ocupados por pinares (1) y su mancha de vegetación natural más cercana (2).

Vamos con el paso a paso:

- **(1)** Crear un campo nuevo llamado _dist\_targe_ en la tabla de atributos del shapefile llamado _MUCVA\_multitemporal.shp_. Debe de ser un campo numérico.
- **(2)** Seleccionar los polígonos que tengan pinos. Para ello nos fijamos en el campo _DES\_UC07_, que contiene la descripción del uso del suelo en cada polígono en 2007. Veremos que hay una leyenda con muchos tipos. Buscamos aquellos que correspondan con bosques densos de coníferas. Y ejecutamos la siguiente consulta de selección con QGIS. Recuerda que hay que poner el nombre del cada campo cada vez que queremos seleccionar un tipo de uso. Y que el operador de unión es _OR_.

```r
"DES_UC07"  =  'FOR. ARBOL. DENSA: CONIFERAS' OR  
"DES_UC07"  =  'FOR. ARBOL. DENSA: QUERCINEAS+CONIFERAS' or 
 "DES_UC07" = 'MATORRAL DENSO ARBOLADO: CONIFERAS DENSAS' 

```
- **(2)** Ahora abrimos la tabla de atributos de la capa y hacemos que todos los registros seleccionados adquieran el valor de 1 en el campo _dist\_targe_. No olvides de guardar los cambios.
- **(3)** Repetimos la misma operación anterior, pero seleccionando los polígonos que tengan la palabra _Quercus_ o _quercínea_ en el campo _DES\_UC07_. 

```r
"DES_UC07" = 'FOR. ARBOL. DENSA: QUERCINEAS' or 
"DES_UC07"  ='MATORRAL DENSO' or  
"DES_UC07"  ='MATORRAL DENSO ARBOLADO: OTRAS FRONDOSAS' or
"DES_UC07"  = 'MATORRAL DENSO ARBOLADO: QUERCINEAS DENSAS' or
"DES_UC07"  = 'MATORRAL DENSO ARBOLADO: QUERCINEAS DISPERSAS' or
"DES_UC07"  =  'MATORRAL DISP. ARBOLADO: QUERCINEAS+CONIFERAS' or 
"DES_UC07"  = 'MATORRAL DISP. ARBOLADO: QUERCINEAS. DENSO' or
"DES_UC07"  = 'MATORRAL DISP. ARBOLADO: QUERCINEAS. DISPERSO'

```
- **(3)** Al igual que antes, haz que estos polígonos seleccionados tomen el valor 2 en el campo _dist\_targe_. Guarda los cambios.
- **(4)** Ahora rasterizamos el fichero de formas anterior con la opción _rasterizar_ de QGIS (menú raster -> conversion -> rasterizar). Aplicamos los siguientes valores a los parámetros necesarios:
  - _input layer_: _MUCVA\_25\_multi\_snevada.shp_
  - _field to use for a burn-in value_: _dist\_targe_
  - _output raster size units_: Georeferenced units
  - _Width/horizontal resolution_: 100m
  - _Height/horizontal resolution_: 100m
  - _output extent_: Selecciona la capa _TCD\_pines\_23030.tif_ para que QGIS copie de la misma la extensión del raster resultante. 
  - _output\_file_: _dist\_target.tif_. Recuerda guardar el archivo en un sito conocido por ti...
- **(5)** Creamos el mapa de distancia usando el algoritmo llamado _proximity raster_ (GDAL) en QGIS. Necesitamos añadir los siguientes parámetros:
  - _input\_layer_: _dist\_target.tif_
  - _band number_: 1
  - _A list of pixel values in the source image to be considered..._: Aquí debemos indicar los valores de nuestro raster inicial que son considerados como "fuentes" de semillas. En nuestro caso es el valor 2.
  - _distance units_: Georeferenced units.
  - _proximity map_ (mapa de salida): _distancia1.tif_

  O expresado en el lenguaje de QGIS:


```python  
  gdal_proximity.py -srcband 1 -distunits GEO -values 2 -nodata 0.0
   -ot Float32 -of GTiff "/tu ruta/dist_target.tif"
    "/tu ruta/distancia1.tif"
```

- **(6)** El mapa de distancias obtenido cubre toda la extensión de la zona de estudio. Pero a nosotros nos interesa conocer la distancia únicamente en los píxeles ocupados por pinares. Por eso, para borrar el resto, multiplicamos el mapa obtenido anteriormente (_distancia1.tif_) por el mapa que muestra la distribución de los pinares (pine\_plantations\_23030.tif). Para hacer esta operación usamos la calculadora de mapas. El raster resultante se llamará _dist\_nat.tif_


### Creación del mapa aptitud desde el punto de vista de la distancia.

-  **(7)** Ya tenemos el mapa de distancia de cada píxel de pinar a manchas donadoras de semillas. Ahora hemos de convertir la distribución de esa variable en un mapa de aptitud. Para eso aplicamos el criterio: **a más distancia menos aptitud**. Es decir, debemos usar una función de preferencia inversa. Debemos de transformar la leyenda del mapa obtenido para que asigne valores cercanos a 1 a las distancias más cortas y valores cercanos a 0 a las distancias más largas. 

-  Asumiremos que la relación entre la variable (distancia) y su aptitud es lineal e inversa. Es decir, necesitamos conocer los parámetros de una recta que cumple las características expresadas en el siguiente esquema:

![imagen](https://raw.githubusercontent.com/fjbonet/teaching_intraspecific_competence/master/presentations_schemes/funcion_pertenencia_inversa.png)

-  Para conocer los valores máximos y mínimos de la capa que queremos transformar en aptitud (_dist\_nat.tif_), vamos a las propiedades de la misma en QGIS y miramos en la pestaña "información".
-  Una vez obtenidos los valores de la función lineal, la introducimos en la calculadora raster:

```python  
  1/(100-7300.68505859375)*"dist_nat@1"-
  (7300.68505859375/(100-7300.68505859375))
 
```

- Le damos el nombre _apt\_distancia.tif_ al raster de salida. 


### Creación del mapa aptitud desde el punto de vista de la densidad de los pinares. 

-  **(8)** El mapa de densidad del pinar está expresado en porcentaje. Y el criterio que vamos a seguir es que **a más densidad más aptitud** para nuestro objetivo (queremos intervenir para reducir la competencia intraespecífica). Así que, en este caso, es muy fácil transformar la variable en un mapa de aptitud: basta con dividir por 100. Hacemos eso en la calculadora raster de QGIS y le damos el nombre _apt\_densidad.tif_ a la capa resultante. 
-  Aunque se trata de una división muy sencilla, incluyo abajo el esquema que aplicaríamos para generar la ecuación de la recta directa, en caso de que la capa original no tuviera valores de entre 0 y 100.


![](https://raw.githubusercontent.com/fjbonet/teaching_intraspecific_competence/master/presentations_schemes/funcion_pertenencia_directa.png)

### Creación del mapa aptitud desde el punto de vista de la humedad del suelo. 

-  **(9)** La capa _cti\_pines.tif_ muestra la distribución de la humedad potencial del suelo (en función del grado de concavidad del territorio). Ahora hemos de convertir la distribución de esa variable en un mapa de aptitud. Para eso aplicamos el criterio: **a más valor de CTI menos aptitud**. Es decir, debemos usar una función de preferencia inversa. Debemos de transformar la leyenda del mapa de humedad del suelo para que asigne valores cercanos a 1 a los sitios más cóncavos y valores cercanos a 0 a los más convexos. 

-  Asumiremos que la relación entre la variable (humedad potencial) y su aptitud es lineal e inversa. Es decir, necesitamos conocer los parámetros de una recta que cumple las características expresadas en el esquema usado para el mapa de distancia.

-  Para conocer los valores máximos y mínimos de la capa que queremos transformar en aptitud (_cti\_pines.tif_), vamos a las propiedades de la misma en QGIS y miramos en la pestaña "información".
-  Una vez obtenidos los valores de la función lineal, la introducimos en la calculadora raster:

```python  
  1/(-0.370579987764359-0.329879999160767)*"cti_pines_23030@1"-
  (0.329879999160767/(-0.370579987764359-0.329879999160767))
 
```

- Le damos el nombre _apt\_cti.tif_ al raster de salida. 

### Integración de los tres criterios: análisis multicriterio.

El análisis multicriterio es una técnica muy sencilla que permite conciliar en un mismo mapa criterios que pueden ser contradictorios. En nuestro ejemplo tenemos tres criterios y se trata de unificarlos en un único mapa que asigne un valor de aptitud global a cada punto ocupado por pinares de repoblación. Para agregar los tres criterios empezaremos asignando un peso a cada uno de ellos. La suma de los pesos ha de ser 1. El criterio que tenga más peso contribuirá en mayor medida al mapa final. Procedemos en dos pasos:

- **(10)** Asignación de pesos a cada variable. Por ejemplo:
  - _apt\_densidad.tif_: 0.6
  - _apt\_cti.tif_:0.1
  - _apt\_distancia_:0.3
- **(11)** Integración de las variables y sus pesos. El proceso se hace fácilmente con la calculadora de mapas. El resultado final es la suma del producto de cada criterio (capa _apt_) por su peso. Introducimos la siguiente ecuación en la calculadora raster:

```python  
  ("apt_densidad@1"*0.6)+("apt_cti@1"*0.1)+("apt_distancia@1"*0.3)
 
```
 - Llamamos _apt\_final.tif_ a la capa resultante.
 - Uno de los problemas del análisis multicriterio es que ocurre una compensación de criterios. Si una variable tiene un valor muy alto en un lugar determinado, puede que el resultado final en ese punto sea algo aunque su peso sea bajo. Esto puede hacer que lugares no adecuados sean etiquetados como sí adecuados. 
 - **(12)** El mapa resultante _apt\_final.tif_ tiene valores númericos que van de 0 a 1. A partir de este mapa debermos seleccionar aquellos píxeles que tengan una aptitud mayor. El resto los descartaremos porque no reunen los requisitos que hemos impuesto. Para hacer esta selección aplicaremos una operación muy común en análisis raster: [reclasificación](https://docs.qgis.org/3.4/en/docs/user_manual/processing_algs/qgis/rasteranalysis.html#qgisreclassifybytable). Consiste en reducir la diversidad de valores de un raster asigando nuevos en función de un rango. Por ejemplo, asignaremos el valor de 1 a todos los píxeles que tengan una aptitud igual o mayor de 0.8. Para hacer esto, construimos una tabla de reclasificación.
 - Buscamos el algoritmo "reclassify by table" en el buscador de procesos de QGIS. Añadimos los siguientes parámetros:
   - _raster layer_: _apt\_final.tif_
   - _reclassification table_: Abrimos la tabla y añadimos las siguientes filas:

   
   | Desde (Mínimo) | hasta (Máximo)| Valor nuevo|
|----------------:|------------:|---------:|
|0|0.9| 0|
| 0.9 | 1|1|
    - _reclassified raster_ (capa de salida): _apt\_final\_re.tif_


### Integración de los tres criterios: uso de operadores lógicos.

**(13)** Esta segunda forma de integrar los criterios es un _bonus_. No es obligatorio trabajar con ella durante la práctica. Los estudiantes que lleguen hasta aquí tendrán puntuación extra. Usamos esta técnica para evitar la compensación de criterios que comentábamos más arriba. 

En este caso usaremos operadores lógicos para integrar las tres capas. Consideraremos que un lugar es adecuado para satisfaer nuestros objetivos si cumple un criterio específico y una combinación de los otros dos. Es decir, pondremos como criterio fundamental que los lugares adecuados tengan una **alta densidad de pinos**. Si no se cumple este criterio, nunca se podrá obtener un valor alto al final del proceso de integración de las variables. Los otros dos criterios serán optativos entre sí. Es decir, seleccionaremos como lugares adecuados aquellos que **o bien están cerca de una mancha de vegetación natural, o bien tienen suelos potencialmente húmedos**. Es decir, en conjunto aplicaremos los siguientes criterios concatenados: Un lugar es considerado como adecuado si:

+ Tiene una alta densidad de pinos **Y**:
+ Está cerca de una mancha de vegetación natural **O** tiene suelos potencialmente húmedos. 

Para implementar esta operación en un SIG, usamos dos operadores matemáticos muy sencillos:

+ Valor **máximo** entre dos capas: es el equivalente al operador **O**. Si en un píxel hay valores altos de aptitud en una capa y bajos en otra, el resultado será alto, puesto que estamos eligiendo el máximo de ambos. Si la aptitud es alta en los dos casos, también seleccionaremos un valor alto. Es decir, se trata de un operador poco restrictivo.
+ Valor **mínimo** entre dos capas: es el equivalente al operador **Y**. Si en un píxel hay valores altos de aptitud en una capa y bajos en otra, el resultado será bajo, puesto que estamos eligiendo el mínimo de ambos. Solo si la aptitud es alta en los dos casos, seleccionaremos un valor alto. Es decir, se trata de un operador poco restrictivo.

Para aplicar estos operadores a nuestras capas, puedes usar el comando [mosaic de SAGA](https://gis.stackexchange.com/questions/150312/combining-multiple-overlapping-rasters-retain-maximum-value). Este comando está disponible en QGIS. No es obligatorio hacer esto, pero quién lo haga tendrá una puntuación mayor.

Una vez que obtengas la capa final usando estos operadores lógicos, tendrás que reclasificar el resultado siguiendo las instrucciones del paso **12**.




