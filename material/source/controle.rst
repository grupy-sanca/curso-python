======================
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

----------
Exercícios
----------

1. Escreva um programa que, dados 2 números diferentes (a e b), encontre o menor
   deles.

#. Para doar sangue é necessário ter entre 18 e 67 anos. Faça um programa que
   pergunte a idade de uma pessoa e diga se ela pode doar sangue ou não.

#. Considere uma equação do segundo grau :math:`f(x) = a * x^2 + b * x + c`. A
   partir dos coeficientes, determine se a equação possui duas raízes reais,
   uma, ou se não possui.

   **Dica:** :math:`delta = b^2 - 4 * a * c`, se delta é maior que 0, possui
   duas raízes reais, se delta é 0, possui uma raiz, e caso delta seja menor que
   0 não possui raiz real

#. Leia dois números e efetue a adição. Caso o valor somado seja maior que 20,
   este deverá ser apresentado somando-se a ele mais 8; caso o valor somado seja
   menor ou igual a 20, este deverá ser apresentado subtraindo-se 5.

#. Leia um número e imprima a raiz quadrada do número caso ele seja positivo ou
   igual a zero e o quadrado do número caso ele seja negativo.

#. Leia um número inteiro entre 1 e 12 e escrever o mês correspondente. Caso o
   usuário digite um número fora desse intervalo, deverá aparecer uma mensagem
   informando que não existe mês com este número.

Desafios
========

1. Escreva um programa que, dados 3 números diferentes (a, b e c), encontre o
   menor deles.

#. Dado 3 valores inteiros lidos do teclado: A, B e C, retorne a soma deles.
   Porém, caso algum desses valores seja 13, então ele não conta para a soma, e
   os valores a sua direita também não.

   Por exemplo:
           | 1, 2, 3 -> 6
           | 1, 2, 13 -> 3
           | 1, 13, 3 -> 1
           | 13, 2, 3 -> 0
