# dds-tp-pares
Punto 2 - Modelo de Dominio (40 puntos)
1. Modelar el dominio presentado utilizando el paradigma orientado a objetos, comunicando su solución mediante
un diagrama de clases. Si utiliza patrones de diseño, indíquelos y justifique su uso. NOTA: Puede ayudarse para
comunicar, además, con código, pseudo-código, prosa u otros diagramas (diagrama de secuencia, de estados,
entre otros). 
2. Ahora un transeúnte también podrá escoger un destino con varias paradas; esto es:
Posición actual -> primer destino -> segundo destino -> ... -> destino final.
Para esto, se deberá especificar la dirección exacta de cada destino y el orden en el que se recorrerán. Además,
el usuario deberá especificar si se detendrá N minutos en cada parada, o si irá avisando punto a punto su estado
de “salud” (si llegó bien).
Si se especifica que se va a detener en cada parada, entonces el sistema deberá ir calculando las demoras
aproximadas por secciones (demora de A->B, demora B->C, etc.); caso contrario, se deberá hacer un cálculo
aproximado total.
Extienda su solución para que soporte este nuevo requerimiento. Además, muestre mediante código o
pseudocódigo cómo implementaría el cálculo de demora aproximado.
