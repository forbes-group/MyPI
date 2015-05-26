Michael McNeil Forbes's Package Index
=====================================

This is a simple list of packages I maintain, usually in source code, for
Python projects.  You can install any version here by adding the index file to
pip with the ``--find-links`` (``-f``) flag or by setting the
``PIP_FIND_LINKS`` environment variable::

   pip install -f https://bitbucket.org/mforbes/mypi/index.html ...

or::

   export PIP_FIND_LINKS=https://bitbucket.org/mforbes/mypi/index.html
   pip install ...

Development Notes
+++++++++++++++++

This uses the Downloads features of bitbucket, i.e.

* https://bitbucket.org/mforbes/mypi/get/0.1.tar.bz2

At some point it might be nice to automatic the generation of this with
something similar to the `basketweaver
<https://pypi.python.org/pypi/basketweaver/>`_ project.  The idea is to link
all distributions I want to manage into a common place, then inspect the
repos to get the tags and branches that form valid revisions.
