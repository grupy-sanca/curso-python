Variáveis
=========

Variável é um *nome* que se refere a um *valor*.


Atribuição
----------

Atribuição é o processo de criar uma nova variável e dar um novo valor a
ela.
Alguns exemplos de atribuições:

.. doctest::

   >>> numero = 11
   >>> numero
   11

.. doctest::

   >>> frase = "Me dá um copo d'água"
   >>> frase
   "Me dá um copo d'água"

.. doctest::

   >>> pi = 3.141592
   >>> pi
   3.141592

No exemplo anterior realizamos três atribuições. No primeiro atribuímos um
número inteiro à variável de nome ``numero``; no segundo uma frase à
variável ``frase``; no último um número de ponto flutuante à ``pi``.

.. _section_nomes_variaveis:

Nomes de Variáveis
------------------

Bons programadores escolhem nomes significativos para as suas variáveis
- eles documentam o propósito da variável.

Nomes de variáveis podem ter o tamanho que você achar necessário e podem
conter tanto letras como números, porém não podem começar com números. É
possível usar letras maiúsculas, porém a convenção é utilizar somente
letras minúsculas para nomes de variáveis.

.. doctest::

   >>> crieiumavariavelcomnomegiganteeestoucompreguiçadeescrevertudodenovo = 10
   >>> crieiumavariavelcomnomegiganteeestoucompreguiçadeescrevertudodenovo # use TAB para autocompletar =D
   10

Tentar dar um nome ilegal a uma variável ocasionará erro de sintaxe:

.. doctest::

   >>> 123voa = 10
   Traceback (most recent call last):
       ...
           123voa = 10
                ^
   SyntaxError: invalid syntax

.. code-block:: python3

   >>> ol@ = "oi"
   Traceback (most recent call last):
       ...
           ol@ = "oi"
               ^
   SyntaxError: invalid syntax

.. code-block:: bash

   >>> def = 2.7
   Traceback (most recent call last):
       ...
           def = 2.7
               ^
   SyntaxError: invalid syntax


``123voa`` é ilegal pois começa com um número. ``ol@`` é ilegal pois
contém um caractere inválido (@), mas o que há de errado com ``def``?

A questão é que ``def`` é uma palavra-chave da linguagem. O Python possui
diversas palavras que são utilizadas na estrutura dos programas, por isso
não podem ser utilizadas como nomes de variáveis.

Outro ponto importante: não é possível acessar variáveis que
ainda não foram definidas:

.. doctest::

   >>> nao_definida
   Traceback (most recent call last):
       ...
   NameError: name 'nao_definida' is not defined

.. spelling::

   definí

Tentar acessar uma variável sem definí-la anteriormente ocasiona em um "erro
de nome".

Também podemos atribuir expressões a uma variável:

.. doctest::

   >>> x = 3 * 5 - 2
   >>> x
   13
   >>> y = 3 * x + 10
   >>> y
   49
   >>> z = x + y
   >>> z
   62

.. doctest::

   >>> n = 10
   >>> n + 2 # 10 + 2
   12
   >>> 9 - n # 9 - 10
   -1

É importante lembrar que para mudar o valor de uma variável é preciso
utilizar a atribuição. Nos dois exemplos anteriores não atribuímos as
expressões à n, portanto seu valor continuou o mesmo.

Vamos alterar o valor de ``n``:

.. doctest::

   >>> n
   10
   >>> n = n + 2
   >>> n
   12
   >>> 9 - n
   -3

Outra forma de somar na variável:

.. doctest::

   >>> num = 4
   >>> num += 3
   >>> num
   7

Também funciona com multiplicação:

.. doctest::

   >>> x = 2
   >>> x *= 3
   >>> x
   6


Atribuição múltipla
-------------------

Uma funcionalidade interessante do Python é que ele permite atribuição
múltipla. Isso é muito útil para trocar o valor de duas variáveis:

.. doctest::

   >>> a = 1
   >>> b = 200

Para fazer essa troca em outras linguagens é necessário utilizar uma
variável auxiliar para não perdemos um dos valores que queremos trocar.
Vamos começar da maneira mais simples:

.. doctest::

   >>> a = b  # perdemos o valor de a
   >>> a
   200

.. doctest::

   >>> b = a  # como perdemos o valor de a, b vai continuar com seu valor original de 200
   >>> b
   200

A troca é bem sucedida se usamos uma variável auxiliar:

.. doctest::

   >>> a = 1
   >>> b = 200
   >>> print(a, b)
   1 200

   >>> aux = a
   >>> a = b
   >>> b = aux
   >>> print(a, b)
   200 1

Porém, como o Python permite atribuição múltipla, podemos resolver esse
problema de uma forma muito mais simples:

.. doctest::

   >>> a = 1
   >>> b = 200
   >>> print(a, b)
   1 200

.. doctest::

   >>> a, b = b, a
   >>> print(a, b)
   200 1

A atribuição múltipla também pode ser utilizada para simplificar a
atribuição de variáveis, por exemplo:

.. doctest::

   >>> a, b = 1, 200
   >>> print(a, b)
   1 200

.. doctest::

   >>> a, b, c, d = 1, 2, 3, 4
   >>> print(a, b, c, d)
   1 2 3 4

.. doctest::

   >>> a, b, c, d = d, c, b, a
   >>> print(a, b, c, d)
   4 3 2 1


Tipos de objetos
----------------

Criamos muitas variáveis até agora. Você lembra o tipo de cada uma? Para
saber o tipo de um objeto ou variável, usamos a função ``type()``:

.. doctest::

   >>> x = 1
   >>> type(x)
   <class 'int'>
   >>> y = 2.3
   >>> type(y)
   <class 'float'>
   >>> type('Python')
   <class 'str'>
   >>> type(True)
   <class 'bool'>

Python vem com alguns tipos básicos de objetos, dentre eles:

* ``bool``: verdadeiro ou falso.
* ``int``: números inteiros.
* ``float``: números reais.
* ``complex``: números complexos.
* ``str``: *strings* (textos).
* ``list``: :ref:`listas <section_listas>`. Estudaremos em breve o que são.
* ``dict``: :ref:`dicionários <section_dicionario>`. Estudaremos em breve o que são.


Buscando ajuda rapidamente
--------------------------

Está com dúvida em alguma coisa? Use a função ``help()`` e depois digite o
que você busca.

.. code-block:: python3

   >>> help()

   Welcome to Python 3.6's help utility!

   If this is your first time using Python, you should definitely check out
   the tutorial on the Internet at http://docs.python.org/3.6/tutorial/.

   Enter the name of any module, keyword, or topic to get help on writing
   Python programs and using Python modules.  To quit this help utility and
   return to the interpreter, just type "quit".

   To get a list of available modules, keywords, symbols, or topics, type
   "modules", "keywords", "symbols", or "topics".  Each module also comes
   with a one-line summary of what it does; to list the modules whose name
   or summary contain a given string such as "spam", type "modules spam".

   help>
   You are now leaving help and returning to the Python interpreter.
   If you want to ask for help on a particular object directly from the
   interpreter, you can type "help(object)".  Executing "help('string')"
   has the same effect as typing a particular string at the help> prompt.

E para buscar ajuda em uma coisa específica?

.. doctest::

   >>> help(len)
   Help on built-in function len in module builtins:
   <BLANKLINE>
   len(obj, /)
       Return the number of items in a container.
   <BLANKLINE>

Para sair do ambiente de ajuda, pressione a tecla ``q``.

.. only:: html

   .. code-block:: python3

      >>> help(str)
      Help on class str in module builtins:

      class str(object)
       |  str(object='') -> str
       |  str(bytes_or_buffer[, encoding[, errors]]) -> str
       |
       |  Create a new string object from the given object. If encoding or
       |  errors is specified, then the object must expose a data buffer
       |  that will be decoded using the given encoding and error handler.
       |  Otherwise, returns the result of object.__str__() (if defined)
       |  or repr(object).
       |  encoding defaults to sys.getdefaultencoding().
       |  errors defaults to 'strict'.
       |
       |  Methods defined here:
       |
       |  __add__(self, value, /)
       |      Return self+value.
       |
       |  __contains__(self, key, /)
       |      Return key in self.
       |
       |  __eq__(self, value, /)
       |      Return self==value.
       |
       |  __format__(...)
       |      S.__format__(format_spec) -> str
       |
       |      Return a formatted version of S as described by format_spec.
       |
       |  __ge__(self, value, /)
       |      Return self>=value.
       |
       |  __getattribute__(self, name, /)
       |      Return getattr(self, name).
       |
       |  __getitem__(self, key, /)
       |      Return self[key].
       |
       |  __getnewargs__(...)
       |
       |  __gt__(self, value, /)
       |      Return self>value.
       |
       |  __hash__(self, /)
       |      Return hash(self).
       |
       |  __iter__(self, /)
       |      Implement iter(self).
       |
       |  __le__(self, value, /)
       |      Return self<=value.
       |
       |  __len__(self, /)
       |      Return len(self).
       |
       |  __lt__(self, value, /)
       |      Return self<value.
       |
       |  __mod__(self, value, /)
       |      Return self%value.
       |
       |  __mul__(self, value, /)
       |      Return self*value.n
       |
       |  __ne__(self, value, /)
       |      Return self!=value.
       |
       |  __new__(*args, **kwargs) from builtins.type
       |      Create and return a new object.  See help(type) for accurate signature.
       |
       |  __repr__(self, /)
       |      Return repr(self).
       |
       |  __rmod__(self, value, /)
       |      Return value%self.
       |
       |  __rmul__(self, value, /)
       |      Return self*value.
       |
       |  __sizeof__(...)
       |      S.__sizeof__() -> size of S in memory, in bytes
       |
       |  __str__(self, /)
       |      Return str(self).
       |
       |  capitalize(...)
       |      S.capitalize() -> str
       |
       |      Return a capitalized version of S, i.e. make the first character
       |      have upper case and the rest lower case.
       |
       |  casefold(...)
       |      S.casefold() -> str
       |
       |      Return a version of S suitable for caseless comparisons.
       |
       |  center(...)
       |      S.center(width[, fillchar]) -> str
       |
       |      Return S centered in a string of length width. Padding is
       |      done using the specified fill character (default is a space)
       |
       |  count(...)
       |      S.count(sub[, start[, end]]) -> int
       |
       |      Return the number of non-overlapping occurrences of substring sub in
       |      string S[start:end].  Optional arguments start and end are
       |      interpreted as in slice notation.
       |
       |  encode(...)
       |      S.encode(encoding='utf-8', errors='strict') -> bytes
       |
       |      Encode S using the codec registered for encoding. Default encoding
       |      is 'utf-8'. errors may be given to set a different error
       |      handling scheme. Default is 'strict' meaning that encoding errors raise
       |      a UnicodeEncodeError. Other possible values are 'ignore', 'replace' and
       |      'xmlcharrefreplace' as well as any other name registered with
       |      codecs.register_error that can handle UnicodeEncodeErrors.
       |
       |  endswith(...)
       |      S.endswith(suffix[, start[, end]]) -> bool
       |
       |      Return True if S ends with the specified suffix, False otherwise.
       |      With optional start, test S beginning at that position.
       |      With optional end, stop comparing S at that position.
       |      suffix can also be a tuple of strings to try.
       |
       |  expandtabs(...)
       |      S.expandtabs(tabsize=8) -> str
       |
       |      Return a copy of S where all tab characters are expanded using spaces.
       |      If tabsize is not given, a tab size of 8 characters is assumed.
       |
       |  find(...)
       |      S.find(sub[, start[, end]]) -> int
       |
       |      Return the lowest index in S where substring sub is found,
       |      such that sub is contained within S[start:end].  Optional
       |      arguments start and end are interpreted as in slice notation.
       |
       |      Return -1 on failure.
       |
       |  format(...)
       |      S.format(*args, **kwargs) -> str
       |
       |      Return a formatted version of S, using substitutions from args and kwargs.
       |      The substitutions are identified by braces ('{' and '}').
       |
       |  format_map(...)
       |      S.format_map(mapping) -> str
       |
       |      Return a formatted version of S, using substitutions from mapping.
       |      The substitutions are identified by braces ('{' and '}').
       |
       |  index(...)
       |      S.index(sub[, start[, end]]) -> int
       |
       |      Like S.find() but raise ValueError when the substring is not found.
       |
       |  isalnum(...)
       |      S.isalnum() -> bool
       |
       |      Return True if all characters in S are alphanumeric
       |      and there is at least one character in S, False otherwise.
       |
       |  isalpha(...)
       |      S.isalpha() -> bool
       |
       |      Return True if all characters in S are alphabetic
       |      and there is at least one character in S, False otherwise.
       |
       |  isdecimal(...)
       |      S.isdecimal() -> bool
       |
       |      Return True if there are only decimal characters in S,
       |      False otherwise.
       |
       |  isdigit(...)
       |      S.isdigit() -> bool
       |
       |      Return True if all characters in S are digits
       |      and there is at least one character in S, False otherwise.
       |
       |  isidentifier(...)
       |      S.isidentifier() -> bool
       |
       |      Return True if S is a valid identifier according
       |      to the language definition.
       |
       |      Use keyword.iskeyword() to test for reserved identifiers
       |      such as "def" and "class".
       |
       |  islower(...)
       |      S.islower() -> bool
       |
       |      Return True if all cased characters in S are lowercase and there is
       |      at least one cased character in S, False otherwise.
       |
       |  isnumeric(...)
       |      S.isnumeric() -> bool
       |
       |      Return True if there are only numeric characters in S,
       |      False otherwise.
       |
       |  isprintable(...)
       |      S.isprintable() -> bool
       |
       |      Return True if all characters in S are considered
       |      printable in repr() or S is empty, False otherwise.
       |
       |  isspace(...)
       |      S.isspace() -> bool
       |
       |      Return True if all characters in S are whitespace
       |      and there is at least one character in S, False otherwise.
       |
       |  istitle(...)
       |      S.istitle() -> bool
       |
       |      Return True if S is a titlecased string and there is at least one
       |      character in S, i.e. upper- and titlecase characters may only
       |      follow uncased characters and lowercase characters only cased ones.
       |      Return False otherwise.
       |
       |  isupper(...)
       |      S.isupper() -> bool
       |
       |      Return True if all cased characters in S are uppercase and there is
       |      at least one cased character in S, False otherwise.
       |
       |  join(...)
       |      S.join(iterable) -> str
       |
       |      Return a string which is the concatenation of the strings in the
       |      iterable.  The separator between elements is S.
       |
       |  ljust(...)
       |      S.ljust(width[, fillchar]) -> str
       |
       |      Return S left-justified in a Unicode string of length width. Padding is
       |      done using the specified fill character (default is a space).
       |
       |  lower(...)
       |      S.lower() -> str
       |
       |      Return a copy of the string S converted to lowercase.
       |
       |  lstrip(...)
       |      S.lstrip([chars]) -> str
       |
       |      Return a copy of the string S with leading whitespace removed.
       |      If chars is given and not None, remove characters in chars instead.
       |
       |  partition(...)
       |      S.partition(sep) -> (head, sep, tail)
       |
       |      Search for the separator sep in S, and return the part before it,
       |      the separator itself, and the part after it.  If the separator is not
       |      found, return S and two empty strings.
       |
       |  replace(...)
       |      S.replace(old, new[, count]) -> str
       |
       |      Return a copy of S with all occurrences of substring
       |      old replaced by new.  If the optional argument count is
       |      given, only the first count occurrences are replaced.
       |
       |  rfind(...)
       |      S.rfind(sub[, start[, end]]) -> int
       |
       |      Return the highest index in S where substring sub is found,
       |      such that sub is contained within S[start:end].  Optional
       |      arguments start and end are interpreted as in slice notation.
       |
       |      Return -1 on failure.
       |
       |  rindex(...)
       |      S.rindex(sub[, start[, end]]) -> int
       |
       |      Like S.rfind() but raise ValueError when the substring is not found.
       |
       |  rjust(...)
       |      S.rjust(width[, fillchar]) -> str
       |
       |      Return S right-justified in a string of length width. Padding is
       |      done using the specified fill character (default is a space).
       |
       |  rpartition(...)
       |      S.rpartition(sep) -> (head, sep, tail)
       |
       |      Search for the separator sep in S, starting at the end of S, and return
       |      the part before it, the separator itself, and the part after it.  If the
       |      separator is not found, return two empty strings and S.
       |
       |  rsplit(...)
       |      S.rsplit(sep=None, maxsplit=-1) -> list of strings
       |
       |      Return a list of the words in S, using sep as the
       |      delimiter string, starting at the end of the string and
       |      working to the front.  If maxsplit is given, at most maxsplit
       |      splits are done. If sep is not specified, any whitespace string
       |      is a separator.
       |
       |  rstrip(...)
       |      S.rstrip([chars]) -> str
       |
       |      Return a copy of the string S with trailing whitespace removed.
       |      If chars is given and not None, remove characters in chars instead.
       |
       |  split(...)
       |      S.split(sep=None, maxsplit=-1) -> list of strings
       |
       |      Return a list of the words in S, using sep as the
       |      delimiter string.  If maxsplit is given, at most maxsplit
       |      splits are done. If sep is not specified or is None, any
       |      whitespace string is a separator and empty strings are
       |      removed from the result.
       |
       |  splitlines(...)
       |      S.splitlines([keepends]) -> list of strings
       |
       |      Return a list of the lines in S, breaking at line boundaries.
       |      Line breaks are not included in the resulting list unless keepends
       |      is given and true.
       |
       |  startswith(...)
       |      S.startswith(prefix[, start[, end]]) -> bool
       |
       |      Return True if S starts with the specified prefix, False otherwise.
       |      With optional start, test S beginning at that position.
       |      With optional end, stop comparing S at that position.
       |      prefix can also be a tuple of strings to try.
       |
       |  strip(...)
       |      S.strip([chars]) -> str
       |
       |      Return a copy of the string S with leading and trailing
       |      whitespace removed.
       |      If chars is given and not None, remove characters in chars instead.
       |
       |  swapcase(...)
       |      S.swapcase() -> str
       |
       |      Return a copy of S with uppercase characters converted to lowercase
       |      and vice versa.
       |
       |  title(...)
       |      S.title() -> str
       |
       |      Return a titlecased version of S, i.e. words start with title case
       |      characters, all remaining cased characters have lower case.
       |
       |  translate(...)
       |      S.translate(table) -> str
       |
       |      Return a copy of the string S in which each character has been mapped
       |      through the given translation table. The table must implement
       |      lookup/indexing via __getitem__, for instance a dictionary or list,
       |      mapping Unicode ordinals to Unicode ordinals, strings, or None. If
       |      this operation raises LookupError, the character is left untouched.
       |      Characters mapped to None are deleted.
       |
       |  upper(...)
       |      S.upper() -> str
       |
       |      Return a copy of S converted to uppercase.
       |
       |  zfill(...)
       |      S.zfill(width) -> str
       |
       |      Pad a numeric string S with zeros on the left, to fill a field
       |      of the specified width. The string S is never truncated.
       |
       |  ----------------------------------------------------------------------
       |  Static methods defined here:
       |
       |  maketrans(x, y=None, z=None, /)
       |      Return a translation table usable for str.translate().
       |
       |      If there is only one argument, it must be a dictionary mapping Unicode
       |      ordinals (integers) or characters to Unicode ordinals, strings or None.
       |      Character keys will be then converted to ordinals.
       |      If there are two arguments, they must be strings of equal length, and
       |      in the resulting dictionary, each character in x will be mapped to the
       |      character at the same position in y. If there is a third argument, it
       |      must be a string, whose characters will be mapped to None in the result.

A `documentação oficial <https://docs.python.org/3/>`_ do Python contém toda a
referência sobre a linguagem, detalhes sobre cada função e alguns exemplos (em inglês).


Listando variáveis criadas
--------------------------

Em algum momento durante o seu código você pode querer saber quais variáveis já 
foram declaradas, ou até mesmo o valor atual delas. Podemos listar todas as 
variáveis declaradas no código usando o comando ``dir()``. Veja um exemplo:

.. doctest::

   >>> a = 1
   >>> b = 2
   >>> dir()
   ['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__', '__package__', '__spec__', 'a', 'b']

Veja que nossas variáveis declaradas aparecem no final do resultado de ``dir()``.
Não se assuste com os outros elementos que aparecem nesse resultado. Essas 
variáveis são criadas e usadas pelo próprio Python, e não são importantes 
nesse momento.

Outra opção para visualizar as variáveis declaradas são os comandos ``globals()`` 
e ``locals()``. Ambas mostram não só as variáveis declaradas, mas também seu 
valor atual. A diferença entre ambas está no escopo em que atuam, mas veja que 
seus resultados são semelhantes:

.. doctest::

   >>> a = 1
   >>> b = 2
   >>> locals()
   {'__name__': '__main__', '__doc__': None, '__package__': None, '__loader__': <class '_frozen_importlib.BuiltinImporter'>, '__spec__': None, '__annotations__': {}, '__builtins__': <module 'builtins' (built-in)>, 'a': 1, 'b': 2}
   >>> globals()
   {'__name__': '__main__', '__doc__': None, '__package__': None, '__loader__': <class '_frozen_importlib.BuiltinImporter'>, '__spec__': None, '__annotations__': {}, '__builtins__': <module 'builtins' (built-in)>, 'a': 1, 'b': 2}

Caso você esteja usando o IPython, os comandos mágicos ``%who`` e ``%whos`` são
ótimas alternativas ao que já vimos anteriormente, pois retiram do resultado as 
variáveis declaradas pelo próprio Python, permitindo uma melhor visualização das 
que você mesmo declarou. Olhe como o IPython pode simplificar nossa vida nesse 
caso:

.. doctest::

   >>> a = 1
   >>> %who
   a
   >>> %whos
   Variable   Type    Data/Info
   ----------------------------
   a          int     1

Exercícios
----------

.. include:: exercicios_variaveis.rst
