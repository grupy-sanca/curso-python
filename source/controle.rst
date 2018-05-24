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

        Na linguagem **python** a identação (espaço dado antes de uma linha) é
        utilizada para demarcar os blocos de código, e são obrigatórios quando
        se usa estruturas de controle

.. doctest::

        >>> a = 7
        >>> if a > 3:
        ...     print("estou no if")
        ... else:
        ...     print("cai no else")
        ...
        estou no if

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


Exercícios
----------

.. include:: exercicios_controle.rst
