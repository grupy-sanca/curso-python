=======================
Estruturas de repetição
=======================

As estruturas de repetição são utilizadas quando queremos que um bloco de código
seja executado várias vezes.

Em **python** existem duas formas de criar uma estrutura de repetição:

        O ``for`` é usado quando se quer iterar sobre um bloco de código um
        número determinado de vezes.

        O ``while`` é usando quado queremos que o bloco de código seja repetido
        até que uma condição seja satisfeita, ou seja, é necessário que uma
        expressão booleana dada seja verdadeira e assim que ela se tornar falsa,
        o ``while`` para.

.. note::

        Na linguagem **python** a identação é obrigatória, assim como estruturs
        de controle, para as estruturas de repetição.

        .. doctest::

                >>> # Aqui repetimos o print 3 vezes
                >>> for n in range(0, 3):
                ...     print(n)
                ...
                0
                1
                2

                >>> # Aqui iniciamos o n em 0, e repetimos o print até que seu valor seja maior ou igual a 3
                >>> n = 0
                >>> while n < 3:
                ...     print(n)
                ...     n += 1
                ...
                0
                1
                2

O *loop* for em **python** itera sobre os itens de um conjunto, sendo assim, o
``range(0, 3)`` precisa ser um conjunto de elementos, e na verdade ele é:

.. doctest::

        >>> list(range(0, 3))
        [0, 1, 2]

Isso se aplica para *strings* também:

.. doctest::

        >>> # Para cada letra na palavra, imprimir a letra
        >>> palavra = "casa"
        >>> for letra in palavra:
        ...     print(letra)
        ...
        c
        a
        s
        a

        >>> lista = [1, 2, 3, 4, 10]
        >>> for numero in lista:
        ...     print(numero**2)
        ...
        1
        4
        9
        16
        100

Para auxiliar as estruturas de repetição, existem dois comandos:

        * ``break``: É usado para sair de um *loop*, não importando o estado em
          que se encontra.

        * ``continue``: Funciona de maneira parecida com a do ``break``, porém
          no lugar de encerrar o *loop*, ele faz com que todo o código que
          esteja abaixo (porém ainda dentro do *loop*) seja ignorado e avança
          para a próxima iteração.

.. testsetup:: input_loop

        def gen():
            yield 'oi'
            yield '?'
            yield 'sair'

        values = gen()

        def input(text):
            value = next(values)
            print(text + value)
            return value

.. testcode::

        """
        Esse código deve rodar até que a palavra "sair" seja digitada.
        * Caso uma palavra com 2 ou menos caracteres seja digitada, um aviso
          deve ser exibido e o loop será executado do início (devido ao
          continue), pedindo uma nova palavra ao usuário.
        * Caso qualquer outra palavra diferente de "sair" seja digitada, um
          aviso deve ser exibido.
        * Por fim, caso a palavra seja "sair", uma mensagem deve ser exibida e o
          loop deve ser encerrado (break).
        """

.. doctest:: input_loop

        >>> while True:
        ...     string_digitada = input("Digite uma palavra: ")
        ...     if string_digitada.lower() == "sair":
        ...         print("Fim!")
        ...         break
        ...     if len(string_digitada) < 2:
        ...         print("String muito pequena")
        ...         continue
        ...     print("Tente digitar \"sair\"")
        ...
        Digite uma palavra: oi
        Tente digitar "sair"
        Digite uma palavra: ?
        String muito pequena
        Digite uma palavra: sair
        Fim!


----------
Exercícios
----------

.. include:: exercicios_repeticao.rst
