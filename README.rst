=============
Python Course
=============

.. image::  https://readthedocs.org/projects/curso-python/badge/?version=latest
   :alt: Read the Docs

This repo contains the material for the Introductory Python course created by grupy-sanca.

All the material is in pt-br.

Check the material `online here <http://curso.grupysanca.com.br/>`_.

Find us in `Facebook <https://www.facebook.com/grupysanca/>`_ and
`Telegram <https://t.me/grupysanca>`_


------------------
How to use locally
------------------

1. Install requirements:
   
   .. code:: sh

        $ pip install -Ur requirements.txt

2. Run the following command to generate the material in HTML:

   .. code:: sh

        $ make html

  Another option is to produce a pdf using latex:

   .. code:: sh

        $ make latexpdf

  You might need to rerun this command.

3. To see the material locally open the page ``build/html/index.html``
   in your favorite browser or the file ``build/latex/CursoIntrodutoriodePython.pdf``
   in your favorite pdf viewer.



-------
LICENSE
-------

This material is licensed under `Creative Commons CC-BY-NC-SA 4.0 License
<https://creativecommons.org/licenses/by-nc-sa/4.0/>`_
