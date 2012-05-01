Installation notes
------------------

You can use the buildout.cfg for a normal install.

If you are to push to read-the-docs
you have to have an up-to-date *requirements.txt* for pip.
In this case you must use *buildout-requirements.cfg*.

However note that buildout.dumprequirements won't install correctly.

The faster way to get around this is::

  $ cd /path/to/project
  $ virtualenv .
  $ pip install buildout.dumprequirements
  $ >/build/buildout.dumprequirements/README.rst
  $ >/build/buildout.dumprequirements/CONTRIBUTORS.rst
  $ pip install buildout.dumprequirements

And finally::

  $ bin/buildout -c buildout-requirements.cfg
