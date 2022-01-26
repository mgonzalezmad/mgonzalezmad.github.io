---
layout: post
title: You're up and running!
published: true
---



Los incidentes de tránsito representan un gran porcentaje de las causas de mortalidad a nivel mundial, cada año se pierden aproximadamente 1.3 millones de vidas en consecuencia de estos. Por otro lado, las personas heridas son alrededor de 20 y 50 millones tienen algún traumatismo no mortal y muchos de estos generan algún tipo de discapacidad. 

Los accidentes traen consigo muchos problemas que quizás no se tienen mapeados directamente, con esto se hace referencia a lo que menciona tanto la OMS sobre las consecuencias y la magnitud de las pérdidas económicas para las personas afectadas, sus familias y los países en conjunto; pues el costo de los tratamientos y la pérdida de productividad (hablando de las personas que quedan discapacitadas o mueren, o inclusive el tiempo de trabajo que sus familiares sacrifican para atenderlos). Los incidentes de tránsito cuestan a la mayoría de los países el 3% de su PIB, demostrando así, que este tipo de incidentes afecta en un porcentaje algunos indicadores macroeconómicos.

# Planteamiento del problema

Es importante realizar un análisis de la accidentalidad en la ciudad de Medellín, pues las cifras en los países de ingresos bajos y medios producen aproximadamente el 93% de defunciones relacionadas con incidentes de tránsito a nivel mundial. También sería interesante revisar si quizás a largo plazo la reducción y el tratamiento de los mismos pueda disminuir (de alguna manera) los índices de pobreza, puesto que es una ciudad en la que una significativa cantidad de la población se dedica al trabajo informal o que incluye manufactura y una discapacidad puede impedirles la posibilidad de trabajo.

La aplicación tiene como finalidad predecir el número de incidentes viales teniendo en cuenta variables geográficas, fechas e información sobre los accidentes y su nivel de gravedad, esto para poder aplicar algún tipo de tratamiento en los sectores "problema", que ayude a definir la implementación de semáforos, cruces peatonales u otras alternativas que puedan reducir en alguna medida estas cifras.


# Base de datos

La base de datos proviene del MEData, que contiene datos s de la ciudad de Medellín para que estos puedan ser usados como  herramienta de gobierno, acción ciudadana y toma de decisiones. 

A continuación se muestra la descripción de la base: 

![_config.yml]({{ site.baseurl }}/images/tabla1_1.PNG)

![_config.yml]({{ site.baseurl }}/images/tabla2.PNG)

# Tratamiento de Datos

Antes de iniciar con el análisis descriptivo se procede a tratar la columna de fecha accidentes (la que viene en formato fecha) y se parte en 2 variables nuevas, la primera es la fecha en formado _ymd_ y la segunda es la hora del accidente en formato _hms_.

A partir de lo anterior se comienzan a crear columnas indicadoras que podrían tener algún aporte significativo a los modelos, como lo son la hora pico, días festivos o fines de semana. 
En hora pico marcamos 1 para los horarios de accidentes ocurridos entre las 7:00 y las 8:30 am para la mañana, y para la tarde los horarios comprendidos entre las 5:30 y las 7:00 pm, lo anterior basado en los horarios del pico y placa en la ciudad de Medellín que regían antes de la pandemia.

# Análisis Descriptivo

Se seleccionan las comunas necesarias para realizar el análisis, esto para tener un poco más de orden con el tratamiento y análisis de los datos. Las variables consideradas son: 

- YEAR, CBML, CLASE_ACCIDENTE, DISENO, GRAVEDAD_ACCIDENTE,MES,NUMCOMUNA,BARRIO,COMUNA,Fecha_accid,fecha, hora_acc,dia, hora_pico,FESTIVO y Fines_semana.

![_config.yml]({{ site.baseurl }}/images/img1_1.PNG)

Se observa que al rededor de un 66% de los accidentes son choques teniendo la mayor participación, la clase que le sigue es la de "otros" con un 11% del total y los atropellos y las caídas de ocupantes tienen una particiáción similar, con un  9% cada una.Por otro lado, los volcamientos y los incendios son las clases que menos se observan, pues en conjunto representan un 4% aproximadamente.

![_config.yml]({{ site.baseurl }}/images/img2_1.PNG)

Más de la mitad de los accidentes tienen heridos, para ser exactos un 55% de ellos, un 0.13% tiene personas muertas reportadas y el 44% aprox. que resta es atribuido a accidentes que solo tienen daños, es decir no reportan heridos y/o muertos. 



The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
