Introdução
==========

.. todo:: dar uma introduzida no assunto, talvez só copiar o texto do doc
          do SESC. Ou não

É muito comum apresentar uma nova linguagem com um exemplo simples que mostra
na tela as palavras Hello World. Antes de adentrar o mundo do Python, vamos
ver como outras linguangens de programação o implementam:

**C**

.. code:: C

   #include <stdio.h>

   int main(int argc, char *argv[]){
       printf("Hello, world\n");
       return 0;
   }

**Java**

.. code:: java

   public class Hello {
         public static void main(String []args) {
            System.out.println("Hello World");
         }
   }

* É obrigatório colocar o programa em um arquivo chamado Hello.java

**Pascal**

.. code:: pascal

   program HelloWorld;

   begin
       writeln('Hello World');
   end.

**Python**

Vamos ver como é o Hello World em Python, escreva este texto abaixo com o
shell do python aberto e clique enter:

.. code:: python

   print("Hello, World!")

.. code::

   Hello, World!


É muito comum utilizar a palavra "imprimir" (ou print em inglês) quando
queremos indicar que o programa irá imprimir (mostrar) o resultado na tela.

.. todo:: como abrir o shell, idle