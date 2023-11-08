#. Por que o seguinte código retorna uma *string* vazia?

   .. doctest::

      >>> texto = "No alto da montanha havia uma rosa"
      >>> texto[0:-1:-1]
      ''

   .. note::

      .. doctest::

         >>> texto = "No alto da montanha havia uma rosa"
         >>> texto[0:-1]
         'No alto da montanha havia uma ros


#. Palindromo é uma palavra, frase ou número que pemanece igual quando lida de trás para frente:

   Faça um programa que retorna se uma palavra é um palindromo.

   **Exemplo:** A palavra ``Radar`` deve retornar ``É um palindromo``, enquanto a palavra ``Python`` deve retornar ``Não é um palindromo``

      .. only:: instructors

         Exemplo de solução:

         .. code-block:: python3

            >>> palavra = "Radar"
            >>> if palavra.upper() == palavra[::-1].upper():
                  print('É um palindromo')
                else:
                  print('Não é um palindromo')

#. Usar strings é algo poderoso. Para experimentar um pouco desse poder, resolva o desafio abaixo utilizando string:

   **Desafio:** Seja um N não negativo, retorne True se o número está a distância de até dois de um múltiplo de dez.

   **Exemplo:** O numero 17 deve retornar ``False``, enquanto o numerto 12 deve retornar ``True``

   **Resolução inspirada por um dos alunos do professor Fernando Masanori.**

      .. only:: instructors
         
         Exemplo de solução:

         .. code-block:: python3

            >>> numero = 17
            >>> str(numero)[-1] in '01289'

#. Crie uma função que receba do usuário uma string. Essa função deve retornar uma string sem suas vogais.

      .. doctest::

         >>> palavra = "Python":
         'Pythn'
         >>> palavra = "Amendoin":
         'mndn'
