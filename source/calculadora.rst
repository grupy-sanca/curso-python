Python como calculadora
=======================

Operadores matemáticos
----------------------

A linguagem Python possui operadores que utilizam símbolos especiais para representar
operações de cálculos, assim como na matemática:


- Soma (:math:`+`)

   .. doctest::

      >>> 2 + 3
      5

   Para utilizar números decimais, use o *ponto* no lugar de vírgula:

   .. doctest::

      >>> 3.2 + 2.7
      5.9

- Subtração (:math:`-`)

   .. doctest::

      >>> 6 - 4
      2

   .. doctest::

      >>> 7 - 8
      -1

- Multiplicação (:math:`*`)

   .. doctest::

      >>> 7 * 8
      56

   .. doctest::

      >>> 2 * 2 * 2
      8

- Divisão (:math:`/`)

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
   aconteceu, ou seja, `"ZeroDivisionError: divison by zero"`.


- Divisão inteira (:math:`//`)

   .. doctest::

      >>> 10 // 3
      3
      >>> 666 // 137
      4
      >>> 666 / 137
      4.861313868613139


- Resto da divisão (:math:`\%`)

   .. doctest::

      >>> 10 % 2
      0
      >>> 10 % 3
      1
      >>> 666 % 137
      118


Agora que aprendemos os operadores aritméticos básicos podemos seguir
adiante. Como podemos calcular :math:`2^{10}`? O jeito mais óbvio seria
multiplicar o número dois dez vezes:

.. doctest::

   >>> 2 * 2 * 2 * 2 * 2 * 2 * 2 * 2 * 2 * 2
   1024

Porém, isso não é muito prático, pois há um operador específico para isso, chamado de *potenciação/exponenciação*: :math:`**`

.. doctest::

   >>> 2 ** 10
   1024

.. doctest::

   >>> 10 ** 3
   1000

.. doctest::

   >>> (10 ** 800 + 9 ** 1000) * 233
   407254001651377825050774086265365912933271559572398924650169906751889900030955189004916347478470698880616885512201849445183728845558993514870858509087817789576388584560964682795896403435448681980001360244790530805842737419978616650940647045809688543958807077794866143976192872389017280782837244051514550016751431331392474612723898201318251801288569103581859710953756463227568553903785400053293756105145991925711692828410365978814157929143646138367222515290495329841814490874087309733954914817582614165290441834984054374534909954119315442169415884429645515258867781282214407424938115130906555866837546110340314133204645184212592152733050063403478054121909337278892530383627259086060904403894148963384111173869448637825223750221720739904084905206403076141255284819817001128530851921214720479861908207168928806625713775441834487646542035428141369478170696522098960677314242891140325390964310295889079588950798788612324634050495786532200848059999839607732520233

E a *raiz quadrada*?

Lembrando que :math:`\sqrt{x} = x^\frac{1}{2}`, então podemos calcular a raiz
quadrada do seguinte modo:

.. doctest::

   >>> 4 ** 0.5
   2.0

Mas a maneira recomendada para fazer isso é usar a função ``sqrt()`` da
biblioteca ``math``:

.. doctest::

   >>> import math
   >>> math.sqrt(16)
   4.0

Na primeira linha do exemplo importamos, da biblioteca padrão do Python, o
módulo ``math`` e então usamos a sua função ``sqrt`` para calcular
:math:`\sqrt{16}`

E se precisarmos utilizar o número :math:`\pi`?

.. doctest::

   >>> math.pi
   3.141592653589793

Não esqueça que é preciso ter executado ``import math`` antes de usar as funções
e constantes dessa biblioteca.

Exercícios
----------

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

O Python segue as mesmas regras de precedência da matemática.
O acrônimo **PEMDAS** ajuda a lembrar essa ordem:

.. spelling::

   arênteses
   xponenciação
   ultiplicação
   ivisão
   dição
   ubtração

#. **P**\ arênteses

#. **E**\ xponenciação

#. **M**\ ultiplicação e **D**\ ivisão (mesma precedência)

#. **A**\ dição e **S**\ ubtração (mesma precedência)

Notação Científica
------------------

Notação científica em Python usa a letra ``e`` como sendo a
potência de 10:

.. doctest::

   >>> 10e6
   10000000.0
   >>> 1e6
   1000000.0
   >>> 1e-5
   1e-05

Também pode ser usada a letra ``E`` maiúscula:

.. doctest::

   >>> 1E6
   1000000.0


Pontos Flutuantes
-----------------

Uma consideração importante sobre pontos flutuantes (números decimais). Por exemplo:

.. doctest::

    >>> 0.1
    0.1

É importante perceber que este valor, em um sentido real na máquina, não é exatamente 1/10. Está arredondando a exibição do valor real da máquina.

.. doctest::

    >>> format(0.1, '.50f')
    '0.10000000000000000555111512312578270211815834045410'

Veja que somente após a 18ª casa que há diferença. Isso é mais dígitos do que a maioria das pessoas acham úteis, então o Python mantém o número de dígitos gerenciáveis exibindo um valor arredondado

Este fato se torna aparente assim que você tenta fazer aritmética com esses valores

.. doctest::

    >>> 0.1 + 0.2
    0.30000000000000004

    >>> 0.7 - 0.2
    0.49999999999999994

Note que isso é da mesma natureza do ponto flutuante binário, não é um bug no Python e muito menos um bug no seu código. Você verá o mesmo tipo de coisa em todos os idiomas que suportam a aritmética de ponto flutuante de seu hardware (embora alguns idiomas possam não exibir a diferença por padrão ou em todos os modos de saída).

Os erros de representação referem-se ao fato de que a maioria das frações decimais não podem ser representadas exatamente como frações binárias (base 2). Essa é a principal razão pela qual o Python (ou Perl, C, C++, Java, Fortran e muitos outros) geralmente não exibe o número decimal exato que é esperado.

O valor de 1/10 não é exatamente representável como uma fração binária. Quase todas as máquinas atualmente (considerando após novembro de 2000) usam aritmética de ponto flutuante `IEEE-754`_, e quase todas as plataformas mapeiam pontos flutuantes do Python para a `"dupla precisão"` IEEE-754, que contêm 53 bits de precisão. Portanto, na entrada, o computador se esforça para converter 0.1 na fração mais próxima possível da forma ``J/2 ** N``, onde ``J`` é um inteiro contendo exatamente 53 bits.

.. _IEEE-754: https://pt.wikipedia.org/wiki/IEEE_754

Exercícios
----------

.. include:: exercicios_calculadora_expressoes.rst


Sobre Comentários
-----------------

Caso precise explicar alguma coisa feita no código, é possível escrever um texto
(que não será executado), que ajuda a entender ou lembrar o que foi feito.
Esse texto é chamado de comentário, e para escrever um basta utilizar o
caractere ``#``. Exemplo:

.. doctest::

   >>> 3 + 4  # será lido apenas o cálculo, do # para frente o interpretador do Python irá ignorar!
   7

.. doctest::

   >>> # Aqui vai um código só com comentários! Posso falar o que quiser que não será interpretado, lalala, la-le-li-lo-lu. A job we hate to buy things we don't need.


Comparações
-----------

Os operadores de comparação em Python são:

========  ===============
Operação  Significado
========  ===============
<         menor que
<=        menor igual que
>         maior que
>=        maior igual que
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
