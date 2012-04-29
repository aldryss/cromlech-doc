==============
About Cromlech
==============

Cromlech is the namecode of a toolkit based on the ZCA, Martian and a
tiny subset of Grok's grokcore packages.

The project and motivation was born from an extensive experience with
Zope and Grok, in the domain of custom WEB application development.

The focus was : a very small and clean dependencies list, a traceable
and understandable publication process, the use of well defined and
precise structure that don't overdo their part. Long story short : the
full control of the stack. The base philosophy is : spend your time
coding, not trying to understand and parameter. If it's not there, do
it yourself.


What is Cromlech ?
------------------

Cromlech is divided in small packages that are dedicated to defining
components. To the Cromlech Team, Zope has shown the limit of the
Component Architecture provoked by the shipping and deep
intertwinement of the definition and the implementation. In order to
deliver a truly pluggable and clean system, the Cromlech Team took the
decision to strictly separate the implementation and the definition.

This is the reason to be of the 2 main Cromlech packages.

cromlech.io
~~~~~~~~~~~

cromlech.io defines the primitive and utmost basic entities of an
application : the request, the response and the actors linked to it,
namedly the publication and the application itself.


cromlech.browser
~~~~~~~~~~~~~~~~

cromlech.browser is the backbone of a webapplication. It defines an
extensive set of publisheable actors, from the forms and views to the
sub-components, known in Zope/Grok as viewlets, viewletmanagers.

This package is more or less similar in the idea to `zope.browser`,
that tried and failed in separating the component definition of the
actual implementation. It failed by the lack of responsivity of the
community and the already monolithic nature of most zope packages.


Does Cromlech do something else ?
---------------------------------

Actually, yes, it does. The previous statement was not completly true
: we do ship some implementations, but not along with the definition.
Some Cromlech packages do provide framework-level components and
others, merely utilities or 'fundamental' middlewares.

Unessential definitions
~~~~~~~~~~~~~~~~~~~~~~~

- cromlech.container

implementations
~~~~~~~~~~~~~~~

- cromlech.dawnlight

- cromlech.zodb

- cromlech.webob

middlewares
~~~~~~~~~~~

- cromlech.security

- cromlech.beaker

utilities
~~~~~~~~~

- cromlech.configuration

- cromlech.wsgi


Dolmen and the application-level components
-------------------------------------------

dolmen.layout
~~~~~~~~~~~~~

x

dolmen.view
~~~~~~~~~~~

x

dolmen.viewlet
~~~~~~~~~~~~~~

x

dolmen.message
~~~~~~~~~~~~~~

x

dolmen.content
~~~~~~~~~~~~~~

x

dolmen.menu
~~~~~~~~~~~

x
