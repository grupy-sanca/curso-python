Python como calculadora
=======================

Operadores matemáticos
----------------------

Python possui operadores que utilizam símbolos especiais que representam
operações de cálculos, assim como na matemática:


Soma (:math:`+`)
~~~~~~~~~~~~~~~~

.. doctest::

   >>> 2 + 3
   5

Para utilizar números decimais, use o **ponto** no lugar de vírgula:

.. doctest::

   >>> 3.2 + 2.7
   5.9


Subtração (:math:`-`)
~~~~~~~~~~~~~~~~~~~~~

.. doctest::

   >>> 6 - 4
   2

.. doctest::

   >>> 7 - 8
   -1


Multiplicação (:math:`*`)
~~~~~~~~~~~~~~~~~~~~~~~~~

.. doctest::

   >>> 7 * 8
   56

.. doctest::

   >>> 2 * 2 * 2
   8


Divisão (:math:`/`)
~~~~~~~~~~~~~~~~~~~

.. doctest::

   >>> 100 / 20
   5.0

.. doctest::

   >>> 10 / 3
   3.3333333333333335

E se fizermos uma divisão por zero?

.. doctest::

   >>> 2 / 0
   Traceback (most recent call last):
     File "<stdin>", line 1, in <module>
   ZeroDivisionError: division by zero

Como não existe um resultado para a divisão pelo número zero, o Python
interrompe a execução do programa (no caso a divisão) e mostra o erro que
aconteceu, no caso o "ZeroDivisionError: divison by zero".


Divisão inteira (:math:`//`)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. doctest::

   >>> 10 // 3
   3
   >>> 666 // 137
   4
   >>> 666 / 137
   4.861313868613139


Resto da divisão (:math:`\%`)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. doctest::

   >>> 10 % 2
   0
   >>> 10 % 3
   1
   >>> 666 % 137
   118


Agora que aprendemos os operadores aritméticos básicos podemos seguir
adiante. Como podemos calcular :math:`2^{10}`? O jeito mais óbvio é
multiplicar o número dois dez vezes:

.. doctest::

   >>> 2 * 2 * 2 * 2 * 2 * 2 * 2 * 2 * 2 * 2
   1024

Porém não é muito prático, para fazer isso podemos usar o operador de
**potenciação/exponenciação**: :math:`**`

.. doctest::

   >>> 2 ** 10
   1024

.. doctest::

   >>> 10 ** 3
   1000

.. doctest::

   >>> (10 ** 800 + 9 ** 1000) * 233
   407254001651377825050774086265365912933271559572398924650169906751889900030955189004916347478470698880616885512201849445183728845558993514870858509087817789576388584560964682795896403435448681980001360244790530805842737419978616650940647045809688543958807077794866143976192872389017280782837244051514550016751431331392474612723898201318251801288569103581859710953756463227568553903785400053293756105145991925711692828410365978814157929143646138367222515290495329841814490874087309733954914817582614165290441834984054374534909954119315442169415884429645515258867781282214407424938115130906555866837546110340314133204645184212592152733050063403478054121909337278892530383627259086060904403894148963384111173869448637825223750221720739904084905206403076141255284819817001128530851921214720479861908207168928806625713775441834487646542035428141369478170696522098960677314242891140325390964310295889079588950798788612324634050495786532200848059999839607732520233


Raíz quadrada
~~~~~~~~~~~~~

Lembrando que :math:`\sqrt{x} = x^\frac{1}{2}`, então podemos calcular a raiz
quadrada do seguinte modo:

.. doctest::

   >>> 4 ** 0.5
   2.0

Mas, a maneira recomendada para fazer isso é usar a função ``sqrt`` da
biblioteca ``math``:

.. doctest::

   >>> import math
   >>> math.sqrt(16)
   4.0

Na primeira linha do exemplo importamos, da biblioteca padrão do python, o
módulo ``math`` e então usamos a sua função ``sqrt`` para calcular
:math:`\sqrt{16}`

E se precisarmos utilizar o número :math:`\pi`?

.. doctest::

   >>> math.pi
   3.141592653589793

Não esqueça que é preciso ter rodado ``import math`` antes de usar as funções
e constantes dessa biblioteca.

Exercícios
~~~~~~~~~~

.. include:: exercicios_calculadora_operadores.rst


Expressões Numéricas
--------------------

Agora que já aprendemos diversos operadores, podemos combiná-los e resolver
problemas mais complexos:

.. doctest::

   >>> 3 + 4 * 2
   11

.. doctest::

   >>> 7 + 3 * 6 - 4 ** 2
   9

.. doctest::

   >>> (3 + 4) * 2
   14

.. doctest::

   >>> (8 / 4) ** (5 - 2)
   8.0

Quando mais de um operador aparece em uma expressão, a ordem de avaliação
depende das regras de precedência.

Python segue as mesmas regras de precedência para seus operadores matemáticos
que a matemática. O acrônimo **PEMDAS** ajuda a lembrar essa ordem:

#. **P** arênteses

#. **E** xponenciação

#. **M** ultiplicação e **D** ivisão (mesma precedência)

#. **A** dição e **S** subtração (mesma precedência)

Exercícios
~~~~~~~~~~

.. include:: exercicios_calculadora_expressoes.rst


Comentários
-----------

Para fazer comentários no código, ou seja, caso queira escrever um texto para
explicar algum código que não sejam executado pelo interpretador do python,
utilize o ``#``. Exemplo:

.. doctest::

   >>> 3 + 4  # será lido apenas o cálculo, do # para frente o interpretador do Python irá ignorar!
   7

.. doctest::

   >>> # Aqui vai um código só com comentários! Posso falar o que quiser que não será interpretado, lalala, la-le-li-lo-lu. A job we hate to buy things we don't need.


Comparacões
-----------

Os operadores de comparação em Python são:

========  ===============
Operação  Significado
========  ===============
<         menor que
<=        menor igual que
>         maior que
<=        maior igual que
==        igual
!=        diferente
========  ===============

.. doctest::

   >>> 2 < 10
   True
   >>> 2 > 11
   False
   >>> 10 > 10
   False
   >>> 10 >= 10
   True
   >>> 42 == 24
   False
   >>> 666 != 137
   True
   >>> 8**2 == 60 + 4
   True
   >>> 100 != 99 + 3
   True
