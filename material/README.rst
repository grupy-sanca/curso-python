-------------------
Compilar Localmente
-------------------

1. Neste diretório, use o makefile disponível para gerar o HTML:

   .. code:: sh

        $ make html

   Ou um pdf:

   .. code:: sh

        $ make pdflatex

2. Para ver a documentação localmente, abra a página ``build/html/index.html``
   em seu navegado favorito.

   Ou abra o PDF ``build/latex/CursoIntrodutriodePython.pdf``

------------
Dependências
------------

* Sphinx 1.6+
* Sphinx_rtd_theme
* texlive (para gerar o pdf)
