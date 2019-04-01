.. spelling::

   yver

#. Joilson está aprendendo Arduino. Ele quer ligar LEDs nas saídas digitais
   do Arduino. Cada pino fornece :math:`5\, V`. Joilson sabe que tem que ligar
   um resistor em série com o LED para não queimar. Calcule o valor do
   resistor que deve ser ligado para cada um desses LEDs, sabendo que a corrente
   de operação de cada um dos LEDs é de :math:`20\, mA`:

   - LED vermelho: opera em :math:`2.0\, V`

   - LED verde: opera em :math:`3.2\, V`

   - LED roxo: opera em :math:`3.7\, V`

   Lembre-se que a voltagem é a corrente multiplicada pela resistência:

   .. math::

      V = R I

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

         >>> V_vermelho = 2
         >>> V_verde    = 3.2
         >>> V_roxo     = 3.7
         >>> V_arduino  = 5
         >>> I = 20e-3
         >>> R_vermelho = (V_arduino - V_vermelho) / I
         >>> R_verde    = (V_arduino - V_verde)    / I
         >>> R_roxo     = (V_arduino - V_roxo)     / I
         >>> print(R_vermelho, R_verde, R_roxo)
         150.0, 89.99999999999999, 64.99999999999999

#. D3yver50n resolveu minerar criptomoedas. Ele decidiu minerar *Ethereum* e viu
   que :math:`1\, ETH = \$687.86` e :math:`\$1 = \mathbb{R}\$3.59`. Ele comprou
   o seguinte computador:

   - 5 placas de vídeo: GTX1080 TI, cada uma por R$5270,90

   - 1 placa mãe: ASRock H110 Pro, por R$920

   - 1 fonte: 1600 W, por R$2299,90

   - 1 HD: 1 TB, SATA3, 7200 RPM por R$208,90

   - 2 pentes de memória: 4 GB, DDR4, 2400 MHZ, cada um por R$259,90

   - 1 CPU: Intel Core i5-8500 por R$899,90

   E resolveu montar usando uma estante de madeira e dois tijolos, para refrigerar
   melhor:

   .. figure:: images/cluster.jpg
      :align: center
      :width: 70%

   Essas GPUs (placas de vídeo) conseguem minerar Ethereum a uma taxa de :math:`\approx 27 Mh/s`
   (mega hash / s = :math:`10^6` hash / s). Cada bloco minerado dá uma recompensa
   de 3 ETH. Considere a dificuldade da rede de :math:`3.29 \cdot 10^{15}`,
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

      .. code-block:: python3

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
         potência = 1.6 / .8  # potência da fonte / eficiência dela :P convertida pra kW
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
         PSU  = 2299.90
         HD   =  208.90
         ram  =  259.90
         CPU  =  899.90
         custo_total = 5 * GTX + mobo + PSU + HD + 2 * ram + CPU
         print("Custo do hardware (R$): ", custo_total)

         tempo = custo_total / profit
         print("Tempo para recuperar investimento (em meses): ", tempo)

      .. code-block:: bash

         $ python eth.py
         ETH / s:  1.231003039513678e-07
         USD / s:  8.467577507598785e-05
         R$ de energia / s:  0.00016
         ETH / mês:  0.3190759878419453
         USD / mês:  219.4796089969605
         R$  / mês:  713.3087292401217
         R$ energia / mês:  414.72
         Lucro (R$) / mês:  298.58872924012167

         Custo do hardware (R$):  31203.000000000004
         Tempo para recuperar investimento (em meses):  104.50160017562789