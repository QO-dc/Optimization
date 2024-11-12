# Optimization

# Tarea 1

## Caso 1: 

Este es un problema de optimización lineal en el que necesitamos minimizar el costo total de los suplementos mientras cumplimos con los requisitos diarios de nutrientes.

Se va a estructurarlo de la siguiente forma:

•	Variables de decisión:

o	x1x_1x1 = número de cápsulas de Vega Vita a comprar.
o	x2x_2x2 = número de cápsulas de Happy Health a comprar.

•	Objetivo: Minimizar el costo total:

Costo total=0.20⋅x1+0.30⋅x2\text{Costo total} = 0.20 \cdot x_1 + 0.30 \cdot x_2Costo total=0.20⋅x1+0.30⋅x2

•	Restricciones:

1.	Vitamin C: 20⋅x1+30⋅x2≥6020 \cdot x_1 + 30 \cdot x_2 \geq 6020⋅x1+30⋅x2≥60
2.	Calcium: 500⋅x1+250⋅x2≥1000500 \cdot x_1 + 250 \cdot x_2 \geq 1000500⋅x1+250⋅x2≥1000
3.	Iron: 9⋅x1+2⋅x2≥189 \cdot x_1 + 2 \cdot x_2 \geq 189⋅x1+2⋅x2≥18
4.	Niacin: 2⋅x1+10⋅x2≥202 \cdot x_1 + 10 \cdot x_2 \geq 202⋅x1+10⋅x2≥20
5.	Magnesium: 60⋅x1+90⋅x2≥36060 \cdot x_1 + 90 \cdot x_2 \geq 36060⋅x1+90⋅x2≥360

Resultado: [1] 3 2

3: Debe comprar 3 cápsulas de Vega Vita.
2: Debe comprar 2 cápsulas de Happy Health.

Este es el número óptimo de cápsulas de cada tipo que debes comprar cada día para cumplir con los requisitos mínimos de nutrientes, minimizando el costo total.

Así que, para satisfacer las necesidades de vitamina C, calcio, hierro, niacina y magnesio, deberías tomar 3 cápsulas de Vega Vita y 2 cápsulas de Happy Health.

## Caso 2: 

El objetivo es minimizar el número total de conductores necesarios para satisfacer la demanda en diferentes intervalos de tiempo durante el día. Los conductores tienen turnos de 8 horas y pueden tener tiempo ocioso dentro de esos turnos.

1.	Variables de decisión:

o	x1x_1x1 = número de conductores que comienzan su turno a las 0:00 (trabajan de 0 a 8).

o	x2x_2x2 = número de conductores que comienzan su turno a las 4:00 (trabajan de 4 a 12).

o	x3x_3x3 = número de conductores que comienzan su turno a las 8:00 (trabajan de 8 a 16).

o	x4x_4x4 = número de conductores que comienzan su turno a las 12:00 (trabajan de 12 a 20).

o	x5x_5x5 = número de conductores que comienzan su turno a las 16:00 (trabajan de 16 a 24).

o	x6x_6x6 = número de conductores que comienzan su turno a las 20:00 (trabajan de 20 a 4 del día siguiente).

3.	Objetivo: Minimizar el número total de conductores.

Minimizarx1+x2+x3+x4+x5+x6\text{Minimizar} \quad x_1 + x_2 + x_3 + x_4 + x_5 + x_6Minimizarx1+x2+x3+x4+x5+x6

5.	Restricciones: Asegurarnos de que se cubra la demanda en cada intervalo de tiempo:

o	De 0 a 4 am: Necesitamos 4 conductores.

o	De 4 a 8 am: Necesitamos 8 conductores.

o	De 8 am a 12 pm: Necesitamos 10 conductores.

o	De 12 pm a 4 pm: Necesitamos 7 conductores.

o	De 4 pm a 8 pm: Necesitamos 12 conductores.

o	De 8 pm a 12 am: Necesitamos 4 conductores.

Sistema de ecuaciones para las restricciones:

•	De 0 a 4 am: x1+x6≥4x_1 + x_6 \geq 4x1+x6≥4
•	De 4 a 8 am: x1+x2≥8x_1 + x_2 \geq 8x1+x2≥8
•	De 8 am a 12 pm: x2+x3≥10x_2 + x_3 \geq 10x2+x3≥10
•	De 12 pm a 4 pm: x3+x4≥7x_3 + x_4 \geq 7x3+x4≥7
•	De 4 pm a 8 pm: x4+x5≥12x_4 + x_5 \geq 12x4+x5≥12
•	De 8 pm a 12 am: x5+x6≥4x_5 + x_6 \geq 4x5+x6≥4

Resultado: [1]  4 10  0  8  4  0

El resultado [1] 4 10 0 8 4 0 que te muestra R corresponde al número óptimo de conductores que debes contratar para cubrir la demanda en cada franja horaria. Aquí está el desglose de lo que significa cada número:

4: Debes contratar 4 conductores para el turno que empieza a las 0:00 (trabajan de 0 a 8 am).

10: Debes contratar 10 conductores para el turno que empieza a las 4:00 (trabajan de 4 a 12 am).

0: No es necesario contratar ningún conductor para el turno que empieza a las 8:00 (trabajan de 8 a 4 pm), ya que la demanda ya está cubierta por otros turnos.

8: Debes contratar 8 conductores para el turno que empieza a las 12:00 (trabajan de 12 a 8 pm).

4: Debes contratar 4 conductores para el turno que empieza a las 16:00 (trabajan de 4 a 12 am).

0: No es necesario contratar ningún conductor para el turno que empieza a las 20:00 (trabajan de 8 pm a 4 am), ya que la demanda está cubierta por otros turnos.

Explicación:

El modelo de programación lineal ha optimizado el número de conductores necesarios para satisfacer la demanda en cada franja horaria de forma eficiente, minimizando el número total de conductores contratados.

Para cumplir con la demanda en las franjas horarias donde hay una alta demanda de conductores (como de 4 am a 8 am o de 12 pm a 4 pm), se contratan más conductores.
En las franjas horarias con menor demanda, como de 8 am a 12 pm y de 8 pm a 12 am, el número de conductores contratados es cero, ya que las demandas ya están cubiertas por los turnos anteriores.

En resumen, el resultado indica que para satisfacer la demanda de conductores, deberías contratar 4 conductores para el turno de 0:00, 10 para el de 4:00, 8 para el de 12:00, y 4 para el de 16:00, mientras que no necesitas contratar conductores para los turnos de 8:00 y 20:00.

# Tarea 2: 

Multicriteria Decision-Making

If you have the criteria: cost of living, language difficulty, possibilities to get a job in that country after studies are finished.
If you have the alternatives: Brazil, Spain, USA, Germany.
Create an AHP model and get the ranking.

Para realizar esta tarea se ha creado en el mismo R en base a opiniones personales una matriz capaz de explicar los diferentes criterios de selección

Criterios escogídos: 
1. Costo de vida 
costo_vida <- matrix(c(1, 1/3, 1/5, 1/5,
                       3, 1, 1/3, 1/3,
                       5, 3, 1, 1,
                       5, 3, 1, 1), 
                     nrow = 4, byrow = TRUE)

2. Dificultad de idioma 
dificultad_idioma <- matrix(c(1, 1, 1/3, 1/7,
                              1, 1, 1/3, 1/7,
                              3, 3, 1, 5,
                              7, 7, 1/5, 1), 
                            nrow = 4, byrow = TRUE)
3. Posibilidades de trabajo
trabajo <- matrix(c(1, 1/3, 1/5, 1/7,
                    3, 1, 1/5, 1/5,
                    5, 5, 1, 3,
                    7, 5, 1/3, 1), 
                  nrow = 4, byrow = TRUE)

Finalmente se combinana realizando un ranking final teniendo como resultado: 
[1] 0.07030307 0.12449081 0.44537582 0.35983030

Esto significa que el país EE.UU. tendría el puntaje más alto (0.445), seguido de Alemania (0.359), España (0.124) y Brasil (0.070), lo que indica que EE.UU. es el país mejor clasificado según los criterios de costo de vida, dificultad del idioma y posibilidades de trabajo.

## Tarea 3: 

1. Variable de Entrada: Gasto en Salud
El gasto destinado al sector salud (2007-2023) es un indicador de los recursos asignados a cada región. Esta información es usada como una variable de entrada (input), ya que representa el esfuerzo financiero para mejorar la salud en las áreas que estás comparando.

2. Variable de Salida: Tasa de Mortalidad en la Niñez
La tasa de mortalidad en la niñez es la variable de salida (output) porque mide un resultado directo de la efectividad del gasto en salud. Disminuciones en esta tasa pueden indicar una mejora en la eficiencia de los servicios de salud.

3. Posible Estructura de Análisis
Objetivo: Determinar qué tan eficientemente los recursos en salud han contribuido a la mejora de la tasa de mortalidad infantil en áreas commo "Total", "Urbana", "Rural", "Lima Metropolitana", "Resto Costa", "Sierra", "Selva", "Sin educación", "Primaria", "Secundaria", "Superior". 

Método: Utilizar herramientas de análisis de eficiencia, como el Análisis Envolvente de Datos (DEA), para comparar la eficiencia relativa de los municipios o regiones en el uso de sus recursos.

Para la elaboración del estudio se ha extraido dos datasets de la INEI:
https://m.inei.gob.pe/estadisticas/indice-tematico/health/
1. GASTO DESTINADO AL SECTOR SALUD, 2007- 2023
2. TASA DE MORTALIDAD EN LA NIÑEZ, SEGÚN PRINCIPALES CARACTERÍSTICAS, 2000-2019-2020-2021

Pasos usados para el proceso de análisis: 
1. Exportar y modificar los datos para que sean usados.
2. Crear un vetor de output y otro de input
3. finalmente realizar el análisis de eficiencia

![image](https://github.com/user-attachments/assets/6dfb65d7-d4b7-4d41-a4d2-a8148081acfe)

Interpretación de los resultados:

Valores de eficiencia:
Los valores 1.0000000 indican que esas unidades (en este caso, algunas categorías de mortalidad) están operando de manera eficiente, es decir, no se podría mejorar su rendimiento utilizando los recursos (gasto en salud) de manera más eficiente. Estas categorías están en el "frente de la frontera de eficiencia" en el modelo DEA.

Los valores menores que 1, como 0.9211729 o 0.8052624, indican que esas unidades no están utilizando los recursos de manera tan eficiente como las que tienen un valor de eficiencia de 1. Por ejemplo, una eficiencia de 0.9211729 sugiere que se podría mejorar en alrededor del 8% para alcanzar la eficiencia máxima.

Distribución de eficiencias:
Se observa que algunas categorías tienen eficiencia máxima (1.0), mientras que otras tienen valores inferiores, lo que sugiere que hay algunas áreas donde el gasto en salud no está siendo tan efectivo en la reducción de la mortalidad.

Url del Rstudio: 
https://qo-dc.github.io/Optimization/Index.html
