Função ``range()``
------------------

Aprendemos a adicionar itens a uma lista mas, e se fosse necessário produzir
uma lista com os números de 1 até 200?

.. doctest::

        >>> lista_grande = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13] # ???
        >>> lista_grande
        [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13]

Em Python existe a função embutida ``range()``, com ela é possível produzir uma lista extensa de uma maneira bem simples:

.. doctest::

        >>> print(list(range(1, 200)))
        [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 171, 172, 173, 174, 175, 176, 177, 178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190, 191, 192, 193, 194, 195, 196, 197, 198, 199]

Além disso, o ``range()`` também oferece algumas coisas interessantes. Por
exemplo, imprimir os números espaçados de 5 em 5, entre 0 e 30:

.. doctest::

        >>> print(list(range(0, 30, 5)))
        [0, 5, 10, 15, 20, 25]

Mas, como na maior parte das vezes apenas queremos uma lista começando em 0 e
indo até o número desejado, a função ``range()`` também funciona da seguinte
maneira:

.. doctest::

        >>> print(list(range(10)))
        [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

.. note:: O intervalo do ``range()`` é aberto, ou seja, quando passamos o valor 10, ele vai até o 9 (n - 1). Caso deseje criar a lista até o 10 de fato, deve-se passar o valor 11.

Mas por que precisamos transformar o ``range()`` em ``list``? O que acontece se não fizermos isso?

.. doctest::

      >>> print(range(200))
      range(0, 200)

Mas o que é que essa função retorna?

.. doctest::

      >>> type(range(200))
      <class 'range'>"

AHA! A função ``range()`` retorna algo do tipo ``range``, por isso precisamos transformar em uma lista para vermos todos os números no ``print()``!