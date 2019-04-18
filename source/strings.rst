`Strings` (sequência de caracteres)
===================================

*Strings* são tipos que armazenam uma *sequência de caracteres*:

.. doctest::

   >>> "Texto bonito"
   'Texto bonito'
   >>> "Texto com acentos de cedilhas: hoje é dia de caça!"
   'Texto com acentos de cedilhas: hoje é dia de caça!'

As *strings* aceitam aspas simples também:

.. doctest::

   >>> nome = 'Silvio Santos'
   >>> nome
   'Silvio Santos'

.. note:: *Strings* aceitam os dois tipos de aspas, desde que seja
   consistente. Se começou com uma, termine com aquela!

.. doctest::

   >>> cor_da_caneta = "azul brilhante'
     File "<stdin>", line 1
       cor_da_caneta = "azul brilhante'
                                      ^
   SyntaxError: EOL while scanning string literal

Também é possível fazer algumas operações com strings:

.. doctest::

   >>> nome * 3
   'Silvio SantosSilvio SantosSilvio Santos'
   >>> nome * 3.14
   Traceback (most recent call last):
       ...
   TypeError: can't multiply sequence by non-int of type 'float'

.. doctest::

   >>> canto1 = 'vem aí, '
   >>> canto2 = 'lá '
   >>> nome + ' ' + canto1 + canto2 * 6 + '!!'
   'Silvio Santos vem aí, lá lá lá lá lá lá !!'

Para strings em várias linhas, utilize 3 aspas:

.. doctest::

   >>> string_grande = '''Aqui consigo inserir um textão com várias linhas, posso iniciar em uma...
   ... e posso continuar em outra
   ... e em outra
   ... e mais uma
   ... e acabou.'''
   >>> string_grande
   'Aqui consigo inserir um textão com várias linhas, posso iniciar em uma...\ne posso continuar em outra\ne em outra\ne mais uma\ne acabou.'
   >>> print(string_grande)
   Aqui consigo inserir um textão com várias linhas, posso iniciar em uma...
   e posso continuar em outra
   e em outra
   e mais uma
   e acabou.

Caso queira um texto que dentro tem aspas, como ``Me dá um copo d'água``, é
necessário utilizar aspas duplas para formar a *string*:

.. doctest::

   >>> agua = "Me dá um copo d'água"
   >>> agua
   "Me dá um copo d'água"

E também é possível utilizar aspas simples, duplas e triplas ao mesmo tempo!
Olha só:

.. doctest::

   >>> todas_as_aspas = """Essa é uma string que tem:
   ... - aspas 'simples'
   ... - aspas "duplas"
   ... - aspas '''triplas'''
   ... Legal né?"""
   >>> todas_as_aspas
   'Essa é uma string que tem:\n- aspas \'simples\'\n- aspas "duplas"\n- aspas \'\'\'triplas\'\'\'\nLegal né?'
   >>> print(todas_as_aspas)
   Essa é uma string que tem:
   - aspas 'simples'
   - aspas "duplas"
   - aspas '''triplas'''
   Legal né?


Tamanho
-------

A função embutida ``len()`` nos permite, entre outras coisas, saber o
tamanho de uma *string*:

.. doctest::

   >>> len('Abracadabra')
   11
   >>> palavras = 'Faz um pull request lá'
   >>> len(palavras)
   22

Assim, vemos que a palavra ``Abracadabra`` tem 11 letras.


Índices
-------

Como visto anteriormente, o método ``len()`` pode ser utilizado para obter o
tamanho de estruturas, sejam elas *strings*, listas, etc. Esse tamanho
representa a quantidade de elementos na estrutura.

Para obter somente um caractere de dentro dessas estruturas, deve-se utilizar
o acesso por índices, no qual o índice entre colchetes ``[]`` representa a
posição do elemento que se deseja acessar.

.. note:: Os índices começam em zero.

.. figure:: images/indices.png
   :align: center
   :scale: 80%

.. doctest::

   >>> palavra = 'Python'
   >>> palavra[0] # primeira
   'P'
   >>> palavra[5] # última
   'n'

Índices negativos correspondem à percorrer a estrutura (string, lista,
...) na ordem reversa:

.. doctest::

   >>> palavra[-1] # última também
   'n'
   >>> palavra[-3] # terceira de tras pra frente
   'h'


Fatias
------

Se ao invés de obter apenas um elemento de uma estrutura (*string*, lista,
...) deseja-se obter múltiplos elementos, deve-se utilizar *slicing*
(fatiamento). No lugar de colocar o índice do elemento entre chaves,
deve-se colocar o índice do primeiro elemento, dois pontos (``:``) e o
próximo índice do último elemento desejado, tudo entre colchetes.

.. doctest::

   >>> frase = "Aprender Python é muito divertido!"
   >>> frase[0:5] # do zero até o 5
   'Apren'
   >>> frase[:] # tudo!
   'Aprender Python é muito divertido!'
   >>> frase
   'Aprender Python é muito divertido!'
   >>> frase[6:] # Se omitido o segundo índice significa 'obter até o final'
   'er Python é muito divertido!'
   >>> frase[:6] # se omitido o primeiro indice, significa 'obter desde o começo'
   'Aprend'
   >>> frase[2:-3] # funciona com números negativos também
   'render Python é muito diverti'
   >>> frase[0:-5]
   'Aprender Python é muito diver'
   >>> frase[2:-2]
   'render Python é muito divertid'
   >>> frase[2:-2:2] # pode-se ecolher o passo com que o slice é feito
   'rne yhnémiodvri'


Formatação de strings
---------------------

A formatação de string nos permite criar frases dinâmicas, utilizando
valores de quaisquer variáveis desejadas. Por exemplo:

.. testsetup:: string_format

   def input(text):
       value = "Silvio Santos"
       print(text + value)
       return value

.. doctest:: string_format

   >>> nome = input('Digite seu nome ')
   Digite seu nome Silvio Santos
   >>> nome
   'Silvio Santos'
   >>> frase = 'Olá, {}'.format(nome)
   >>> frase
   'Olá, Silvio Santos'

Vale lembrar que as chaves ``{}`` só são trocadas pelo valor após a chamada do
método ``str.format()``:

.. doctest::

   >>> string_a_ser_formatada = '{} me formate!'
   >>> string_a_ser_formatada
   '{} me formate!'

   >>> string_a_ser_formatada.format("Não")  # também podemos passar valores diretamente para formatação, apesar de ser desncessário
   'Não me formate!'

A string a ser formatada não é alterada nesse processo, já que não foi
feita nenhuma atribuição:

.. doctest::

   >>> string_a_ser_formatada
   '{} me formate!'

É possível formatar uma quantidade arbitrária de valores:

.. doctest::

   >>> '{} x {} = {}'.format(7, 6, 7 * 6)
   '7 x 6 = 42'

.. doctest::

   >>> palavra = 'Python'
   >>> numero = 10
   >>> booleano = False
   >>> '{} é {}. E as outras linguagens? {}'.format(palavra, numero, booleano)
   'Python é 10. E as outras linguagens? False'


Separação de *Strings*
----------------------

Se tivermos a frase ``Sílvio Santos vem aí, oleoleolá!`` e quisermos separar
cada palavra, como fazer? Pode-se usar o fatiamento:

.. doctest::

   >>> frase = "Sílvio Santos vem aí, oleoleolá!"
   >>> frase[:6]
   'Sílvio'
   >>> frase[7:13]
   'Santos'
   >>> frase[14:17]
   'vem'
   >>> frase[18:21]
   'aí,'
   >>> frase[22:]
   'oleoleolá!'

Mas também podemos usar a função ``split()``:

.. doctest::

   >>> frase.split()
   ['Sílvio', 'Santos', 'vem', 'aí,', 'oleoleolá!']

.. note::

        É possível transformar uma string em número, dado que seja um número:

        .. doctest::

                >>> numero = int("2")
                >>> numero
                2

.. note::

        A volta também é possível:

        .. doctest::

                >>> numero_string = str(1900)
                >>> numero_string
                '1900'
                >>> type(numero_string)
                <class 'str'>


Exercícios
----------

.. include:: exercicios_string.rst
