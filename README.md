# estrategia_comercial_simple

Si MA10 es mayor que MA50, el precio de las acciones es creído por algunos comerciantes, que subira en los próximos días. De lo contrario, el precio disminuirá.


si MA10 es mayor que MA50, compraremos y mantendremos una acción. Alternativamente hablando, vamos a prolongar una parte de las acciones.

A continuación, vamos a calcular el beneficio diario. Primero, creamos la variable Close1, que es el precio de cierre de mañana.
 A continuación, crearemos una nueva variable llamada "Ganancia", que de hecho es el beneficio diario.
 Si las acciones son iguales a 1, el beneficio diario es igual al precio de cierre de mañana menos el precio de cierre de hoy. Puede ser positivo o negativo. Si es negativo, perdemos dinero ese día. Si las acciones son iguales a 0, significa que no tenemos acciones a mano, el beneficio es igual a cero. Podemos trazar el beneficio y descubrir que en algunos días ganamos dinero, en otros días perdemos dinero.

 Podemos calcular la riqueza acumulada. Utilizamos el método DataFrame, Cumsum para calcular la suma acumulada y crear una nueva variable Riqueza. 

Luego, verificamos la parte de cola de DataFrame, y comprobamos si ganamos dinero o perdemos dinero. 

 En la última fila, el beneficio y la riqueza tienen valores NaN, porque esos rendimientos se calculan desde Close1, y Close1 se calcula usando shift (-1). 

Por lo tanto, para obtener una riqueza terminal usando loc, el nivel del índice debe ser ms.index [-2]. 

Luego, imprimimos la riqueza, que de hecho es una suma de ganancias. 

La media móvil durante un largo período refleja el cambio de precio a lo largo de la historia a largo plazo, que llamamos señal lenta. 
Creamos MA10 y MA50, que son señal rápida y señal lenta respectivamente. 
Luego, trazamos el precio de cierre MA10 y MA50. Si MA10 es mayor que MA50, el precio de las acciones es creído por algunos comerciantes, que sube en los próximos días. De lo contrario, el precio disminuirá.

![image](https://user-images.githubusercontent.com/91780371/220675255-1b9e8184-f63b-4ce9-9034-dd8c0b832770.png)


#####

mediante un gráfico se muestra  la ganancia o pérdida

![image](https://user-images.githubusercontent.com/91780371/220675922-84b7a273-301a-41c7-bea1-317dd958556b.png)




#####
![image](https://user-images.githubusercontent.com/91780371/220676421-9d6bb39f-0bf0-4654-81c3-aa2e06f7c0ae.png)
curva de rendimiento durante el periodo para las acciones de faceboock

####


![image](https://user-images.githubusercontent.com/91780371/220677361-e73857a0-9dae-4f4c-a4de-bf007a647164.png)
curva de rendimiento para las acciones de Microsoft



