#. Faça uma função que calcule a área de um círculo. Insira o raio como
   argumento.

   **Dica:** faça a importação de ``math`` e use PI de lá.

#. Crie uma função que receba um valor de temperatura em Fahrenheit e transforme
   em Celsius.

   Relembrar é viver:

        .. math::

                \frac{C}{5} = \frac{F - 32}{9}

#. Faça uma função que determina se um número é par ou ímpar. Use o ``%`` para
   determinar o resto de uma divisão. Por exemplo: ``3 % 2 = 1`` e ``4 % 2 = 0``

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
   Por exemplo, fatorial de 5: :math:`5! = 5*4*3*2*1 = 120`

#. Crie uma função que aproxima a função matemática seno, utilizando a seguinte
   equação:

   .. math::

        \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)!} \cdot x^{2n+1}