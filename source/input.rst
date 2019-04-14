Lendo valores do teclado
========================

Em Python também é possível ler do teclado as informações digitadas pelo
usuário. E isso é feito por meio da função embutida ``input()`` da seguinte
forma:

.. testsetup:: input_single

        def input(text):
            print(text + '10')
            return '10'

.. doctest:: input_single

        >>> valor_lido = input("digite um valor: ")
        digite um valor: 10

        >>> type(valor_lido)  # deve-se notar que o valor lido é SEMPRE do tipo string
        <class 'str'>

A função ``input()`` "termina" de ser executada quando pressionamos *enter*.

.. note:: O valor lido é sempre do tipo string.

Mas, como realizar operações com os valores lidos?

.. doctest:: input_single

        >>> valor_lido + 10  # para trabalhar com esse valor, é preciso converter para o tipo correto
        Traceback (most recent call last):
            ...
        TypeError: must be str, not int

Para poder fazer isso pode-se usar os operadores ``int()`` e ``float(),`` que
converte o valor lido para o tipo de dado esperado:

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

Tudo o que for digitado no teclado, até pressionar a tecla *enter*, será
capturado pela função ``input()``. Isso significa que podemos ler palavras
separadas por um espaço, ou seja, uma frase inteira:

.. testsetup:: input_frase

   def input():
      frase = 'Rosas são vermelhas, violetas são azuis, girassóis são legais.'
      print(frase)
      return frase

.. doctest:: input_frase

   >>> frase = input()
   Rosas são vermelhas, violetas são azuis, girassóis são legais.
   >>> frase
   'Rosas são vermelhas, violetas são azuis, girassóis são legais.'


Exercícios
----------

.. include:: exercicios_input.rst
