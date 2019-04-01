Python Course
=============

.. image::  https://readthedocs.org/projects/curso-python/badge/?version=latest
   :alt: Read the Docs

This repo contains the material for the Introductory Python course created by grupy-sanca.

All the material is in pt-br.

Check the material `online here <http://curso.grupysanca.com.br/>`_.

Find us in `Facebook <https://www.facebook.com/grupysanca/>`_,
`Telegram <https://t.me/grupysanca>`_,
`Instagram <https://www.instagram.com/grupysanca/>`_,
`Meetup <https://www.meetup.com/grupy-sanca>`_ and
`YouTube <https://www.youtube.com/channel/UC9AED1x6Nn10lu-3rNELQnw>`_


How to use locally
------------------

1. Install requirements:

   .. code:: sh

        $ pip install -Ur requirements.txt

   You also need `enchant <https://github.com/AbiWord/enchant>`_,
   `pyenchant <https://github.com/rfk/pyenchant/>`_ and a pt-br dictionary
   (e.g. `hunspell-pt-br <https://hunspell.github.io/>`_) for spell checker.


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

How to generate instructor's guide
----------------------------------

.. code:: sh

    $ SPHINXOPTS="-t instructors" make html


How to contribute
-----------------

Fork this repo, make your changes and open a Pull Request.

Don't forget to add your name to ``source/contribuidores.rst``. Please, keep the
list in alphabetical order.


LICENSE
-------

This material is licensed under `Creative Commons CC-BY-NC-SA 4.0 License
<https://creativecommons.org/licenses/by-nc-sa/4.0/>`_
