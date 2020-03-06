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

![Modo de operación concentración cámara de reaireación](parametros_esp2.png)

### CHEQUEO GENERAL EN TERRENO

Ronda realizada diariamente por las distintas áreas del taller de deshidratación.

A continuación se listan las distintas puntos con los que hay que estar atentos al momento de realizar el chequeo. 

#### Preparadoras de Polímero

 - Revisar los consumos de polímero

Los consumos de las unidades por área (espesamiento, deshidratación) deben ser similares. Si alguna unidad preparó mucho más que otra entonces esa unidad tendrá menor timepo de maduración. Hay que solicitar ajuste por parte de operaciones.

 - Revisar las válvulas de manifold, ver que estén configuradas como corresponde 

 - Asegurarse que las unidades *Coperion* estén en modo **Gravimétrico**, no **Volumétrico**. 

En caso de que no esté en modo gravimetrico, simplemente se aprieta el botón para cmabiar de modo. Una vez cambiado es buena idea hacerle un pequeño seguimiento al equipo, ya que a veces el cambio de modo se puede originar por problemas que hay que analizar más profundamente.

![Display unidad Coperion](coperion.jpg)

 - Revisar el estado del polímero

 Observar como se ve la preparación. Idealmente debería ser una mezcla homogenea sin presencia de grumos.

 - Revisar la limpieza del área

Muchas veces la caida de las centrífugas está llena de polímero por los lados. En ese caso hay que solicitar apoyo a operación para que realicen limpieza del sector.

#### Centrifugas de Espesamiento

 - Revisar los resultados por centrífuga

Lo más rapido para no perder mucho tiempo en esto es revisar visualmente la calidad de los centrados. Por lo general Se espera que os centrados estén en nivel 1, lo que significa un centrado con 0 o pocos residuos solidos. En caso de que no esté en el nivel esperado se realiza un ajuste de **VR** (o de **torque** dependiendo del modo de operación)

![Display de control de centrífugas](centrifugas.jpg)

> A mayor VR el centrado sale más claro, pero baja el torque. A mayor torque la sequedad del lodo aumenta. Ambas variables son inversamente proporcionales.

En caso de tener tiempo se puede tomar una muestra de lodo hacerle una sequedad en las termo del área.

OJO: En caso de que tanto el centrado como el lodo estén bajo lo esperado, lo más problable es que se esté subdosificando polímero, por lo que quedan dos opciones:

1. Es necesario subir el ratio de polímero

2. La concentración de lodo con la que están trabajando los equipos no corresponde, corregir.

![Centrado ejemplar](centrado_bueno.jpg)

 - Revisar los centrados comunes

> Nunca le creas al centrado de una centrifuga.

Otra forma de ver los resultados de centrado es fijarse en los centrados comunes. Se sigue la misma lógica descrita anteriormente, el centrado debe cumplir con las espectativas de nivel. En caso de no cumplirlo hay que identifcar las centrífugas responsable y corregir. 

#### Pre-espesadores

 - Revisar los espejos

Tal cual como lo dice el título, de vez en cuendo es bueno ver como se encuentran los espejos para hacerse una idea de los sobrenadantes de los pre-espesadores.

 - Revisar el lodo pre-espesado

En caso de ser necesario (querer verificar la concentración marcada por los sensores, por ejemplo) se puede tomar una muestra de lodo pre-espesado y tirarla a la termo. Tomar en cuenta que la muestra debe ser tomada desde una bomba que se encuentre en operación.

![Camara de bombas de lodo espesamiento](camara_bomb_cent.jpg)

### RESUMEN OPERACIÓN CENTRÍFUGA ALFA LAVAL

Actualmente no se ha realizado, pero hasta hace poco se solicitaba enviar una vez por semana un resumen de la operación en la centrífuga Alfa-Laval. La ruta con los archivos para realizar este seguimiento es la siguiente:

```
T:\PROCESOS\18. Seguimientos\Espesamiento\AlfaLaval
```
El archivo que hay que actualizar es la planilla *datosAlfaLaval.xlsx* 

### RATIOS DE LA SEMANA
```
T:\PROCESOS\18. Seguimientos\Polimero
```


### CONSIGNAS DE CENTRIFUGACIÓN
```
T:\PROCESOS\17. Datos Diarios\Consignas Centrífugación
```

### PROYECCIÓN DE CAMIONES
```

```

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

![Resultados aforo de polímero](aforo_pol.png)

En caso de existir desviación hay que analizar a que se debe. Es posible que sea necesario realizar aviso a intrumentación para que realicen ajustes al equipo.

## PRUEBAS

### LODO BIOLOGICO + PRIMARIO EN CENTRÍFUGA E

![Bombas de lodo primario a centrífuga E espesamiento](bombas_primario.jpg)



![Sensor de lodo primario](sensor_lp.jpg)


### PRUEBA 2 POLÍMERO EN CENTRIFUGA ESPESAMIENTO

![Centrífuga E de espesamiento](cent_e.jpg){width=250px} ![Centrífuga F de espesamiento](cent_f.jpg){width=250px}

### SENSOR EN LINEA CENTRADO DESHIDRATACIÓN

![Equipo de medición centrado deshidratación](centrado_linea.jpg)


## PROYECTOS

> Todo lo que espero completar algun día ~~pero probablemente nunca termine~~.

* Arreglar la base utilizada por los seguimientos de espesamiento y deshidratación
    * Generar una versión preeliminar en excel
    * Generar la misma base pero en SQL
* Crear programa con GUI para realizar la proyección de camiones
* Crear programa con GUI para las instrucciones diarias.


