#. Supondo que a cotação do dólar esteja em :math:`\mathrm{R}\$\, 3{,}25`,
   salve esse valor em uma variável e utilize-o para calcular quanto você
   teria ao cambiar :math:`\mathrm{R}\$\, 65{,}00` para dólares.

#. Abelindo é um professor muito malvado. Ele quer decidir como reprovar
   Rondineli, que tirou 8.66, 5.35, 5 e 1, respectivamente nas provas
   P1, P2, P3 e P4. Para isso, ele pode calcular a nota final usando média
   aritmética (M.A.), média geométrica (M.G.) ou média harmônica (M.H.).

   .. math::

      M.A. = \frac{P_1 + P_2 + P_3 + P_4}{4}

   .. math::

      M.G. = \sqrt[4]{|P_1 P_2 P_3 P_4|}

   .. math::

      M.H. = \frac{4}{\frac{1}{P_1} + \frac{1}{P_2} + \frac{1}{P_3} + \frac{1}{P_4}}

   Qual dessas médias dá a maior nota pra Rondineli? E qual das médias dá
   a pior nota?

   .. only:: instructors

      Exemplo de solução:

      .. code:: python

         p1 = 8.66
         p2 = 5.35
         p3 = 5
         p4 = 1
         MA = (p1 + p2 + p3 + p4) / 4
         MG = (p1 * p2 * p3 * p4)**(1/4)
         MH = 4 / (1/p1 + 1/p2 + 1/p3 + 1/p4)
         print(MA, MG, MH)
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

      .. code:: python

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

#. D3yver50n resolveu minerar criptomoedas. Ele decidiu minerar *Ethereum* e viu
   que :math:`1\, ETH = $687.86\, USD` e :math:`$1\, USD = R$3.59`. Ele comprou
   o seguinte computador:

   - 5 placas de vídeo: GTX1080 TI, cada uma por R$5270,90

   - 1 placa mãe: ASRock H110 Pro, por R$920

   - 1 fonte: 1000 W, por R$1149,90

   - 1 HD: 1 TB, SATA3, 7200 RPM por R$208,90

   - 2 pentes de memória: 4 GB, DDR4, 2400 MHZ, cada um por R$259,90

   - 1 CPU: Intel Core i5-8500 por R$899,90

   E resolveu montar usando uma estante de madeira e dois tijolos, para coolear
   melhor:

   .. figure:: images/cluster.jpg
      :align: center
      :width: 70%

   Essas GPUs conseguem minerar Ethereum a uma taxa de :math:`\approx 27 Mh/s`
   (mega hash / s). Cada bloco minerado dá uma recompensa de 3 ETH.
   Considere a dificuldade da rede de :math:`3.29 \cdot 10^{15}`,
   o *block time* médio de :math:`15.44\, s`.

   Para calcular quantos dólares por segundo ele vai ganhar com esse computador,
   D3yver50n fez as seguintes contas:

   .. math::

        ETH / s = \mathrm{cluster\_ratio} \frac{recompensa}{\mathrm{block\_time}}

   O cluster_ratio é calculado como:

   .. math::

      \mathrm{cluster\_ratio} = n_\mathrm{GPU} \frac{\mathrm{GPU\_hashrate}}{\mathrm{network\_hashrate}}

   onde :math:`n_\mathrm{GPU}` é o número de placas de vídeo que ele tem.
   O network_hashrate é calculado como:

   .. math::

      \mathrm{network\_hashrate} = \frac{\mathrm{dificuldade}}{\mathrm{block\_time}}

   a. Calcule quantos ETH por segundo D3yver50n vai ganhar com esse PC.

   b. Calcule quantos dólares por segundo ele vai ganhar.

   c. Calcule quanto ele vai pagar de energia elétrica por segundo para manter
      esse computador ligado, sabendo que o custo de energia elétrica é de
      :math:`0.008 \mathrm{ centavos} / kW`.

   d. Após um mês, quantos ETH ele vai ganhar? Isso equivale a quantos reais?
      Quanto de energia elétrica ele vai gastar? Deu lucro ou prejuízo?

   e. Se ele teve lucro, após quanto tempo ele ganha o dinheiro que investiu
      no computador de volta?


   .. only:: instructors

      Exemplo de solução:

      .. code:: python

         # item a - ETH / s
         GPU_hashrate = 27e6 # Hash/s
         n_GPU = 5
         difficulty = 3.29e15
         block_time = 15.44
         reward = 3

         network_hashrate = difficulty / block_time
         cluster_ratio = n_GPU * GPU_hashrate / network_hashrate
         ETH_s = cluster_ratio * reward / block_time
         print("ETH / s: ", ETH_s)

         # item b - dólar / s
         ETH = 687.86 # 1 ETH = 687.86 USD
         dólar_s = ETH_s * ETH
         print("USD / s: ", dólar_s)

         # item c - energia elétrica
         kW = 0.008 / 100 # 1 kW = R$0.00008
         potência = 1 / .8  # potência da fonte / eficiência dela :P convertida pra kW
         energia_s = potência * kW
         print("R$ de energia / s: ", energia_s)

         # item d - tudo isso depois de um mês
         mês = 30 * 24 * 60 * 60 # 1 mês em segundos
         dólar = 3.25

         ETH_mês     = ETH_s * mês
         dólar_mês   = dólar_s * mês
         reais_mês   = dólar_mês * dólar
         energia_mês = energia_s * mês
         profit = reais_mês - energia_mês
         print("ETH / mês: ", ETH_mês)
         print("USD / mês: ", dólar_mês)
         print("R$  / mês: ", reais_mês)
         print("R$ energia / mês: ", energia_mês)
         print("Lucro (R$) / mês: ", profit)
         print("")

         # item e - tempo pra recuperar o investimento
         GTX  = 5270.90
         mobo =  920.00
         PSU  = 1149.90
         HD   =  208.90
         ram  =  259.90
         CPU  =  899.90
         custo_total = 5 * GTX + mobo + PSU + HD + 2 * ram + CPU
         print("Custo do hardware (R$): ", custo_total)

         tempo = custo_total / profit
         print("Tempo para recuperar investimento (em meses): ", tempo)

      .. code:: bash

         $ python eth.py
         ETH / s:  1.231003039513678e-07
         USD / s:  8.467577507598785e-05
         R$ de energia / s:  0.0001
         ETH / mês:  0.3190759878419453
         USD / mês:  219.4796089969605
         R$  / mês:  713.3087292401217
         R$ energia / mês:  259.2
         Lucro (R$) / mês:  454.1087292401217

         Custo do hardware (R$):  30053.000000000004
         Tempo para recuperar investimento (em meses):  66.18018563591343

#. Joilson está aprendendo Arduino. Ele quer ligar LEDs nas saídas digitais
   do Arduino. Cada pino fornece :math:`5\, V`. Joilson sabe que tem que ligar
   um resistor em série com o LED para não queimar. Calcule o valor do
   resistor que deve ser ligado para cada um desses LEDs, sabendo que a corrente
   de operação de cada um dos LEDs é de :math:`20\, mA`:

   - LED vermelho: opera em :math:`2.0\, V`

   - LED verde: opera em :math:`3.2\, V`

   - LED roxo: opera em :math:`3.7\, V`
