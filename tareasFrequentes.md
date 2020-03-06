---
title: "Listado de Tarea y Responsabilidades"
subtitle: "A usar en caso de que el autor no se encuentre presente"
author: "Sebastián González"
date: "2020-03-05"
lang: "es"
titlepage: true
titlepage-color: 900C3F
titlepage-text-color: FFFFFF
titlepage-rule-color: 008000
---

# LISTADO DE TAREAS Y RESPONSABILIDADES
*Por Sebastián González*

## TAREAS FRECUENTES

> Tareas que se realizan con una frecuencia de 1 mes o más. Todo lo rutinario . Lo más básico de mi pega.

Tarea | Frecuencia
------|------------
[Chequeo general en SCADA](#chequeo-general-en-scada) | Todos los días
[Chequeo general en terreno](#chequeo-general-en-terreno) | 1 x semana
[Resumen operación centrífuga Alfa Laval](#resumen-operación-centrífuga-alfa-laval) | Cada lunes
[Ratios de la semana](#ratios-de-la-semana) | Cada martes
[Consignas de centrifugación](#consignas-de-centrifugación) | Todos los días
[Proyección de camiones](#proyección-de-camiones) | Todos los días
[Análisis avanzado de polímero](#análisis-avanzado-de-polimero) | 1 x mes
[Seguimiento concentraciones](#seguimiento-concentraciones) | 1 x semana
[Seguimiento preparación polímero](#seguimiento-preparación-polímero) | 1 x semana
[Revisar aforos Procesos](#revisar-aforos-procesos) | 1 x semana
[Actualizar indicador CAMBI](#actualizar-indicador-cambi) | Cuando lo pidan 

### CHEQUEO GENERAL EN SCADA

Listado general de los distintos puntos observados en SCADA. Suelo realizarlo cada mañana, pero no es mala idea darle unas cuantas vueltas a las patallas.

 - Centrífugas de espesamiento y deshidratación

Revisar los parámetros principales de operación, torque y VR. Dependiendo de la centrífuga los valores aproximados en los que se deberían encontrar. 

Tambien es bueno fijarse en los caudalemtros de lodo y polímero, ver que estén dosificando lo que corresponde al set point. En caso de que no corresponda fijarse en le PID, en todos los casos debe estar en **AUTO1**. En caos de que esté en AUTO1 pero aun así no cumple con el caudal, es necesario hacer un análisis más profundo. 

 - Pre-espesadores

Por lo general es buena idea que la extracción de los pre-espesadores sea pareja. En caso de que algún pre-espesador esté extrayendo mucho más que los otros corre el pelígro de que se desconcentre.

Otro consejo es asegurar de que la suma de las distintas extracciones sea similar al caudal total de alimentación de las centríguas, ajustar los caudales de los pre-espesadores tomando en cuenta este caudal.

 - Parámetros de las centrifugas

Revisar que los ratios sean los que se solicitaron. Pasa que muchas veces los operadores hacen ajustes de ratio dependiendo de lo observado en terreno. En caso de que eso pase la diferencia entre el valor ingresado y el set-point no debería ser muy grande.

Fijarse en el modo de operación del valor de pre-espesadores. Ahora contamos con dos sensores así que tenemos la opción de operar con cualquiera de estos, su promedio o el valor de laboratorio. Lo ideal sería operar con el valor de uno de los sensores.

![Modo de operación concentración cámara de reaireación](parametros_esp2.png){width=300px}

### CHEQUEO GENERAL EN TERRENO

Ronda realizada diariamente por las distintas áreas del taller de deshidratación.

A continuación se listan las distintas puntos con los que hay que estar atentos al momento de realizar el chequeo. 

#### Preparadoras de Polímero

 - Revisar los consumos de polímero

Los consumos de las unidades por área (espesamiento, deshidratación) deben ser similares. Si alguna unidad preparó mucho más que otra entonces esa unidad tendrá menor timepo de maduración. Hay que solicitar ajuste por parte de operaciones.

 - Revisar las válvulas de manifold, ver que estén configuradas como corresponde 

 - Asegurarse que las unidades *Coperion* estén en modo **Gravimétrico**, no **Volumétrico**. 

En caso de que no esté en modo gravimetrico, simplemente se aprieta el botón para cmabiar de modo. Una vez cambiado es buena idea hacerle un pequeño seguimiento al equipo, ya que a veces el cambio de modo se puede originar por problemas que hay que analizar más profundamente.

![Display unidad Coperion](coperion.jpg){width=300px}

 - Revisar el estado del polímero

 Observar como se ve la preparación. Idealmente debería ser una mezcla homogenea sin presencia de grumos.

 - Revisar la limpieza del área

Muchas veces la caida de las centrífugas está llena de polímero por los lados. En ese caso hay que solicitar apoyo a operación para que realicen limpieza del sector.

#### Centrifugas de Espesamiento

 - Revisar los resultados por centrífuga

Lo más rapido para no perder mucho tiempo en esto es revisar visualmente la calidad de los centrados. Por lo general Se espera que os centrados estén en nivel 1, lo que significa un centrado con 0 o pocos residuos solidos. En caso de que no esté en el nivel esperado se realiza un ajuste de **VR** (o de **torque** dependiendo del modo de operación)

![Display de control de centrífugas](centrifugas.jpg){width=300px}

> A mayor VR el centrado sale más claro, pero baja el torque. A mayor torque la sequedad del lodo aumenta. Ambas variables son inversamente proporcionales.

En caso de tener tiempo se puede tomar una muestra de lodo hacerle una sequedad en las termo del área.

OJO: En caso de que tanto el centrado como el lodo estén bajo lo esperado, lo más problable es que se esté subdosificando polímero, por lo que quedan dos opciones:

1. Es necesario subir el ratio de polímero

2. La concentración de lodo con la que están trabajando los equipos no corresponde, corregir.

![Centrado ejemplar](centrado_bueno.jpg){width=300px}

 - Revisar los centrados comunes

> Nunca le creas al centrado de una centrifuga.

Otra forma de ver los resultados de centrado es fijarse en los centrados comunes. Se sigue la misma lógica descrita anteriormente, el centrado debe cumplir con las espectativas de nivel. En caso de no cumplirlo hay que identifcar las centrífugas responsable y corregir. 

#### Pre-espesadores

 - Revisar los espejos

Tal cual como lo dice el título, de vez en cuendo es bueno ver como se encuentran los espejos para hacerse una idea de los sobrenadantes de los pre-espesadores.

 - Revisar el lodo pre-espesado

En caso de ser necesario (querer verificar la concentración marcada por los sensores, por ejemplo) se puede tomar una muestra de lodo pre-espesado y tirarla a la termo. Tomar en cuenta que la muestra debe ser tomada desde una bomba que se encuentre en operación.

![Camara de bombas de lodo espesamiento](camara_bomb_cent.jpg){width=300px}

### RESUMEN OPERACIÓN CENTRÍFUGA ALFA LAVAL

Actualmente no se ha realizado, pero hasta hace poco se solicitaba enviar una vez por semana un resumen de la operación en la centrífuga Alfa-Laval. La ruta con los archivos para realizar este seguimiento es la siguiente:

```
T:\PROCESOS\18. Seguimientos\Espesamiento\AlfaLaval
```
El archivo que hay que actualizar es la planilla *datosAlfaLaval.xlsx*. Este contiene dos hojas, *datosDia* y *muestrasPuntuales*. ambas deben contener todos los datos para la centrífuga A (para los días en la que operó). En caso de que falte un dato reemplazar con un promedio.

Con estos datos se puede contruir una comparativa de la carga total a la centrífuga A y su comparación con las otras centrífugas, normalmente representada como un gráfico de barras.

![Comparación de cargas alimentación centrífuga espesamiento](carga_al.png){width=300px}

En el mail tambien se incluyen datos como los resultados en un gráfico de sequedad vs. tasa de captura, pero eso es anexo. Lo más importante es el análisis de la carga con la que operó la centrífuga.

![Comparación de cargas alimentación centrífuga espesamiento](resultado_al.png){width=300px}

Yo cuento con un script en R para realizar esto de manera automatica, pero por falta de tiempo ustedes mejor lo hacen en excel. Al llegar les puedo enseñar lo básico para que por último puedan correr el script.

### RATIOS DE LA SEMANA

Todas las semanas operaciones realiza el conteo de polímero consumido semanalmente. Con estos datos yo realizo una comparación que muestras los ratios de espesamiento y deshidratación tanto para el consumo según **stock** (dato operaciones) como el dato según **SCADA**.

La ruta donde se encuentran los datos es la siguiente:

```
T:\PROCESOS\18. Seguimientos\Polimero
```
La planilla que se utiliza es *Comparativa Polímero Stock.xlsx* la cual continene 3 hojas. 

La primera *DatosDiariosSCADA* contiene información según SCADA y se actualiza automaticamente, por lo que no hay que meter mano.

La segunda *Datos semanales* contiene los datos de consumo obtenido por operaciones para cada polímero. Esta planilla se llena manualmente, por lo que hay que tener cuidado con lo que se ingresa, contiene el periodo de consumo por semana, el número de més, número de semana, área en la que se utilizó el polímero, tipo de polímero y el consumo segun stock y SCADA. OJO, operaciones envía los datos de consumo mensual, como en esta planilla se ven semanalmente, al dato informado por operaciones se le restan las semanas anteriores del mismo mes.

>Operaciones suele enviar los datos los días lunes, por lo que el periodo comprendido es de martes a lunes. Por este motivo la comparación de ratios se suele enviar los martes, para asegurarse de tener todos los datos del día lunea y calcular el ratio correcto para la carga de alimentación.

La tercera planilla es donde se reune el consolidado de la información. Estos datos se reyenan automaticamente por lo ingresado en las planillas anteriores. Lo unico que hay que hacer para ver el ratio correspondiente a stock o scada es cambiar la celda en la columna de ratio.

![Tabla de consolidado](pol_consolidado.png){width=300px}

Luego es tos datos se pegan en una tabla para ser enviados por correo.

![Tabla correo comparación de polímero](tabla_correo.png){width=300px}

### CONSIGNAS DE CENTRIFUGACIÓN

Datos que se envía todos los días en latarde, al momento de tener los datos de laboratorio del día. La ruta de acceso del archivo es la siguiente:

```
T:\PROCESOS\17. Datos Diarios\Consignas Centrífugación
```

Al abrir la planilla *Consignas de Centrífugas.xlsx* esta se actualiza con los datos del día y del día anterior pero la mayoría de los datos se ingresan manual. Incluye rangos de operación para las centrífugas en torque o vr y los ratios de polímero que se deben ultilizar.

![Sección de las consignas dedicada a deshidraatción](consig_dh.png){width=300px}

La hoja incluye un espacio para dejar objetivos a mejorar por centrífuga. Ejemplo: mejorar sequedad, centrado, bajar ratio, etc.

Al finalizar se crea una copia con los valores pegados para el día y se envía por correo.

### PROYECCIÓN DE CAMIONES

Proyección con los camiones necesario a sacar de planta para la semana. Se envía todos los días de semana a primera hora. La ruta donde se encuentran los archivos es:

```
T:\PROCESOS\17. Datos Diarios\Proyección de Camiones\2020
```

Actualmente el cálculo se realiza por medio de una script de python, pero todavía se puede realizar como se hace tipicamente, ya que la planilla se sigue utilizando.

### ANÁLISIS AVANZADO DE POLÍMERO

En evaluación si lo seguiremos realizando nosotros, ~~espero que no~~ o si pasara a laboratorio. Dudo que lo tengan que realizar en estas semanas así lo dejaré así por ahora....

### SEGUIMIENTO CONCENTRACIONES

El archivo que contiene los datos de los sensores de los pre-espesadores y los espesadores es el *Concentración Espesadores SCADA.xlsx*. Este se debe actualizar con los datos de concentración mínima, máxima y promedio. 

Este archivo se encuentra en la siguiente ubicación:
```
T:\PROCESOS\18. Seguimientos\Concentraciones Lab vs. SCADA
```
La planilla contiene las hojas **670**, **650** y **datos1650** con los vinculos para historian.

La hoja donde se pegan los datos finales son **Resumen670**, **Resumen650** y **1650prom**. Lo que hago apra facilitar el pegado de los datos es dejar los datos correspondientes como valor en las hojas destinadas para el minimo, máximo y promedio. Todos estos datos deben ir a parar a las hojas Resumen (para losdatos de 650 y 1650) o la hoja 1650prom, para los datos del sensor en linea.

Una vez actualizado este archivo se puede abrir la planilla *Comparativo Concentraciones Esp-Dig* ubicada en la misma dirección de la planilla anterior. En esta planilla se encuentran las gráficas de comparación.

### REVISAR AFOROS PROCESOS

Los datos de aforos se pueden encontrar en una de esta dos direcciónes:
```
T:\OPERACIONES\1. AFORO UNIDADES DE POLIMERO\Aforo Unidades Polímero 2020
o...
S:\OPERACIONES\14. AFORO UNIDADES POLIMERO\AFORO UNIDADES 2020
```
Este aforo debería realizarse todos los días, los resulatdos se presentan en una tabla como la expuesta a continuación:

![Resultados aforo de polímero](aforo_pol.png){width=300px}

En caso de existir desviación hay que analizar a que se debe. Es posible que sea necesario realizar aviso a intrumentación para que realicen ajustes al equipo.

## PRUEBAS

Listado de pruebas pendientes a realizar.

### LODO BIOLOGICO + PRIMARIO EN CENTRÍFUGA E

Prueba consistente en alimentar lodo biológico más una fracción de lodo primario a la centrífuga E de espesamiento. Se espera que esta fracción de lodo primario permita generar un ahorro en el polímero.

Estas pruebas vienen a ser la continuación de lo que ya se probó a nivel de laboratorio y terreno en presencia de Andritz, solo que ahora se espera lograr operar **en continuo**.

Actualmente contamos con todo lo necesario para realizar la prueba. Tenemos la bomba de lodo primario conectada a la linea de lodo de la centrífuga E.

![Bombas de lodo primario a centrífuga E espesamiento](bombas_primario.jpg){width=300px}

Tenemos el sensor de lodo primario con señal hacia SCADA.

![Sensor de lodo primario](sensor_lp.jpg){width=300px}

Y por último, contamos con un automatismo de seguiridad que detiene la bomba en caso de que la centrífuga se detenga.

Si quisieramos continuar con las pruebas sería neceasrio ir probando estos distintos componentes y asegurarse de que estén funcionando bien. 

Al tratarse de una prueba en continuo, no es necesario hacer muchas más aparte de asegurarse de que la bomba esté funcionando e ir registrando los datos:

- Cantidad de lodo biológico dosificado.
- Cantidad de lodo primario dosificado.
- Cantidad de polímero dosificado.
- Concentraciones de cada uno.
- Resultados de las muestras tomadas por operaciones

La cantidad de lodo primario debe ser baja.Segun lo visto en su momento, la carga másica de LP sebe ser ~10% de la carga total.

### PRUEBA 2 POLÍMERO EN CENTRIFUGA ESPESAMIENTO

Alimentación de dos polímeros distintos en una centrífuag de espesamiento. Actualmente se considera utilizar la centrífuga E para la prueba. 

Los dos polimeros se alimentan en distintos puntos de la linea de lodo. El polímero **SNF 4530** se alimenta a cabeza, donde normalmente se alimenta el polímero. Mientras que el polímero **DP8011** se alimenta a la altura del equipo Flomix, ubicado el primer piso del taller, a la altura de la cam1690.

![Punto de inyección polímero DP 8011](conexion_pol.jpg){width=300px}

En el segundo piso, a la altura de las centrífugas se encuentra la conexión que posibilita la alimentación del polímero SNF 4530 por medio de la bomba de la centrífuga F de espesamiento. Esto significa que al momento de la prueba la centrífuga F quedará inoperativa.

![Centrífuga E de espesamiento](cent_e.jpg){width=250px} ![Centrífuga F de espesamiento](cent_f.jpg){width=250px}

Existen por ahora algunos temas pendientes para poder empezar con esta prueba. Por un lado la valvula que evita el paso de polímero a la centrífuga F no se puede cerrar. Ya existe una aviso creado para que vean esto.

Otro punto a revisar es el automatismo para la detención de la bomba de polímero D en caso de que la centrífuga E se detenga. Se solicitó a Misael que revisara eso.

Los ratios de polímero a utilizar son los normales pero divido en dos. Si estamos con ratios de 12 entonces hay que utilizar 6 de ratio para el SNF 4530 y 6 para el DP 8011.

### SENSOR EN LINEA CENTRADO DESHIDRATACIÓN

Hay que ir realizando un seguimiento a este sensor. Actualmente la carpeta con el archivo de seguimiento se encuentra en la siguiente ruta:

```
T:\PROCESOS\18. Seguimientos\Deshidratacion\Sensor centrado DH
```
Consultar a Mauricio si es necesario seguir con la extracción de muestras para la comparación del sensor.

![Equipo de medición centrado deshidratación](centrado_linea.jpg){width=300px}


## PROYECTOS

> Todo lo que espero completar algun día ~~pero probablemente nunca termine~~.

* Arreglar la base utilizada por los seguimientos de espesamiento y deshidratación
    * Generar una versión preeliminar en excel
    * Generar la misma base pero en SQL
* Crear programa con GUI para realizar la proyección de camiones
* Crear programa con GUI para las instrucciones diarias.


