============
Condicionais
============

O tipo de dado boleano (``bool``) refere-se a uma unidade lógica sobre a qual
podemos realizar operações, particularmente úteis para o controle de fluxo de um
programa.

A unidade boleana assume apenas 2 valores: Verdadeiro (``True``) e Falso (``False``).

.. note::

        Essa estrutura binária é a forma com a qual o computador opera (0 e 1).

.. doctest::

        >>> True
        True
        >>> type(False)
        <class 'bool'>

Qualquer expressão lógica retornará um valor boleano:

.. doctest::

        >>> 2 < 3
        True
        >>> 2 == 5
        False

Os operadores lógicos utilizados em programação são:

        * ``>``: maior a, por exemplo 5 > 3
        * ``<``: menor a
        * ``>=``: maior ou igual a
        * ``<=``: menor ou igual a
        * ``==``: igual a
        * ``!=``: diferente de

Para realizar operações com expressões lógicas, existem:

        * ``and`` (e): opera segundo a seguinte tabela:
                ========== ========== ==========
                Valor 1    Valor 2    Resultado
                ========== ========== ==========
                Verdadeiro Verdadeiro Verdadeiro
                Verdadeiro Falso      Falso
                Falso      Verdadeiro Falso
                Falso      Falso      Falso
                ========== ========== ==========
        * ``or`` (ou):
                ========== ========== ==========
                Valor 1    Valor 2    Resultado
                ========== ========== ==========
                Verdadeiro Verdadeiro Verdadeiro
                Verdadeiro Falso      Verdadeiro
                Falso      Verdadeiro Verdadeiro
                Falso      Falso      Falso
                ========== ========== ==========
        * ``not`` (não):
                ========== ==========
                Valor      Resultado
                ========== ==========
                Verdadeiro Falso
                Falso      Verdadeiro
                ========== ==========

.. doctest::

        >>> 10 > 3 and 2 == 4
        False

        >>> 10 > 3 or 2 == 4
        True

        >>> not not not 1 == 1
        False

Assim como os operadores aritméticos, os operadores boleanos também
possuem uma ordem de prioridade:

        * ``not`` tem maior prioridade que ``and`` que tem maior prioridade
          que ``or``:

.. doctest::

        >>> not False and True or False
        True
