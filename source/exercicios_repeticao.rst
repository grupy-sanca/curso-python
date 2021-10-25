#. Calcule a tabuada do 13.

#. Ler do teclado uma lista com 5 inteiros e imprimir o menor valor.

#. Ler do teclado uma lista com 5 inteiros e imprimir ``True`` se a lista
   estiver ordenada de forma crescente ou False caso contrário.

#. Exiba em ordem decrescente todos os números de 500 até 10.

#. Ler do teclado 10 números e imprima a quantidade de números entre 10 e 50.

#. Ler do teclado a idade e o sexo de 10 pessoas, calcule e imprima:

        a) idade média das mulheres

        #) idade média dos homens

        #) idade média do grupo

#. Calcule o somatório dos números de 1 a 100 e imprima o resultado.

#. Receba dois números inteiros correspondentes à largura e altura. Devolva uma cadeia de caracteres ``#`` que representa um retângulo com as medidas fornecidas.

#. Ler do teclado um número inteiro e imprimir se ele é primo ou não.

#. Um restaurante que enfrenta problemas com sua capacidade de clientes pediu sua ajuda para fazer um programa
   para saber quando eles atingem sua capacidade máxima. Faça um programa que leia um número inteiro da capacidade
   máxima do restaurante, e depois pergunte e leia a quantidade de clientes que chegaram até ocupar toda a capacidade
   do restaurante e quando lotar imprima na tela "Restaurante lotado, não há mais mesas disponíveis".

#. O grupy-sanca tem uma fixação com números primos, e é uma tradição marcar seus
   eventos em horas e minutos que sejam números primos, como por exemplo 19:31.

   Você ficou responsável por marcar o próximo Pylestras, e, seguindo a tradição,
   gostaria de marcar o evento para um horário cuja hora e minuto sejam números primos.

   Para escolher a melhor opção, você gostaria de saber todos os horários que
   satisfazem esta condição!

   Crie um programa que imprime no formato ``HH:MM`` todos os horários cuja hora e
   minuto são números primos.

   .. note:: Zero não é um número primo e divisões por zero podem estragar suas contas!

   .. only:: instructors

      Exemplo de solução:

      .. code-block:: python3

           horas = 24
           minutos = 60

           for hora in range(horas):
               hora_primo = 0
               for divisor in range(1, hora):
                   if hora % divisor == 0:
                       hora_primo += 1
               if hora_primo == 1:
                   for minuto in range(minutos):
                       minuto_primo = 0
                       for divisor in range(1, minuto):
                           if minuto % divisor == 0:
                               minuto_primo += 1
                       if minuto_primo == 1:
                           print(f"{hora}:{minuto}")

#. As reuniões mais memoráveis do grupy-sanca são, sem dúvidas, os PyBares!
   Quando finalmente foi decretado o final da pandemia de Covid-19, pythonistas
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

   Você pegou no Meetup uma lista com N nomes de participantes, a duração do evento
   é de 2 horas, e cada rodada dura 5 minutos. Caso você chegue ao final da lista e
   o tempo ainda não tiverem passado as 2h do Coding Dojo, você começará de novo.

   .. note:: Utilize o operador de resto da divisão (``%``)  para iterar circularmente sobre a lista.

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
