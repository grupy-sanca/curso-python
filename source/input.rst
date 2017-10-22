========================
Lendo valores do teclado
========================

Em **python** também é possível ler do teclado as informações digitadas pelo
usuário, e isso é feito por meio da função embutida ``input`` da seguinte forma:

.. testsetup:: input_single

        def input(text):
            print(text + '10')
            return '10'

.. doctest:: input_single

        >>> valor_lido = input("digite um valor: ")
        digite um valor: 10

        >>> type(valor_lido)  # deve-se notar que o valor lido é SEMPRE do tipo string
        <class 'str'>

        >>> valor_lido + 10  # ou seja, antes de trabalhar com esse valor, é preciso converter para o tipo correto
        Traceback (most recent call last):
            ...
        TypeError: must be str, not int

Isso pode ser feito usando os operadores ``int()`` e ``float(),`` dependendo do
valor esperado:

.. testsetup:: input_convert

        def gen():
            yield '10'
            yield '1.5'

        values = gen()

        def input(text):
            value = next(values)
            print(text + value)
            return value

.. doctest:: input_convert

        >>> valor_lido = int(input("digite um valor inteiro: "))
        digite um valor inteiro: 10

        >>> type(valor_lido)
        <class 'int'>

        >>> valor_lido + 10
        20

        >>> valor_lido = float(input("digite um valor decimal: "))
        digite um valor decimal: 1.5

        >>> valor_lido - 1
        0.5

----------
Exercícios
----------

.. include:: exercicios_input.rst
