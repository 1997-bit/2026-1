### a. Árboles Generales

Estructura de datos no lineal jerárquica donde cada nodo puede tener un número ilimitado de hijos. No hay restricción en cuanto a la cantidad de descendientes por nodo.

### b. Árboles Binarios

Árbol en el que cada nodo puede tener como máximo dos hijos: un hijo izquierdo y un hijo derecho.

### c. Árboles Binarios Distintos

Dos árboles binarios son distintos cuando tienen diferente estructura (forma), independientemente de los valores almacenados en sus nodos.

### d. Árboles Binarios Similares

Dos árboles binarios son similares cuando tienen exactamente la misma estructura (forma), sin importar los valores que contengan sus nodos.

### e. Árboles Binarios Equivalentes o Copias

Dos árboles binarios son equivalentes o copias cuando son similares en estructura y además contienen los mismos valores en cada nodo correspondiente.

### f. Árboles Binarios de Expresiones Aritméticas

Árbol binario usado para representar expresiones aritméticas, donde los nodos hoja son operandos (números o variables) y los nodos internos son operadores aritméticos (+, -, \*, /, ^). El nivel de un nodo indica implícitamente su precedencia de evaluación.

### g. Árboles Binarios de Búsqueda (ABB)

Árbol binario ordenado donde, para cada nodo N, todos los valores del subárbol izquierdo son menores que N, y todos los valores del subárbol derecho son mayores que N. Permite búsquedas eficientes.

### h. Árboles Binarios en Montón (Heap)

Árbol binario completo que cumple una propiedad de orden. En un Max Heap, el valor de cada nodo es mayor o igual que el de sus hijos. En un Min Heap, el valor de cada nodo es menor o igual que el de sus hijos.

### i. Nodos

Cada uno de los elementos que forman el árbol. Contienen información (dato) y referencias a sus nodos hijos.

### j. Nodo Raíz

Es el nodo principal o inicial del árbol. No tiene padre y es el único nodo sin antecesor. Todo árbol no vacío tiene exactamente una raíz.

### k. Nodo Padre

Nodo que tiene al menos un hijo. Es el antecesor directo de otro nodo en la jerarquía del árbol.

### l. Nodo Hijo

Nodo que desciende directamente de otro nodo (su padre). Todo nodo, excepto la raíz, tiene exactamente un padre.

### m. Nodo Hermano

Nodos que comparten el mismo nodo padre. Se encuentran en el mismo nivel del árbol.

### n. Nodo Terminal u Hoja

Nodo que no tiene hijos, es decir, su grado es cero. Se encuentra al final de una rama del árbol.

### o. Nodo Interno

Nodo que tiene al menos un hijo. Incluye todos los nodos del árbol excepto las hojas.

### p. Rama o Arista

Enlace o conexión entre dos nodos del árbol que representan una relación padre-hijo. En un árbol con N nodos existen exactamente N-1 ramas.

### q. Antecesor

Cualquier nodo que se encuentre en el camino desde la raíz hasta un nodo dado. El padre, el abuelo y todos los nodos superiores son antecesores de un nodo.

### r. Sucesor

Cualquier nodo que descienda de un nodo dado. Los hijos, nietos y todos los nodos inferiores son sucesores de un nodo.

### s. Grado de un nodo

Número de hijos que tiene un nodo. En un árbol binario el grado máximo es 2.

### t. Grado del árbol

Es el mayor grado entre todos los nodos del árbol. En un árbol binario el grado máximo del árbol es 2.

### u. Nivel

Indica la posición jerárquica de un nodo dentro del árbol. La raíz se encuentra en el nivel 0 (o 1, según la convención), y cada generación descendente incrementa el nivel en 1.

### v. Altura o Profundidad

Es el número máximo de niveles del árbol, es decir, la longitud del camino más largo desde la raíz hasta cualquier hoja. Un árbol con un solo nodo tiene altura 0 o 1 según la convención.

### x. Anchura

Es el número máximo de nodos que existe en cualquier nivel del árbol. Representa cuán "ancho" es el árbol en su nivel más poblado.

### y. Peso

Es el número total de nodos hoja (nodos terminales) que tiene el árbol. Representa la cantidad de nodos sin descendientes.

### z. Camino

Secuencia de nodos conectados consecutivamente por ramas, que va desde un nodo hasta otro. En un árbol existe un único camino entre cualquier par de nodos.
