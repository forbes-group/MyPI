Michael McNeil Forbes's Package Index
=====================================

This is a simple list of packages I maintain, usually in source code, for
Python projects.  You can install any version here by adding the index file to
pip with the ``--extra-index-url`` flag or by setting the
``PIP_EXTRA_INDEX_URL`` environment variable.  Unfortunately, as far as `I can
see <https://groups.google.com/forum/#!topic/python-virtualenv/JO135HL9S7s>`_,
the index directory needs to be hosted by a true web server so that
directories ending in slashes will serve the appropriate `index files
<http://peak.telecommunity.com/DevCenter/EasyInstall#package-index-api>`_,
thus I must also host these in a separate place::

   pip install --extra-index-url=https://mforbes.bitbucket.org/mypi/index/

or::

   export PIP_EXTRA_INDEX_URL=https://mforbes.bitbucket.org/mypi/index/

I hope at some point to figure out how to simply host these here:

   export PIP_EXTRA_INDEX_URL=https://bitbucket.org/mforbes/mypi/raw/tip/index.html

Development Notes
+++++++++++++++++

I use this by including it as a subrepo of my `mforbes.bitbucket.org
<https://mforbes.bitbucket.org/mforbes.bitbucket.org>` project using the
techniques of `subrepos done right
<http://blog.rusty.io/2010/01/24/submodules-and-subrepos-done-right/>`_.  I
also include an ignored directory ``dist`` which I symlink to the ``dist``
directory in all of the repos I want to host here.

When I want to include a revision, I run::

   python setup.py sdist

in the appropriate project, which will add the tarball to the ``dist``
directory.  Then I run ``makeindex dist`` from the `basketweaver
<https://pypi.python.org/pypi/basketweaver/>`_ project to get a skelton, and
replace all of the entries with appropriate links as shown in the index files.

.. note:: The basketweaver scripts could be easily updated to do this
   automatically, but I do not have the need just yet.  Patches welcome:-)
