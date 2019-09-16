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

.. _section_fatias_strings:

Fatias
------

Se, ao invés de obter apenas um elemento de uma estrutura (*string*, lista,
...), deseja-se obter múltiplos elementos, deve-se utilizar *slicing*
(fatiamento). No lugar de colocar o índice do elemento entre chaves,
deve-se colocar o índice do primeiro elemento, dois pontos (``:``) e o
próximo índice do último elemento desejado, tudo entre colchetes. Por
exemplo:

.. doctest::

   >>> frase = "Aprender Python é muito divertido!"
   >>> frase[0]
   'A'
   >>> frase[5]
   'd'
   >>> frase[0:5] # do zero até o antes do 5
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
   >>> frase[0:-6]
   'Aprender Python é muito dive'
   >>> frase[0:-7]
   'Aprender Python é muito div'
   >>> frase[2:-2]
   'render Python é muito divertid'

É possível controlar o *passo* que a fatia usa. Para isso, coloca-se mais
um dois pontos (``:``) depois do segundo índice e o *tamanho do passo*:

.. doctest::

   >>> frase[::1] # do começo, até o fim, de 1 em 1. Ou seja, tudo do jeito que ja era, não faz diferença nenhuma.
   'Aprender Python é muito divertido!'
   >>> frase[::2] # do começo, até o fim, de 2 em 2
   'Arne yhnémiodvrio
   >>> frase[2:-2:2] # Do terceiro, até o ante penúltimo, de 2 em dois
   'rne yhnémiodvri'

Resumindo: para fazer uma fatia de nossa *string*, precisamos saber de onde
começa, até onde vai e o tamanho do passo.

.. code::

   fatiável[começo : fim : passo]

.. note::

   As fatias incluem o índice do primeiro elemento e *não incluem* o elemento do índice final. Por isso que ``frase[0:-1]`` perde o último elemento.

Caso o final da fatia seja antes do começo, obtemos um resultado vazio:

.. doctest::

   >>> frase[15:2]
   ''

E se quisermos uma fatia fora da string?

.. doctest::

   >>> frase[123:345]
   ''

Mas e se o final da fatia for mais para frente que o tamanho da *string*? Não
tem problemas, o Python vai até o onde der:

.. doctest::

   >>> frase[8:123456789]
   ' Python é muito divertido!'
   >>> frase[8:]
   ' Python é muito divertido!'
   >>> frase[123456789]
   Traceback (most recent call last):
     File "<stdin>", line 1, in <module>
   IndexError: string index out of range

Tamanhos negativos de passo também funcionam. Passos positivos significam *para
frente* e passos negativos significam *para trás*:

.. doctest::

   >>> "Python"[::-1]
   'nohtyP'

Quando usamos passos negativos, a fatia começa no fim e termina no começo e
é percorrida ao contrário. Ou seja, invertemos a ordem. Mas tome cuidado:

.. doctest::

   >>> "Python"[2:6]
   'thon'
   >>> "Python"[2:6:-1]
   ''
   >>> "Python"[6:2]
   ''
   >>> "Python"[6:2:-1]
   'noh'

No caso de ``"Python"[6:2]``, o começo é depois do fim. Por isso a *string*
fica vazia.

No caso de ``"Python"[2:6:-1]``, o começo é o índice ``6``, o fim é o índice
``2``, percorrida ao contrário. Ou seja, temos uma *string* vazia ao
contrário, que continua vazia.

Quando fazemos ``"Python"[6:2:-1]``, o começo é o índice ``2``, o fim é o índice
``6``, percorrida ao contrário. Lembre que o índice final nunca é incluído.
Ou seja, temos a *string* ``hon`` a ser invertida. O que resulta em ``noh``.

.. dica::

   Se você quiser fazer uma fatia invertida, ou seja, inverter um trecho de
   uma *string*, é muito mais fácil fazer primeiro a fatia e depois a
   inversão:

   .. doctest::

      >>> texto = "No alto da montanha havia uma rosa"
      >>> texto[3:19]
      'alto da montanha'
      >>> texto[3:19][::-1]
      'ahnatnom ad otla'


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


Além disso, também é possível usar nomes para identificar quais valores serão
substituídos:

.. doctest::

   >>> '{a}, {a}, {a}. {b}, {b}, {b}'.format(a='oi', b='tchau')
   'oi, oi, oi. tchau, tchau, tchau'


Alternativa ao `.format()`
__________________________

Uma maneira mais recente de formatar strings foi introduzida a partir da versão
3.6 do Python: `PEP 498 -- Literal String Interpolation`, carinhosamente
conhecida como `fstrings` e funciona da seguinte forma:

.. doctest::

   >>> nome = 'Silvio'
   >>> f'Olá, {name}.'
   'Olá, Silvio.'


É também possível fazer operações:

.. doctest::

   >>> f'4654 * 321 é {4654 * 321}'
   '4654 * 321 é 1493934'



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
