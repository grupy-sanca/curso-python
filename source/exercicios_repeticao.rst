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

   OBS: zero não é um número primo e divisões por zero podem estragar suas contas!

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
