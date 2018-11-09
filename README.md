# Sobre La Dificultad De Entrenar Redes Profundas
Este repositorio contiene el codigo para generar todos los resultados descritos en en este [blog](http://menteartificial.com/sobre-la-dificultad-de-entrenar-redes-profundas/). El objetivo es crear un generador de redes neuronales convolucionales simples para comparar su desempeño al variar el número de capas. 

# Contenido

`simpleNet.py` contiene el código para la generación de la red, la función principal a llamar es:

`simpleNet()`. Los parámetro de esta función son: num_layers = número de capas convolucionales que deseamos, num_maxPool = número de capas de muestreo requeridas, num_clases = número de clases a clasificar en nuestra base de datos, img_size = altura y longitud de las imagenes (por el momento solo funciona en imagenes de tres canales), batch_norm = valor booleano que especifica si implementar normalización en las capas previo a la aplicación de la función de activación.

`large_nets.py` contiene el código para la implementación y entrenamiento de la red.
