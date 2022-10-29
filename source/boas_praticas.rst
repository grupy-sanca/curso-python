Boas práticas de programação
============================

Uma situação comum para programadores é ler e contribuir com códigos feitos por outras pessoas, por isso a importância da padronização da escrita. 
Convenções de escrita de código viabilizam que diversos contribuidores sigam um mesmo padrão, deixando o código mais legível.
As convenções de escrita de código para Python são regidas pela PEP8, disponível em https://peps.python.org/pep-0008/. 
Aqui apresentamos algumas convenções básicas para você de início já sair programando como um profissional ;-)  

Nome de funções e variáveis
-----------
**Nome de variáveis** devem receber nomes em letra minúscula com palavras separadas por '_' (*underscore*) caso seja necessário facilitar a leitura.

**Nomes de funções** seguem o mesma convenção que nomes de funções. 

.. doctest::

   >>> def soma(numero1, numero2)
   ...    return numero1 + numero2

.. doctest::


O uso misturado, ou seja, no qual uma palavra com letras minúsculas é seguido de uma com a primeira letra maiúscula, 
é permitido para caso em que o código pré-existente já esteja escrito desta forma, mantendo-se a compatibilidade.  

.. doctest::

   >>> casoMisto = 20

.. doctest::


Indentação
---------

A orientação é utilizar 4 espaços por nível de identação.
Alguns códigos utilizam tab no lugar de espaços. O recomendável é evitar esta prática a menos que se esteja trabalhando em um código antigo em que a identação já foi feita por tab. A mistura de tabs e espaços **não** deve ser realizada.

Tamanho da linha
----------------
O limite recomendável é 79 caracteres para o código e 72 para comentários e docstrings.
Limitar o tamanho da linha permite que o código seja visualizado melhor na janela, sem quebras e necessidade de 'rolar' para enxergar o que está escrito. 

Quebra de linha em operações
-----------
No Python é permitido quebrar linhas antes ou depois do operador matemático. O importante é manter a consistência. 
Se começar com um padrão sigua até o final do código.

.. doctest::

   >>> feira = (banana
             + abacate
             + laranja
             + alface)
             
   >>> feira = (banana +
                abacate +
                laranja +
                alface)
                 
.. doctest::

