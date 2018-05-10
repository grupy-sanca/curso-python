#. Faça uma função que determina se um número é par ou ímpar. Use o ``%`` para
   determinar o resto de uma divisão. Por exemplo: ``3 % 2 = 1`` e ``4 % 2 = 0``

#. Faça uma função que calcule a área de um círculo. Insira o raio como
   argumento.

   **Dica:** faça a importação de ``math`` e use :math:`\pi` de lá.

   .. math::

            A = \pi R^2

#. Crie uma função que receba um valor de temperatura em Fahrenheit e transforme
   em Celsius.

   Relembrar é viver:

        .. math::

                \frac{C}{5} = \frac{F - 32}{9}

#. Crie uma função que receba 3 valores e calcula as raízes da fórmula de
   Bháskara.

   .. math::

        x = \frac{-b \pm \sqrt{b^2 - 4 \cdot a \cdot c}}{2 \cdot a}

   **Dica:** raiz quadrada é ``sqrt()``, importando ``math``: ``math.sqrt()``

   Faça um teste com ``bhaskara(1, -4, -5)`` e o programa deve obter as raízes:
   (5.0, -1.0)

#. Dada a função: :math:`y = 5x + 2`, determine os valores de :math:`y` para
   :math:`x` entre -10 a +10, onde :math:`x` é inteiro

#. Escreva uma função chamada ``has_duplicates`` que tome uma lista e retorne
   ``True`` se houver algum elemento que apareça mais de uma vez. Ela não deve
   modificar a lista original.

#. Duas palavras são um “par inverso” se uma for o contrário da outra. Escreva
   uma função que dado duas palavras, retorne ``True`` caso sejam.

#. Escreva uma função que imprime todos os números primos entre 1 e 50

   **Dica:** um número é primo se ele for divisível apenas por 1 e ele mesmo,
   use o operador ``%`` (resto da divisão) para isso.

#. Duas palavras são anagramas se você puder soletrar uma rearranjando as letras
   da outra. Escreva uma função chamada ``is_anagram`` que tome duas strings e
   retorne ``True`` se forem anagramas ou False caso contrário.

#. Escreva uma função que dado um número, calcule o fatorial desse número.
   Por exemplo, fatorial de 5:

    .. math::

        5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120

#. Crie uma função que aproxima a função matemática seno, utilizando a seguinte
   equação:

   .. math::

        \sin(x) = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)!} \cdot x^{2n+1}

#. Calcule :math:`\pi` usando um método de Monte Carlo.

   Monte Carlo é uma classe de métodos para resolver problemas usando
   estatística. Aqui você vai implementar uma função usando um desses algoritmos
   para calcular o número :math:`\pi`.

   Dado um círculo de raio :math:`R` dentro de um quadrado de lados :math:`2R`,
   a razão entre a área do círculo para a área do quadrado é:

   .. math::

      \frac{A_\bigcirc}{A_\square} = \frac{\pi R^2}{4 R^2} = \frac{\pi}{4}

   Ou seja, se você escolher aleatoriamente um ponto dentro do quadrado, a
   probabilidade dele cair dentro do círculo é de :math:`\pi / 4`. Se você
   escolher :math:`N` pontos aleatórios dentro do quadrado, cerca de
   :math:`N \pi / 4` estarão dentro do círculo.

   Então, basta escolher pontos aleatórios dentro do quadrado e ver se estão
   dentro do círculo 🙃.

   Um ponto :math:`(x, y)` está dentro do círculo se
   :math:`x^2 + y^2 \leq R^2`.

   Faça uma função que receba como argumento um número :math:`N` de pontos
   :math:`(x, y)` (aleatórios) a serem sorteados. Dentro dessa função, você
   deve fazer um laço que sorteie esses :math:`N` pontos e veja quantos estão
   dentro do círculo. Se :math:`M` pontos caírem dentro do círculo, então a
   probabilidade de um ponto aleatório estar dentro do círculo é
   aproximadamente :math:`M / N`. Então, podemos estimar :math:`\pi` como:

   .. math::

      \pi \approx \frac{4 M}{N}

   Para sortear um número aleatório entre :math:`a` e :math:`b` utilize a
   função `uniform(a, b)` do módulo `random`. Exemplo:

   .. doctest::

      >>> import random
      >>> random.uniform(1, 2) # número aleatório entre 1 e 2
      1.8740445361226983

   .. only:: instructors-guide

      .. code:: python

         import random

         def pi(N):
             M = 0
             for i in range(N):
                 x, y = random.uniform(0, 1), random.uniform(0, 1) # cosideramos R = 1

                 if (x**2 + y**2 < 1):
                     M += 1

             return 4 * M / N

         print(pi(100))
         print(pi(1000))
         print(pi(10000))
         print(pi(100000))
         print(pi(1000000))
         print(pi(10000000)) # demora um pouquinho :P
