=============
Cromlech demo
=============

The cromlech demo is a good way to start to understand what cromlech provides.

It is quite a dense demo as it tries to show very different things that can be
done with cromlech.

It was not conceived for normal framework users,
but to developpers eagers to understand how the framework work
and how it does not close you in a silo
but tries to keeps setup and requirements simple at the same time.

Installation
============

Here is how to install CromlechDemo on a debian linux.

prerequisite
-------------

We need some basic packages::

  $ apt-get install python python-dev python-virtualenv

Getting source
--------------

Clone repo and use branch zeam.setup::

  $ git clone git://devel.dolmen-project.org/CromlechDemo.git
  $ cd CromlechDemo
  $ git checkout zeam.setup

We will do it in an isolated virtualenv_ to avoid conflicts::

  $ virtualenv --no-site-packages .
  $ . bin/activate

.. note::
   if python 3 is your default python version
   you may use ``-p /usr/bin/python2.7`` (or python2.6)

Boostrap and build::

  (CromlechDemo)$ python bootstrap.py
  (CromlechDemo)$ setup install

Running
--------

Now you can run the command that will launch the uWSGI_ server::

  $ bin/demoapp

Now point your browser to http://localhost:8080/ and there you are !




This way, please!
=================

Here is what you can see on the CromlechDemo.

First it is serve by uWSGI_ but could have been equally served by Paste_
(easier at development time).

It use a simple `Twitter Bootstrap`_ based skin.

ZODB Application
-----------------

The first page you land on is part of the ZODB_ application.

ZODB is an object database that helps building application
with complex relations between entities without worrying about persitency
too much.

There is not much to bee seen as the database is empty. But you can use
*Add to folder* to add an Author. After adding an author you may add books
using *Add to folder* on the author page. You can also edit or delete items.

The *Book list* shows you a simple JSON view,
typical from what you could except from a webservice.

Also note that each item is rendered using a so called *view*
(the central part)
where as general menu, footer and so on are provided by a *layout*.
The hello world banner is a so called *viewlet*, a fragment of view.

As you can see it's a hierarchical store.
You can see that url follows the containment as a path in a filesystem.
This is usually called a *traversing* based routing
(you find stuff traversing objects).


Traject Application (SQL Database)
----------------------------------

The upper menu permits you to go to the *traject application*
located at http://localhost:8080/traject

This application use a SQL database (here a simple sqlite_ one).
Routing (finding the object to display at a certain url)
is done using traject_.
ORM is SQLAlchemy.

Once again you are presented with an author / book database.
You can, add, edit, delete items.
See how urls now follows tables names.


Basic application
--------------------

Basic page at http://localhost:8080/basic is there to show how cromlech
plays well with wsgi only parts and does not require to enter in a particular
model. It does not even use any layout, it's raw html.

Raw skin
---------

A hidden feature is a raw view skin, a skin which as no layout, no menu,
just raw content from the skin.
This is accessible adding ``++request_type++raw`` at the begining
of your path, as in http://localhost:8080/++request_type++raw/
It works everywhere.

Note that the links does not preserve the *raw* marker
as this part of url would normally be hidden to user
and added by the HTTP Server on, say, a raw.mysite.com address.


Diving into the code
====================

.. todo::
    Write this


.. _virtualenv: http://pypi.python.org/pypi/virtualenv
.. _uWSGI: http://projects.unbit.it/uwsgi/
.. _Paster: http://pythonpaste.org/script/#paster-serve
.. _`Twitter Bootstrap`: http://twitter.github.com/bootstrap/
.. _ZODB : http://www.zodb.org/
.. _sqlite : http://sqlite.org/
.. _traject : http://pypi.python.org/pypi/traject/
.. _SQLAlchemy : http://www.sqlalchemy.org/
