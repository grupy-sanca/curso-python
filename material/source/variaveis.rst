Variáveis
=========

Variável é um **nome** que se refere a um valor.


Atribuição
----------

Atribuição é o processo de criar uma nova variável e dar um novo valor a
ela. A seguir damos exemplos de como fazer atribuições:

.. code:: python

   >>> numero = 11
   >>> numero
   11

.. code:: python

   >>> frase = "Me dá um copo d'água"
   >>> frase
   "Me dá um copo d'água"

.. code:: python

   >>> pi = 3.141592
   >>> pi
   3.141592

No exemplo anterior realizamos três atribuições. No primeiro atribuimos um
número inteiro à variável de nome ``numero``; no segundo uma frase à
variável ``frase``; no último um número de ponto flutuante à ``pi``.

Nomes de Variáveis
------------------

Bons programadores escolhem nomes significativos para as suas variáveis
- eles documentam o propósito da variável.

Nomes de variáveis podem ter o tamanho que você achar necessário e podem
conter tanto letras como números, porém não podem começar com números. É
possível usar letras maiúsculas, porém a convenção é utilizar somente
letras minúsculas para nomes de variáveis.

Tentar dar um nome ilegal a uma variável ocasionará em um erro de sintaxe:

.. code:: python

    >>> 123voa = 10
      File "<stdin>", line 1
        123voa = 10
             ^
    SyntaxError: invalid syntax

.. code:: python

   >>> ol@ = "oi"
     File "<stdin>", line 1
       ol@ = "oi"
           ^
   SyntaxError: invalid syntax

.. code:: python

   >>> def = 2.7
     File "<stdin>", line 1
       def = 2.7
           ^
   SyntaxError: invalid syntax


``123voa`` é ilegal pois começa com um número. ``ol@`` é ilegal, pois
contém um caracter inválido (@), mas o que há de errado com ``def``?

A questão é que ``def`` é uma palavra-chave do Python e o interpretador
usa essas palavras para reconhecer a estrutura do programa e não podem ser
utilizadas como nomes de variável.

Outro ponto importante de notar é que não é possível acessar variáveis que
ainda não foram definidas:

.. code:: python

   >>> nao_definida
   Traceback (most recent call last):
     File "<stdin>", line 1, in <module>
   NameError: name 'nao_definida' is not defined

Tentar acessar uma variável sem definí-la anteriormente ocasiona em um "erro
de nome".

Também podemos atribuir expressões a uma variável:

.. code:: python

   >>> x = 3 * 5 - 2
   >>> x
   13
   >>> y = 3 * x + 10
   >>> y
   49
   >>> z = x + y
   >>> z
   62

.. code:: python

   >>> n = 10
   >>> n + 2 # 10 + 2
   12
   >>> 9 - n # 9 - 10
   -1


É importante lembrar que para mudar o valor de uma variável é preciso
utilizar a atribuição. Nos dois exemplos anteriores não atribuimos as
expressões à n, portanto seu valor continuou o mesmo.

Vamos alterar o valor de ``n``:

.. code:: python

   >>> n
   10
   >>> n = n + 2
   >>> n
   12
   >>> 9 - n
   -3

Outra forma de somar na variável:

.. code:: python

   >>> num = 4
   >>> num += 3
   >>> num
   7

Também funciona com multiplicação:

.. code:: python

   >>> x = 2
   >>> x *= 3
   >>> x
   6

Faça agora o :ref:`exercício 5 <ex_variaveis-basico>`
