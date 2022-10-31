Função Lambda
=============

A função lambda tem origem no lambda cálculo, iniciamente desenvolvido pelo matemático Alonzo Church. No Python é também chamada de função anônima e seu uso permite a criação rápida de funções sem que seja necessário nomeá-las. Uma função lambda pode receber n números de argumentos, mas possui uma única expressão.

No Python tem a forma: lambda <argumentos> : <expressão>

Como exemplo, a soma de três variáveis x, y e z utilizando-se o comando *lambda* fica da seguinte forma: 

.. doctest::

   >>> lambda x,y,z: x+y+z

No exemplo abaixo mostramos como uma mesma função pode ser escrita de duas formas, utilizando-se o comando *def* ou *lambda*. 

.. doctest::
>>> def duplica(x):
...   return 2*x
>>> duplica(5)
10
...
>>> duplica = lambda x: 2*x
>>> duplica(5)
10

Lambda e funções
----------------

O uso do lambda pode ser realizado dentro de outras funções. 
No caso abaixo a função *multiplica* retorna uma outra função definida pela expressão lambda. 
Passando-se o valor 3, é retornado uma função que realiza a multiplicação por 3: 
f(x) = 3x.

.. doctest::
>>> def multiplica(n):
...   return lambda x: n*x
...     
>>> multiplica(3)
<function __main__.multiplica.<locals>.<lambda>(x)>      
...
>>> triplica = multiplica(3)
>>> triplica(10)
30
...
>>> quadruplica = multiplica(4)
>>> quadruplica(10)
40

Lambda e strings
--------------

Assim como ocorre em funções criadas pelo comando *def*, outros métodos do Python podem ser utilizados na expressão da função *lambda*.
Abaixo mostramos alguns exemplos com manipulação de strings associado ao uso do *lambda*.

.. doctest::
>>> letra_maiuscula = lambda string: string[0].upper() + string[1:]
>>> letra_maiuscula('maria')
'Maria'
...
>>> inverte = lambda string: string[::-1]
>>> inverte('EDUARDO')
'ODRAUDE'
