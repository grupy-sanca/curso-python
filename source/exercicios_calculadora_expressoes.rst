
#. Quantos segundos há em 3 horas, 23 minutos e 17 segundos?

#. Se você correr 65 quilômetros em 3 horas, 23 minutos e 17 segundos, qual
   é a sua velocidade média em m/s?

#. Resolva essa expressão:

   .. math::

      \frac{100 - 413 \cdot (20 - 5 \times 4)}{5}

#. Enivaldo quer ligar três capacitores, de valores:

   - :math:`C_1 = 10  \, \mu F`
   - :math:`C_2 = 22  \, \mu F`
   - :math:`C_3 =  6.8\, \mu F`

   Se ele ligar os três em paralelo, a capacitância resultante é a soma:

   .. math::

      C_p = C_1 + C_2 + C_3

   Se ele ligar os três em série, a capacitância resultante é:

   .. math::

      \frac{1}{C_s} = \frac{1}{C_1} + \frac{1}{C_2} + \frac{1}{C_3}

   Ou seja:

   .. math::

      C_s = \frac{1}{\frac{1}{C_1} + \frac{1}{C_2} + \frac{1}{C_3}}

   Qual é o valor resultante em cada um desses casos?

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> 10 + 22 + 0.8 # em paralelo, resposta em µF
         32.8
         >>> 1 / (1 / 10 + 1 / 22 + 1 / 0.8) # em série, resposta em µF
         0.7166123778501629
         >>> 1 / (1 / 10e-6 + 1 / 22e-6 + 1 / 0.8e-6) # em série, resposta em F
         7.166123778501629e-07

#. Você e os outros integrantes da sua república (Joca, Moacir, Demival e
   Jackson) foram no supermercado e compraram alguns itens:

   - 75 latas de cerveja: R\$ 2,20 cada (da ruim ainda, pra fazer o dinheiro render)

   - 2 pacotes de macarrão: R\$ 8,73 cada

   - 1 pacote de Molho de tomate: R\$ 3,45

   - 420g Cebola: R\$ 5,40/kg

   - 250g de Alho: R\$ 30/kg

   - 450g de pães franceses: R\$ 25/kg

   Calcule quanto ficou para cada um.

#. Krissia gosta de bolinhas de queijo. Ela quer saber quantas bolinhas de
   queijo dá para colocar dentro de um pote de sorvete de :math:`2\, L`. Ela
   pensou assim:

      *Um pote de sorvete tem dimensões 15 cm x 10 cm x 13 cm.
      Uma bolinha de queijo é uma esfera de raio r = 1.2 cm.
      O fator de empacotamento ideal é 0.74, mas o pote de sorvete tem
      tamanho comparável às bolinhas de queijo, aí tem efeitos de borda, então 
      o fator deve ser menor. Mas as bolinhas de queijo são razoavelmente
      elásticas, então empacota mais. Esse valor parece razoável.*

   Sabendo que o volume de uma esfera de raio :math:`r` é
   :math:`V = \frac{4}{3} \pi r^3`, o volume do pote de sorvete é
   :math:`V = x \cdot y \cdot z` e o fator de empacotamento é a fração de volume
   ocupado pelas bolinhas de queijo. Ou seja, :math:`74 \%` do pote de sorvete
   vai ser ocupado pelas bolinhas de queijo.

   Ajude a Krissia descobrir quantas bolinhas de queijo cabem no pote de sorvete!

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> from math import pi, floor
         >>> 15 * 10 * 13 * 0.74 / (4 / 3 * pi * 1.2**3)
         199.35814486250436
         >>> floor(15 * 10 * 13 * 0.74 / (4 / 3 * pi * 1.2**3))
         199