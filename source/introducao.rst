Introdução
==========


Hello World
-----------

É muito comum, ao apresentar uma nova linguagem, começar com um exemplo simples que mostra
na tela as palavras `Hello World`. Para não perder o costume, antes de adentrar
o mundo do Python, vamos ver como outras linguangens de programação implementam
esse exemplo:

C
~

.. code:: C

   #include <stdio.h>

   int main(int argc, char *argv[]){
       printf("Hello, World!\n");
       return 0;
   }


Java
~~~~

.. code:: java

   public class Hello {
         public static void main(String[] args) {
            System.out.println("Hello, World!");
         }
   }

É obrigatório que o código acima esteja em um arquivo chamado `Hello.java`


Pascal
~~~~~~

.. code:: pascal

   program HelloWorld;

   begin
       writeln('Hello, World!');
   end.


Python
~~~~~~

Vamos ver como é o Hello World em Python. Para isso, abra o `shell` do
Python e digite o texto abaixo (não esqueça de apertar `enter` no final):

.. doctest::

   >>> print("Hello, World!")
   Hello, World!


Em programação, é muito comum utilizar a palavra `imprimir` (ou `print`, em
inglês) como sinônimo de mostrar algo na tela.


IDLE
----

Para usuários Windows é recomendado utilizar o `IDLE`. Ele é composto pelo interpretador do Python e um editor de texto para criar programas.
Após seguir o :ref:`intro-instalacao`, o menu inicial deve estar da seguinte
forma:

.. figure:: images/idle1.png
   :align: center
   :scale: 80%

Ao abrir o `IDLE (Python 3.X)`, aparecerá uma janela como na
imagem abaixo:

.. figure:: images/idle2.png
   :align: center
   :scale: 80%

No `IDLE` é possível digitar comandos para o interpretador do Python e, também,
é possível criar e digitar em um arquivo. Para fazer isso, no menu clique em
`File` -> `New File` (Ou pressione as teclas `Ctrl` + `N` juntas)

.. figure:: images/idle3.png
   :align: center
   :scale: 80%

Para rodar um programa, clique em `Run` -> `Run Module` (Ou aperte a tecla `F5`)

.. figure:: images/idle4.png
   :align: center
   :scale: 80%

Caso o arquivo ainda não tenha sido salvo, é necessário salvá-lo antes de
executá-lo. Não esqueça de prefixar o nome do arquivo com `.py`
(extensão do Python):

.. figure:: images/idle5.png
   :align: center
   :scale: 80%

Após isso, o resultado da execução do código deve aparecer na janela anterior do `IDLE`:

.. figure:: images/idle6.png
   :align: center
   :scale: 80%


Função print
------------

Erros comuns
~~~~~~~~~~~~

Usar a letra `P` maiúscula ao invés de minúscula: 

.. doctest::

  >>> Print("Hello, World!")
  Traceback (most recent call last):
      ...
  NameError: name 'Print' is not defined

Esquecer de abrir e fechar áspas no texto que é passado para a função
``print()``:

.. doctest::

  >>> print(Hello, World!)
  Traceback (most recent call last):
      ...
  SyntaxError: invalid syntax

Esquecer de abrir ou fechar as aspas:

.. doctest::

  >>> print("Hello, World!)
  Traceback (most recent call last):
      ...
  SyntaxError: EOL while scanning string literal

Começar com aspas simples e terminar com aspas duplas ou vice-versa:

.. doctest::

  >>> print('Hello, World!")
  Traceback (most recent call last):
      ...
  SyntaxError: EOL while scanning string literal

Usar espaço ou tab antes do ``print()``:

.. doctest::

  >>>  print('Hello, World!')
  Traceback (most recent call last):
      ...
  IndentationError: unexpected indent

  >>>     print('Hello, World!')
  Traceback (most recent call last):
      ...
  IndentationError: unexpected indent

Mas, e se eu precisar usar aspas dentro do texto a ser mostrado na tela? Bem, Caso queira imprimir
aspas duplas, envolva tudo com aspas simples e use aspas duplas na parte desejada:

.. doctest::

  >>> print('Python é legal! Mas não o "legal" como dizem pra outras coisas')
  Python é legal! Mas não o "legal" como dizem pra outras coisas

Caso deseje imprimir aspas simples, faça o contrário (envolva com aspas duplas e use aspas simples onde necessário):

.. doctest::

  >>> print("Python é legal! Mas não o 'legal' como dizem pra outras coisas")
  Python é legal! Mas não o 'legal' como dizem pra outras coisas
