# Actividad integradora - Sistemas multiagentes

Samantha Sofía Bautista Gauna

[Github](https://github.com/samsbg/multiagentesEvidencia)

[Colaborative](https://colab.research.google.com/drive/1xTTaKVBKE1YjYvsJ5x4ZI-kM4hZAYzLt?usp=sharing)

### Describe la situación y/o problema a simular

La situación que se está tratando de simular es la limpieza de un espacio a traves de robots que limpian (roombas). Desde el principio las variables de la simulación, como son las dimensiones, cantidad de robots, porcetanje de suciedad y tiempo total maximo, son determinados por el usuario y el modelo continua hasta que el espacio se encuentre completamente limpio o el tiempo total maximo se haya superado.

### Describe los agentes involucrados así como sus acciones o percepciones

Se decidió que dentro de la simulación, cada espacio tuviera un agente, este siendo (2) el robot de limpieza, (1) un espacio sucio y (0) un espacio limpio. El robot de limpieza es el agente que más interactua con su ambiente debido a que se mueve a un cuadro adyacente de manera aleatoria, dejando atrás un espacio limpio y reemplaza cualquier agente que está en su nueva posición. Este también percibe a su entorno debido a que si se va a mover a una posición con un robot de limpieza, este no se mueve hasta la siguiente iteración. Finalmente los espacios sucios o limpios se quedan en su lugar y son eliminados de la cuadricula cuando un robot pase por ellos.

### Decribe como interactuan y se comunican dos o más agentes del mismo

En el caso de los robots de limpieza, cada uno decide una dirección aleatoria a cual moverse mientras esta se encuentre a un cuadro de distancia (también descrito como posición vecina), pero al hacerlo también checa si otro de robot de limpieza se encuentra en esa posición, en ese caso no se mueve.

### Describe el entorno

Como cada espacio es tomado por un agente, el entorno de cada uno son agentes tanto de robots de limpieza a espacios limpios o sucios.

### Identifica las variables y los parametros que determinan el funcionamiento del sistema

Las variables iniciales identificadas por el usuario son las dimensiones del espacio, cantidad de robots de limpieza, el porcentaje de celdas sucias y un tiempo maximo que puede tomar la simulación. A partir de ahí otras variables pertinentes son la cantidad de espacios limpios/sucios para determinar cuando termina la simulación y hacer análisis finales y una lista de todas las posciones por iteracción o paso del modelo para poder representar la simulación visualmente.

### Describe el proceso de la simulación

Para correr la simulación, lo primero que se busca son las variables iniciales provenientes del usuario, que son las dimensiones del espacio, cantidad de robots de limpieza, el porcentaje de celdas sucias y un tiempo máximo que puede tomar la simulación. A partir de ahí empieza el tiempo para medir cuanto la simulación va a tomar o si se llega a pasar el tiempo máximo. A partir de ahí crea el modelo con las variables iniciales, colocando todos los robots en la primera fila y el resto de los espacios (limpios o sucios) dependiendo del porcentaje inicial de espacios sucios. Finalmente en cada paso se mueve el robot a uno de sus epacios vecinos dejando un agente de espacio limpio atrás y reemplaza el nuevo espacio. Finalmente se repiten los pasos hasta que no haya espacios sucios o se pase del tiempo predetermiando.

### Discute clara y concisamente los resultados obtenidos

Los resultados obtenidos son más que nada las impresiones del espacio guardadas en una lista para poder visualizar el modelo y graficar el decremento de espacios sucios mientras que los robots limpian.