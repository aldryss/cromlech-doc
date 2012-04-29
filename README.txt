Installation notes
------------------

buildout.dumprequirements won't install correctly.

The faster way to get around this is::

  $ cd /path/to/project
  $ virtualenv .
  $ pip install buildout.dumprequirements
  $ >/build/buildout.dumprequirements/README.rst
  $ >/build/buildout.dumprequirements/CONTRIBUTORS.rst
  $ pip install buildout.dumprequirements
