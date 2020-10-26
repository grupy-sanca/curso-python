=======
Funções
=======

Função é uma sequência de instruções que executa uma operação de computação. Ao definir uma função, você especifica o nome e a sequência de instruções. Depois, pode utilizar (“chamar”) a função pelo nome.

A ideia é similar às funções matemáticas! Mas funções em uma linguagem de programação não realizam necessariamente apenas cálculos.

Vimos o ``type()``, um exemplo de função:

.. doctest::

        >>> type(23)
        <class 'int'>

        >>> type('textinho')
        <class 'str'>

Definindo funções
-----------------

Se quisermos uma função que ainda não existe em Python, temos que
*definí-la*.

Criando uma função simples::

        def NOME_DA_FUNÇÃO(LISTA DE PARÂMETROS):
            COMANDOS

.. warning::

        Coloque os dois pontos após definir a função!

.. note::
        Faça a indentação nas linhas abaixo da definição da função!

.. doctest::

        >>> def soma():
        ...     print(1 + 1)
        ...
        >>> soma()
        2

        >>> def soma():
        ...     return 1 + 1
        ...
        >>> soma()
        2

Qual a diferença entre utilizar ``print()`` e ``return()`` aqui em cima?!?

.. doctest::

        >>> def imprime_letra():
        ...     print("If you didn't care what happened to me. And I didn't care for you")
        ...
        >>> imprime_letra()
        If you didn't care what happened to me. And I didn't care for you

        >>> type(imprime_letra)
        <class 'function'>

        >>> def repete_letra():
        ...     imprime_letra()
        ...     imprime_letra()
        ...
        >>> repete_letra()
        If you didn't care what happened to me. And I didn't care for you
        If you didn't care what happened to me. And I didn't care for you

Funções com argumentos
----------------------

Queremos somar ``3`` com um número qualquer que insiro na função. Bora lá:

.. doctest::

        >>> def soma_valor(x):
        ...     return 3 + x
        ...
        >>> soma_valor(5)
        8

        >>> z = soma_valor(10)
        >>> z
        13

Que sem graça! Quero somar dois números quaisquer!

.. doctest::

        >>> def soma_dois_numeros(x, y):
        ...     return x + y
        ...
        >>> soma_dois_numeros(7, 4)
        11

Tenho dificuldade com a tabuada do 7! Ajude-me!

.. doctest::

        >>> def tabuada_do_7():
        ...     for i in range(11):
        ...         print (7 * i)
        ...
        >>> tabuada_do_7()
        0
        7
        14
        21
        28
        35
        42
        49
        56
        63
        70

Mai tá legal isso! Quero a tabuada do 1 ao 10 agora! Bora!

.. doctest::

        >>> def tabuadas():
        ...     for i in range(1, 11):
        ...         for j in range(1, 11):
        ...             print("{} * {} = {}".format(i, j, i * j))
        ...
        >>> tabuadas()
        1 * 1 = 1
        1 * 2 = 2
        1 * 3 = 3
        1 * 4 = 4
        1 * 5 = 5
        1 * 6 = 6
        1 * 7 = 7
        1 * 8 = 8
        1 * 9 = 9
        1 * 10 = 10
        2 * 1 = 2
        2 * 2 = 4
        2 * 3 = 6
        2 * 4 = 8
        2 * 5 = 10
        2 * 6 = 12
        2 * 7 = 14
        2 * 8 = 16
        2 * 9 = 18
        2 * 10 = 20
        3 * 1 = 3
        3 * 2 = 6
        3 * 3 = 9
        3 * 4 = 12
        3 * 5 = 15
        3 * 6 = 18
        3 * 7 = 21
        3 * 8 = 24
        3 * 9 = 27
        3 * 10 = 30
        4 * 1 = 4
        4 * 2 = 8
        4 * 3 = 12
        4 * 4 = 16
        4 * 5 = 20
        4 * 6 = 24
        4 * 7 = 28
        4 * 8 = 32
        4 * 9 = 36
        4 * 10 = 40
        5 * 1 = 5
        5 * 2 = 10
        5 * 3 = 15
        5 * 4 = 20
        5 * 5 = 25
        5 * 6 = 30
        5 * 7 = 35
        5 * 8 = 40
        5 * 9 = 45
        5 * 10 = 50
        6 * 1 = 6
        6 * 2 = 12
        6 * 3 = 18
        6 * 4 = 24
        6 * 5 = 30
        6 * 6 = 36
        6 * 7 = 42
        6 * 8 = 48
        6 * 9 = 54
        6 * 10 = 60
        7 * 1 = 7
        7 * 2 = 14
        7 * 3 = 21
        7 * 4 = 28
        7 * 5 = 35
        7 * 6 = 42
        7 * 7 = 49
        7 * 8 = 56
        7 * 9 = 63
        7 * 10 = 70
        8 * 1 = 8
        8 * 2 = 16
        8 * 3 = 24
        8 * 4 = 32
        8 * 5 = 40
        8 * 6 = 48
        8 * 7 = 56
        8 * 8 = 64
        8 * 9 = 72
        8 * 10 = 80
        9 * 1 = 9
        9 * 2 = 18
        9 * 3 = 27
        9 * 4 = 36
        9 * 5 = 45
        9 * 6 = 54
        9 * 7 = 63
        9 * 8 = 72
        9 * 9 = 81
        9 * 10 = 90
        10 * 1 = 10
        10 * 2 = 20
        10 * 3 = 30
        10 * 4 = 40
        10 * 5 = 50
        10 * 6 = 60
        10 * 7 = 70
        10 * 8 = 80
        10 * 9 = 90
        10 * 10 = 100


Argumento padrão
~~~~~~~~~~~~~~~~~

Em alguns casos é conveniente deixar um valor padrão para algum (ou alguns)
argumento(s) de uma função. Por exemplo, imagina uma função que soma dois ou
três números:

.. doctest::

        >>> def soma_numeros(x, y, z=0):
        ...     return x + y + z
        ...
        >>> soma_numeros(1, 2, 3)
        6
        >>> soma_numeros(4, 5)
        9

Assim podemos usar a mesma função `soma_numeros` para somar dois ou três
argumentos. Basta definir o valor do argumento na definição da função. Isso só
é permitido para os últimos argumentos, ou seja, todos os argumentos à direita
de um argumento padrão devem também ser um argumento padrão. Por exemplo:

.. doctest::

        # argumento 'normal' depois de um padrão
        >>> def soma_numeros(x, y=0, z):
        ...     return x + y + z
        ...
        Traceback (most recent call last):
          File "<stdin>", line 1
        SyntaxError: non-default argument follows default argument

        >>> def soma_numeros(x, y=0, z=0):
        ...     return x + y + z
        ...
        >>> soma_numeros(1, 2, 3)
        6

É possível também utilizar o retorno de uma função diretamente como argumento de outra.
Por exemplo, o resultado da função acima como argumento de uma outra função qualquer. No caso estamos utilizando
a mesma função. Assim:

.. doctest::

        >>> def soma_numeros(x, y):
        ...     return x + y
        ...
        >>> soma_numeros(1, soma_numeros(3, 4))
        8

O  retorno de `soma_numeros(3, 4)` é 7. Ao utilizar este valor como argumento da função `soma_numeros(1, 7)`, o retorno
é 8.

Recursão
--------

Este conceito é uma técnica de programação que envolve "chamar" a mesma função repetidas vezes até chegar na solução.

   .. note::

      Confira sua função recursiva para evitar de cair em um `loop` infinito!

Para que a função seja aplicada diversas vezes, o retorno da função deve conter a própria função. Por exemplo:

.. doctest::

        >>> def fatorial(n):
        ...     if n == 1:
        ...         return 1
        ...     else:
        ...         return n * fatorial(n-1)
        ...
        >>> fatorial(3)
        6

Vamos entender o que está sendo feito aqui.

O cálculo do fatorial de um número, por exemplo, o fatorial de 3 (ou 3!), é:

3! = 3 * 2 * 1

Por definição:

- 1! = 1
- 0! = 1

Então, para obter 3! pela função que escvrevemos, o 3 entra como argumento e é analisado no ``if`` e "cai" no
``else``, por não ser igual a 1.

Aqui é que a magia acontece! O retorno desta função será 3 multiplicado pela função ``fatorial`` (sendo utilizada
pela segunda vez) que irá fazer o cálculo com 2 agora como argumento. Da mesma forma, cai no `else` e
multiplica o valor de 2 pelo ``fatorial(1)``. Agora esta função "cai" no ``if`` e retorna 1. Ao retornar o valor 1 na
função anterior (``factorial(2)``), é feito o produto de 2 por 1 que resulta em 2. Este valor 2 é utilizado no retorno
da função anterior à esta (``factorial(3)``), sendo o retorno de 3 por 2, que resulta em 6.

Aqui uma ilustação para compreender estas etapas [1]_:

   .. figure:: images/recursion.png
      :align: center
      :width: 70%

Exercícios
----------

.. include:: exercicios_funcoes.rst


[1] `<https://www.programiz.com/python-programming/recursion>`_
