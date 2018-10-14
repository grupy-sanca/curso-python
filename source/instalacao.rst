.. _intro-instalacao:

Guia de Instalação do Python
============================

Linux - Ubuntu
--------------

Provavelmente você já tem o Python instalado e configurado. Para ter certeza
que ele está instalado e descobrir qual versão, abra um terminal e execute o
comando:

.. code::

   $ python --version

Se o resultado do comando for `Python 3.6.5` (ou alguma versão igual ou
superior a `3.5`) o Python já está instalado corretamente.

Caso o resultado do comando anterior tenha sido `Python 2.7.13` (ou qualquer
versão do `Python 2`) tente rodar o seguinte comando, pois seu computador
pode ter ambas versões `2` e `3` instaladas:

.. code::

    $ python3 --version

Caso tenha aparecido a mensagem ``bash: python: command not found``, você pode
instalá-lo da seguinte maneira:

.. code::

   $ sudo apt install python3.6


Mac OS X
--------

Obtenha o instalador na sessão de downloads para `Mac OS X do Python`_. Clique
duas vezes no Python.mpkg para abrir o instalador.

Para ter certeza que ele está instalado e descobrir qual versão, abra um
terminal e execute o comando:

.. code::

   $ python --version
   Python 3.6.5


Windows
-------

Primeiramente, deve-se obter o arquivo de instalação compatível com a
arquitetura. O arquivo x86 provavelmente funcionará para todos computadores,
os links estão a seguir:

    - x86_64_
    - x86_

A seguir, o aquivo deve ser executado e a seguinte imagem aparecerá:

.. figure:: images/install1.png
   :align: center
   :width: 80%

Deve ser selecionado a opção `Add Python 3.6 to PATH`, e deve ser clicado na
opção 'Customize installation'

.. figure:: images/install2.png
   :align: center
   :width: 80%

Clique em 'Next'

.. figure:: images/install3.png
   :align: center
   :width: 80%

Selecionar a opção `Install for all users` e clicar em `Install`. Então, uma
janela pedindo permissão de administrador deve aparecer, é necessário aceitar

.. figure:: images/install4.png
   :align: center
   :width: 80%

Selecione `Disable path lenght limit` e, novamente, uma janela de permissão de
administrador irá aparecer, é necessário aceitar

.. figure:: images/install5.png
   :align: center
   :width: 80%

Clique em `Close`

Parabéns, agora o Python está intalado em sua máquina!


.. _Mac OS X do Python: https://www.python.org/downloads/mac-osx/
.. _x86_64: https://www.python.org/ftp/python/3.6.5/python-3.6.5-amd64.exe
.. _x86: https://www.python.org/ftp/python/3.6.5/python-3.6.5.exe


Ambientes de Desenvolvimento
============================

Há diversos programas para desenvolvermos códigos, alguns são mais bonitinhos,
outros são mais poderosos, alguns são mais simples, outros são mais amigaveis.
Dê uma olhada nesta seção e escolha o que você achar mais interessante. Somente
você pode responder à pergunta "Qual o melhor ambiente de desenvolvimento para
*mim*?"

IDE (*Integrated Development Environment* - Ambiente de Desenvolvimento Integrado, em português)
é um editor de texto que possui ferramentas e recursos que facilitam a vida do programador.
Entre as ferramentas e recursos, podemos citar:

- Identificar quais variavéis foram declaradas.
- Identificar erros no código.
- Personalizar o ambiente de trabalho.
- Ocultar parte do código para melhor visualização.

Linha de comando
----------------

.. explicar que tem que abrir um editor de texto e o shell para trabalhra com arquivos

.. colocar aqui como abrir o shell do python no windows e no Linux

.. colocar aqui o ipython

Ambientes gráficos
------------------

ATOM
~~~~

O programa ATOM é um IDE *open-source* que apresenta diversos pacotes para personalizar.

.. figure:: images/ide_Atom.png
   :align: center
   :width: 80%

No site oficial do `ATOM <https://atom.io>`_, você encontrará um link para a Documentação do programa. 
Na documentação, é possível acessar o `manual <https://flight-manual.atom.io/getting-started/sections/installing-atom/#platform-windows>`_ que mostrará passo a passo como instalar o programa (tanto para Windows como para Linux).

Caso você tenha alguma dúvida, é aconselhavel entrar na seção de `discursão <https://discuss.atom.io/>`_. Nessa página, você encontrará respostas para diversas dúvidas, e possívelmente, para a sua.

IDLE
~~~~

Para usuários Windows é recomendado utilizar o `IDLE`. Ele é composto pelo interpretador do Python e um editor de texto para criar programas.
Após seguir o :ref:`intro-instalacao`, o menu inicial deve estar da seguinte
forma:


.. figure:: images/idle1.png
   :align: center
   :width: 80%

Ao abrir o `IDLE (Python 3.X)`, aparecerá uma janela como na
imagem abaixo:

.. figure:: images/idle2.png
   :align: center
   :width: 80%

No `IDLE` é possível digitar comandos para o interpretador do Python e, também,
é possível criar e digitar em um arquivo. Para fazer isso, no menu clique em
`File` -> `New File` (Ou pressione as teclas `Ctrl` + `N` juntas)

.. figure:: images/idle3.png
   :align: center
   :width: 80%

Para rodar um programa, clique em `Run` -> `Run Module` (Ou aperte a tecla `F5`)

.. figure:: images/idle4.png
   :align: center
   :width: 80%

Caso o arquivo ainda não tenha sido salvo, é necessário salvá-lo antes de
executá-lo. Não esqueça de prefixar o nome do arquivo com `.py`
(extensão do Python):

.. figure:: images/idle5.png
   :align: center
   :width: 80%

Após isso, o resultado da execução do código deve aparecer na janela anterior do `IDLE`:

.. figure:: images/idle6.png
   :align: center
   :width: 80%

.. colocar aqui outras IDEs
