#. Escreva um programa que, dados 2 números diferentes (a e b), encontre o menor
   deles.

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> a = 10
         >>> b = 8
         >>> if a < b:
         ...   print("a é o menor")
         ... else:
         ...   print("b é o menor")
         ...
         b é o menor

#. Para doar sangue é necessário [1]_:

   - Ter entre 16 e 69 anos.
   - Pesar mais de 50 kg.
   - Estar descansado (ter dormido pelo menos 6 horas nas últimas 24 horas).

   Faça um programa que pergunte a idade, o peso e quanto dormiu nas últimas
   24 h para uma pessoa e diga se ela pode doar sangue ou não.

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> idade = int(input("Qual a sua idade? "))
         >>> peso = int(input("Qual o seu peso? "))
         >>> horas_de_sono = int(input("Quantas horas dormiu nas ultimas 24h? "))
         >>> if idade > 16 and idade < 69 and peso > 50 and horas_de_sono > 6:
         ...   print("você pode doar sangue")
         ... else:
         ...   print("você não pode doar sangue")
         ...

#. Considere uma equação do segundo grau
   :math:`f(x) = a \cdot x^2 + b \cdot x + c`.
   A partir dos coeficientes, determine se a equação possui duas raízes reais,
   uma, ou se não possui.

   **Dica:** :math:`\Delta = b^2 - 4 \cdot a \cdot c` : se delta é maior que 0,
   possui duas raízes reais; se delta é 0, possui uma raiz; caso delta seja
   menor que 0, não possui raiz real

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> a = int(input("Qual o valor de a? "))
         >>> b = int(input("Qual o valor de b? "))
         >>> c = int(input("Qual o valor de c? "))
         >>> delta = b**2 - 4*a*c
         >>> if delta > 0:
         ...   print("A equação possui duas raizes")
         ... elif delta == 0:
         ...   print("A equação possui uma raiz")
         ... else:
         ...   print("A equação não possui raiz real")
         ...

#. Leia dois números e efetue a adição. Caso o valor somado seja maior que 20,
   este deverá ser apresentado somando-se a ele mais 8; caso o valor somado seja
   menor ou igual a 20, este deverá ser apresentado subtraindo-se 5.

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> a = int(input("Qual o primeiro valor? "))
         >>> b = int(input("Qual o segundo valor? "))
         >>> if a+b > 20:
         ...   print(a+b+8)
         ... else:
         ...   print(a+b-5)
         ...

#. Leia um número e imprima a raiz quadrada do número caso ele seja positivo ou
   igual a zero e o quadrado do número caso ele seja negativo.

#. Leia um número inteiro entre 1 e 12 e escreva o mês correspondente. Caso o
   usuário digite um número fora desse intervalo, deverá aparecer uma mensagem
   informando que não existe mês com este número.

#. Um supermercado está tendo muitos problemas com a validade de seus produtos
   e pediu sua ajuda com esse problema. Faça um programa que leia o dia, o mês e o
   ano da data atual e de validade de um produto, e imprima se o produto já está vencido
   ou não.  


.. [1] Para mais informações sobre doação de sangue, acesse
       http://www.prosangue.sp.gov.br/artigos/requisitos_basicos_para_doacao.html