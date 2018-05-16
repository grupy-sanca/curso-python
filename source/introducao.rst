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


Função print
------------

``print()`` é uma função nativa do Python. Basta colocar algo dentro dos
parênteses que o Python se encarrega de fazer a magia de escrever na tela :)

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

.. code:: python

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

E como faz para imprimir um texto em várias linhas? Bom, para isso precisamos
lembrar de um carácter especial, a *quebra de linha*: `\n`. Esse `\n` é um
caracter especial que significa *aqui acaba a linha, o que vier depois deve
ficar na linha de baixo*. Por exemplo:

.. doctest::

  >>> print('Olha esse textão sobre áspas simples e dúplas.\nIsso aqui é áspas duplas: "\nIsso aqui é áspas simples: \''
  Olha esse textão sobre áspas simples e dúplas.
  Isso aqui é áspas duplas: "
  Isso aqui é áspas simples: '
