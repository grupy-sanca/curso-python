Como nomear em Python?
=========

Uma situação comum para programadores é ler e contribuir com códigos feitos por outras pessoas, por isso a importância da padronização da escrita. 
Convenções de escrita de código viabilizam que diversos contribuidores sigam um mesmo padrão, deixando o código mais legível.
As convenções de escrita de código para Python são regidas pela PEP8, disponível em https://peps.python.org/pep-0008/. 
Aqui apresentamos algumas convenções básicas da PEP8 quanto a nomenclatura para você de início já sair programando como um profissional ;-)  

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
