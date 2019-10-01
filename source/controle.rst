Estruturas de controle
======================

As estruturas de controle servem para decidir quais blocos de código serão
executados.

Exemplo:
        | Se estiver nublado:
        |         Levarei guarda-chuva
        | Senão:
        |         Não levarei

.. note::

        Na linguagem Python, a indentação (espaço dado antes de uma linha) é
        utilizada para demarcar os blocos de código, e são obrigatórios quando
        se usa estruturas de controle.

.. doctest::

        >>> a = 7
        >>> if a > 3:
        ...     print("estou no if")
        ... else:
        ...     print("cai no else")
        ...
        estou no if

Também é possível checar mais de uma condição com o ``elif``. É a abreviatura
para ``else if``. Ou seja, se o ``if`` for falso, testa outra condição antes do
``else``:

.. doctest::

        >>> valor_entrada = 10
        >>> if valor_entrada == 1:
        ...     print("a entrada era 1")
        ... elif valor_entrada == 2:
        ...     print("a entrada era 2")
        ... elif valor_entrada == 3:
        ...     print("a entrada era 3")
        ... elif valor_entrada == 4:
        ...     print("a entrada era 4")
        ... else:
        ...     print("o valor de entrada não era esperado em nenhum if")
        ...
        o valor de entrada não era esperado em nenhum if

Note que quando uma condição for verdadeira, aquele bloco de código é executado
e as demais condições (``elif`` e ``else``) são puladas:

.. doctest::

      >>> a = 1
      >>> if a == 1:
      ...     print("é 1")
      ... elif a >= 1:
      ...     print("é maior ou igual a 1")
      ... else:
      ...     print("é qualquer outra coisa")
      ...
      é 1


Exercícios
----------

.. include:: exercicios_controle.rst
