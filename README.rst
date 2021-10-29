Python Course
=============

.. image:: https://readthedocs.org/projects/curso-python/badge/?version=latest
    :target: https://readthedocs.org/projects/curso-python/builds/
    :alt: Documentation Status

.. image:: https://github.com/grupy-sanca/curso-python/actions/workflows/build_spell.yml/badge.svg
    :target: https://github.com/grupy-sanca/curso-python/actions/workflows/build_spell.yml?query=branch%3Amaster
    :alt: Documentation Status

This repo contains the material for the Introductory Python course created by grupy-sanca.

All the material is in pt-br.

Check the material `online here <http://curso.grupysanca.com.br/>`_.

Find us in `Facebook <https://www.facebook.com/grupysanca/>`_,
`Telegram <https://t.me/grupysanca>`_,
`Discord <https://discord.gg/AgS2dBa>`_,
`Instagram <https://www.instagram.com/grupysanca/>`_,
`Meetup <https://www.meetup.com/grupy-sanca>`_ and
`YouTube <https://www.youtube.com/channel/UC9AED1x6Nn10lu-3rNELQnw>`_


How to use locally
------------------

1. Install requirements:

   .. code:: sh

        $ python -m venv env
        $ source env/bin/activate
        $ pip install -Ur requirements.txt

   You also need `enchant <https://github.com/AbiWord/enchant>`_,
   `pyenchant <https://github.com/rfk/pyenchant/>`_ and a pt-br dictionary
   (e.g. `hunspell-pt-br <https://hunspell.github.io/>`_) for spell checker.

   .. code:: sh

      # On macOS
      $ brew update && brew install enchant
      # On Debian based distros (linux Mint, Ubuntu...)
      $ sudo apt update && sudo apt install enchant python3-enchant hunspell hunspell-pt-br

2. Run the following command to generate the material in HTML:

   .. code:: sh

        $ make html

   Another option is to produce a pdf using latex:

   .. code:: sh

        $ make latexpdf

3. To see the material locally open the page ``build/html/index.html``
   in your favorite browser or the file ``build/latex/CursoIntrodutoriodePython.pdf``
   in your favorite pdf viewer.

4. To run the spell checker:

   .. code:: sh

      $ sphinx-build -b spelling -nW source/ build/

5. To run doctest:

   .. code:: sh

      $ sphinx-build -b doctest -n source/ build/

How to generate instructor's guide
----------------------------------

To generate the HTML:

.. code:: sh

    $ SPHINXOPTS="-t instructors" make html

To generate the PDF:

.. code:: sh

    $ SPHINXOPTS="-t instructors" make latexpdf

Or both together:

.. code:: sh

    $ SPHINXOPTS="-t instructors" make latexpdf html

LaTeX dependencies
------------------

To generate the PDF, you need a modern LaTeX installation like ``texlive``. To
install the minimum packages on ArchLinux (btw):

.. code:: sh

   $ sudo pacman -Syu texlive-{bin,core,latexextra}

How to contribute
-----------------

Fork this repo, make your changes and open a Pull Request.

Don't forget to add your name to ``source/contribuidores.rst``. Please, keep the
list in alphabetical order.


LICENSE
-------

This material is licensed under `Creative Commons CC-BY-NC-SA 4.0 License
<https://creativecommons.org/licenses/by-nc-sa/4.0/>`_
