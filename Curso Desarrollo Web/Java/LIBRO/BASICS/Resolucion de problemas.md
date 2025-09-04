# 1. Analisis del problema 
En esta fase requiere definir el problema y especificar claramente la tarea que el programa debe realizar y el resultado o solucion que se espera; esta etapa se divide en varias fases:
* Comprender el problema 
* Entender y describir los requerimientos del problema
  Escpecificar si el programa requiere interaccion con el usuario para leer datos de entrada y salida o resultados
* Especificiar los datos supone describirlos y representarlos

Algunas preguntas que se puede realizar son: 
1. Que entradas requieren? Tipo y Cantidad
2. Cual es la salida deseada? Tipo y Cantidad
3. Que metodo produce la salida deseada? Que requisitos o necesidades adicionales para la solicion


# 2. Diseño del algoritmo
Despues de analizar el problema, y la descirpcion, tenemos que diseñar el algoritmo
EL algoritmo se puede expresar en un lenguaje de programacion diferente y ejecutarse en una computadora distinta

La especificacion dle orden en el que se realizan las intrucciones o acciones del programa se denomina *Control del programa* , se relaiza la instrucciones secuenciales o repetitivas(Blucles o ciclos)

Las instrucciones de un programa tambien puedne ser conocidos como sentencias 

Cualquier software bien diseñado consta de un programa principal (Modulo de Alto nivel), al cual llama a los subprogramas (Modulos de bajo nivel) que a su vez ejecuta otros subprogramas

El proceso es el siguiente:

1. Programa un Modulo
2. Comprobarlo
3. SI es necesario, depurarlo
4. Combinarlo con modulos anteriores


Como ultimo paso para el diseño del algoritmo, se debe comprobar y verificar su exactitd; es decir que produzca un resultado en un tiempo finito 



Para todo esto, se puedne expresar y representar graficamente por medio de formulas, diagramas de flujo N-S y pseudocodigo

### Ejemplo de Pseudocodigo de Ir al Cine

1. Inicio
2. Ver cartelera de cines en Internet
3. Si no proyectan Harry Potter  **Entonces
	1. Decidir otras actividades. 
	2. Bifurcar paso 7
	3. sino
	4. ir al cine 
	5. fin_si
4. Hay fila **Entonces
	1. formarse
	2. **mientras** haya personas delante **hacer
		1. avanzar en la fila
	3. fin_mientras



# 3. Codificacion 
La codificacion es la escritura del lenguaje de programacion de la representacion del algoritmo desarrollada en las etapas precedentes.
Para convertir el algoritmo en programa se deben utilizar sustiuir las palabras reservadas en español con sus equivalentes en ingles y las operaciones indicadas en lenguaje natural por las correspondientes al lenguaje de programacion correspondiente 

# 4. Compilacion 
Examinar el codigo fuente, el algoritmo y en muchos casos, revisar las especificaciones y analisis del problema hasta que se ejecute conrecctamente y sin errores

# 5. Verificacion y depuracion 
Es el proceso de su ejecucion con una amplia variedad de datos de entrada llamados test, o prueba que determina si el programa tiene errores o no;  verificar supone el empleo de una amplia gama de datos de prueba, tales como valores normales de entrdaa, valores extremos de entrada, etcetera para comprobar los limites y aspectos especiales del programa

Los errores se pueden verificar y hallar si son:

1. **Errores de Compilacion**
	Normalmente son errores de sintaxis que se producen por el uso incorrecto de las reglas de lenguaje
2. **Errores de Ejecucion**
	Se producen por instrucciones que la computadora puede comprender, pero no ejecutar
	Por ejemplo la division entre 0 y raices cuadradas de numeros negativos
3. **Errores Logicos**
	Se producen en la logica del programa y su fuente suele ser el diseño del algoritmo; estos son los mas dificiles de detectar oorque el programa puede funcionar y no producir errores de compilacion ni de ejecucion y solo pueden advertirse al obtener esultado incorrectos
	Suelen ser provocados en la fase de sueño dle algoritmo, modificado y cambiar el programa fuente 

# 6. Documentacion
Consiste en describir los pasos a seguir en el proceso de su resolucion; su importancia destaca por su decisiva influencia en el producto final

La documentacion puede ser Interna y Externa, la primera es la que se encuentra en las lines de comentarios, mientras que en la segunda se incluye en el analisis, diagramas de flujo o pseudocodigo 

Es vital para el mantenimiento y corregir futuros errores


## Documentacion Interna //

El objetivo del programador debe ser escribir codigos sencillos y limpios 


