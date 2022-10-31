Função Lambda
=============

A função lambda tem origem no lambda cálculo, iniciamente desenvolvido pelo matemático Alonzo Church. É também chamada de função anônima no Python e seu uso permite a criação rápida de funções sem que seja necessário nomeá-las.

Np python tem a forma: 
lambda <argumentos> : <expressão>

No exemplo abaixo mostramos como uma mesma função pode ser escrita de duas formas, definindo-se função def ou usando lambda. 

.. doctest::
>>> def duplica(x):
      return 2 * x
>>> duplica(5)
10

>>> duplica = lambda x: 2 * x
>>> duplica(5)
10

