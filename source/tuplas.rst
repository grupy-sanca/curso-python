.. _section_tuplas:

Tuplas
======

As tuplas são listas que não podem ser modificadas. Elas são definidas usando parênteses ``()``.

.. doctest::

        >>> nomes_frutas = ("maçã", "banana", "abacaxi")
        >>> nomes_frutas[0] = "melancia"
        Traceback (most recent call last):
          File "<python-input-3>", line 1, in <module>
            nomes_frutas[0] = "melancia"
            ~~~~~~~~~~~~^^^
        TypeError: 'tuple' object does not support item assignment

Também não é possível adicionar elementos como nas listas usando ``append``.

.. doctest::

        >>> nomes_frutas = ("maçã", "banana", "abacaxi")
        >>> nomes_frutas.append("melancia")
        Traceback (most recent call last):
          File "<python-input-5>", line 1, in <module>
            nomes_frutas.append("melancia")
            ^^^^^^^^^^^^^^^^^^^
        AttributeError: 'tuple' object has no attribute 'append'

Mas por que alguém utilizaria tuplas em lugar de listas? A resposta está na velocidade de execução que as tuplas oferecem.
