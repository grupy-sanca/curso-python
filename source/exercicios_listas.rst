#. Crie uma lista com o nome das 3 pessoas mais próximas.

#. Crie três listas, uma lista de cada coisa a seguir:

   * frutas
   * docinhos de festa (não se esqueça de brigadeiros!!)
   * ingredientes de feijoada

   Lembre-se de salvá-las em alguma variável!

   a. Agora crie uma lista que contém essas três listas.

   Nessa lista de listas (vou chamar de *listona*):

   b. você consegue acessar o elemento *brigadeiro*?

   c. Adicione mais *brigadeiros* à segunda lista de listona. O que aconteceu
      com a lista de *docinhos de festa*?

   d. Adicione bebidas ao final da *listona*, mas sem criar uma lista!

#. Utilizando o ``del``, remova todos os elementos da lista criada anteriormente
   até a lista ficar vazia.

#. Faça uma lista de compras do mês, não se esqueça de comprar produtos de
   limpeza e sorvete!

   Agora "vá ao mercado" e delete apenas os produtos de limpeza da lista.

   Agora "vá à sorveteria" e se empanturre de sorvete e tire o sorvete da lista.

#. Dado uma lista de números, faça com que os números sejam ordenados e, em seguida, inverta a ordem da lista usando *slicing*.
#. Receba uma lista com números inteiros e devolva um número inteiro correspondente à soma dos números recebidos.
#. As reuniões mais memoráveis do grupy-sanca são, sem dúvidas, os PyBares!
   Quando finalmente foi decretado o final da pandemia de covid-19, pythonistas
   de São Carlos e região se reuniram para comemorar, e a comemoração foi tanta,
   que neste momento estão com dificuldades de listar quais atividades e
   eventos são organizados pelo grupo, sem repetirem as já listadas.

   Como programar já é a sua especialidade, você resolveu escrever um programa para sanar este
   pequeno problema. Seu programa deve ler um número N que determina quantos eventos
   e atividades foram elencados (que pode ter itens repetidos), e, em seguida,
   N nomes de atividades e eventos organizados pelo grupy-sanca e imprimir uma
   lista ordenada alfabeticamente e sem itens repetidos.

   Dica: utilize o operador ``in`` para testar se uma entrada já está na lista,
   e o método ``sort`` para ordená-la. Também pode ser útil utilizar o método
   ``strip`` no seu ``input`` para evitar que espaços em branco interfiram nas suas
   comparações.

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3
        tentativas = int(input("Digite o número de atividades elencadas: "))
        atividades = []
        for i in range(tentativas):
           palpite_atual = input(f"Digite o nome da {i+1}ª atividade: ").strip()
           if palpite_atual not in atividades:
               atividades.append(palpite_atual)
        atividades.sort()
        print("Atividades sem repetição e ordenadas:")
        print("\n".join(atividades))


#. Uma das atividades preferidas do grupy-sanca é o Coding Dojo.
   Coding Dojo é uma atividade colaborativa onde pessoas se reúnem a fim de
   resolver desafios de programação juntas, programando em pares, e utilizando
   a metodologia de desenvolvimento orientada a testes (TDD). A pessoa na posição
   do piloto programará por 5 minutos, orientada pela pessoa na posição de copiloto,
   e ao final deste tempo, o piloto voltará para a plateia, o copiloto será promovido a piloto
   e uma pessoa da plateia tomará a posição de copiloto.

             plateia -> copiloto -> piloto -> plateia

   Você está responsável pela organização do Coding Dojo de hoje, e, para garantir
   que todas as pessoas participarão da atividade da forma mais justa possível,
   você resolveu criar um programa que imprimirá o nome de cada dupla que representará
   copiloto e piloto em cada rodada.

   Você pegou no meetup uma lista com N nomes de participantes, a duração do evento
   é de 2 horas, e cada rodada dura 5 minutos. Caso você chegue ao final da lista e
   o tempo ainda não tiverem passado as 2h do Coding Dojo, você começará de novo.

   Dicas: utilize o operador de resto da divisão (``%``)  para iterar circularmente sobre a lista.

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3
          num_participantes = int(input("Digite o número de participantes: "))
          participantes = []
          for participante_atual in range(num_participantes):
              participantes.append(input(f"Digite o nome da {participante_atual+1}ª pessoa da lista: ").strip())
          rodadas = 2 * 60 // 5 # duas horas vezes sessenta minutos divididos por 5 minutos cada rodada
          print("Distribuição:")
          for rodada in range(rodadas):
              piloto = participantes[rodada % num_participantes]
              copiloto = participantes[(rodada+1) % num_participantes]
              print(f"piloto: {piloto}\t copiloto: {copiloto}")