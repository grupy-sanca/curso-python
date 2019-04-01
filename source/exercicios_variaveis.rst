#. Supondo que a cotação do dólar esteja em :math:`\mathrm{R}\$\, 3{,}25`,
   salve esse valor em uma variável e utilize-o para calcular quanto você
   teria ao cambiar :math:`\mathrm{R}\$\, 65{,}00` para dólares.

#. Abelindo é um professor muito malvado. Ele quer decidir como reprovar
   Rondinelly, que tirou 8.66, 5.35, 5 e 1, respectivamente, nas provas
   P1, P2, P3 e P4. Para isso, ele pode calcular a nota final usando média
   aritmética (M.A.), média geométrica (M.G.) ou média harmônica (M.H.).

   .. math::

      M.A. = \frac{P_1 + P_2 + P_3 + P_4}{4}

   .. math::

      M.G. = \sqrt[4]{|P_1 P_2 P_3 P_4|}

   .. math::

      M.H. = \frac{4}{\frac{1}{P_1} + \frac{1}{P_2} + \frac{1}{P_3} + \frac{1}{P_4}}

   Qual dessas médias dá a maior nota pra Rondinelly? E qual das médias dá
   a pior nota?

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> p1 = 8.66
         >>> p2 = 5.35
         >>> p3 = 5
         >>> p4 = 1
         >>> MA = (p1 + p2 + p3 + p4) / 4
         >>> MG = (p1 * p2 * p3 * p4)**(1/4)
         >>> MH = 4 / (1/p1 + 1/p2 + 1/p3 + 1/p4)
         >>> print(MA, MG, MH)
         5.0024999999999995 3.901309628628489 2.662425726074314

#. Josefson deseja fazer compras na China. Ela quer comprar
   um celular de :math:`\mathrm{USD}\, 299{,}99`,
   uma chaleira de :math:`\mathrm{USD}\, 23{,}87`,
   um gnomo de jardim de :math:`\mathrm{USD}\, 66{,}66` e
   6 adesivos de unicórnio de :math:`\mathrm{USD}\, 1{,}42` cada um. O frete
   de tudo isso para a cidade de Rolândia, no Paraná, ficou em
   :math:`\mathrm{USD}\, 12{,}34`.

   a. Calcule o valor total da compra em dólares.

   b. Usando o mesmo valor do dólar do exercício anterior, calcule o preço
      final em Reais. Lembre-se que o valor do *IOF* é de :math:`6{,}38 \, \%`.

   c. Quanto ela pagou apenas de *IOF*?

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> dolar     = 3.25
         >>> celular   = 299.99
         >>> chaleira  = 23.87
         >>> gnomo     = 66.66
         >>> unicórnio = 1.42
         >>> frete     = 12.34
         >>> total_dolares          = celular + chaleira + gnomo + 6 * unicórnio
         >>> total_dolares_comfrete = celular + chaleira + gnomo + 6 * unicórnio + frete
         >>> IOF = 6.38 / 100
         >>> total_reais = total_dolares_comfrete * dolar * (1 + IOF)
         >>> imposto = total_dolares_comfrete * dolar * IOF

         >>> total_dolares
         399.03999999999996
         >>> total_dolares_comfrete
         411.37999999999994
         >>> total_reais # item b
         1422.284643
         >>> imposto     # item c
         85.29964299999999
