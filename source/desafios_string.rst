#. Por que o seguinte código retorna uma *string* vazia?

   .. doctest::

      >>> texto = "No alto da montanha havia uma rosa"
      >>> texto[0:-1:-1]
      ''

   .. note::

      .. doctest::

         >>> texto = "No alto da montanha havia uma rosa"
         >>> texto[0:-1]
         'No alto da montanha havia uma ros