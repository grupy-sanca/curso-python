=======
Funções
=======

Função é uma sequência de instruções que executa uma operação de computação. Ao
definir uma função, você especifica o nome e a sequência de instruções. Depois,
pode utilizar (“chamar”) a função pelo nome.

A ideia é similar à função matemática! Mas funções em uma linguagem de
programação não realizam necessariamente apenas cálculos.

Vimos o ``type``, um tipo de função:

.. doctest::

        >>> type(23)
        <class 'int'>

        >>> type('textinho')
        <class 'str'>

Criando uma função simples::

        def NOME_DA_FUNÇÃO(LISTA DE PARÂMETROS):
            COMANDOS

.. warning::

        Coloque os dois pontos após definir a função!

.. note::
        Faça a identação nas linhas abaixo da definição da função!

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

Qual a diferença entre utilizar ``print`` e ``return`` aqui em cima?!?

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

----------------------
Funções com argumentos
----------------------

Queremos somar 3 com um número qualquer que insiro na função. Bora lá:

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
        ...             print("%d * %d = %d" % (i, j, i * j))
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

Exercícios
==========

1. Faça uma função que calcule a área de um círculo. Insira o raio como
   argumento.

   **Dica:** faça a importação de ``math`` e use PI de lá.

#. Crie uma função que receba um valor de temperatura em Fahrenheit e transforme
   em Celsius.

   Relembrar é viver:

        .. math::

                \frac{C}{5} = \frac{F - 32}{9}

#. Faça uma função que determina se um número é par ou ímpar. Use o ``%`` para
   determinar o resto de uma divisão. Por exemplo: ``3 % 2 = 1`` e ``4 % 2 = 0``

#. Crie uma função que receba 3 valores e calcula as raízes da fórmula de
   Bháskara.

   .. math::

        x = \frac{-b \pm \sqrt{b^2 - 4 \cdot a \cdot c}}{2 \cdot a}

   **Dica:** raiz quadrada é ``sqrt()``, importando ``math``: ``math.sqrt()``

   Faça um teste com ``bhaskara(1, -4, -5)`` e o programa deve obter as raízes:
   (5.0, -1.0)

#. Dada a função: :math:`y = 5x + 2`, determine os valores de :math:`y` para
   :math:`x` entre -10 a +10, onde :math:`x` é inteiro

#. Escreva uma função chamada ``has_duplicates`` que tome uma lista e retorne
   ``True`` se houver algum elemento que apareça mais de uma vez. Ela não deve
   modificar a lista original.

#. Duas palavras são um “par inverso” se uma for o contrário da outra. Escreva
   uma função que dado duas palavras, retorne ``True`` caso sejam.

#. Escreva uma função que imprime todos os números primos entre 1 e 50

   **Dica:** um número é primo se ele for divisível apenas por 1 e ele mesmo,
   use o operador ``%`` (resto da divisão) para isso.

#. Duas palavras são anagramas se você puder soletrar uma rearranjando as letras
   da outra. Escreva uma função chamada ``is_anagram`` que tome duas strings e
   retorne ``True`` se forem anagramas ou False caso contrário.

#. Escreva uma função que dado um número, calcule o fatorial desse número.
   Por exemplo, fatorial de 5: :math:`5! = 5*4*3*2*1 = 120`

#. Crie uma função que aproxima a função matemática seno, utilizando a seguinte
   equação:

   .. math::

        \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)!} \cdot x^{2n+1}
