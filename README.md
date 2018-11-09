# Clase de Python para implementar el algoritmo ID3
Este repositorio contiene el código para generar todos los resultados descritos en este [blog](http://menteartificial.com/sobre-la-dificultad-de-entrenar-redes-profundas/). El objetivo es crear una clase 'ID3_C' que implemente el algoritmo ID3 para tareas de clasificación.

# Contenido

`nodo.py`: Contiene la clase que representa a los nodos del árbol. Esta tiene 4 atributos: nombre, padre, hijos y arista. Tambien posee dos métodos auxiliares con el fin de buscar y agregar hijos al nodo.

`ID3_C.py`: Contiene la clase principal para generar el árbol de decisión. Los métodos más importantes de desta son:
1. 'entrenar': Toma como entrada la base de datos dividida en atributos (X) y en la variable objetivo(Y). Ambos deben de ser arreglos de NumPy, en dodne X es bidimensional y Y unidimensional.
2. 'predecir': Toma como parámetro un conjunto de patrones de entrenamiento X en forma de un arreglo bidimensional de NumPy y computa la predicción para cada una de sus instancias.

# Ejemplo de uso
Lo primero es importar la clase

```python
from ID3_C import ID3_C
import numpy as np
P.generate_seq(60)
```

Para generar predicciones sobre la base de datos 'futbol.csv' podríamos correr el siguiente código:

```python
datos = np.genfromtxt('futbol.csv', delimiter=",", dtype="str")

X     = datos[:, :-1]
Y     = datos[:, -1]

arbol = ID3_C()
arbol.entrenar(X, Y)
salida = arbol.predecir(X)
print('Porcentaje de aciertos: ', 100 * sum(Y == salida)/X.shape[0])
```
