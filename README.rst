Michael McNeil Forbes's Package Index
=====================================

This is a simple list of packages I maintain, usually in source code, for
Python projects.  You can install any version here by adding the index file to
pip with the ``--find-links`` (``-f``) flag or by setting the
``PIP_FIND_LINKS`` environment variable::

   pip install -f https://bitbucket.org/mforbes/mypi/ ...

or::

   export PIP_FIND_LINKS=https://bitbucket.org/mforbes/mypi/
   pip install ...

or add the following to your ``requirements.txt`` file::

   --find-links https://bitbucket.org/mforbes/mypi/

If you need a specific version, you can access the file as follows,
replacing ``tip`` with the appropriate version number::

   --find-links https://bitbucket.org/mforbes/mypi/src/tip/README.rst


Package Index
+++++++++++++

Here is the package index:

mmfutils Distributions
----------------------
 * `mmfutils-0.4.1 <https://bitbucket.org/mforbes/mmfutils/get/0.4.1.tar.bz2#egg=mmfutils-0.4.1>`_
 * `mmfutils-0.4.2 <https://bitbucket.org/mforbes/mmfutils/get/0.4.2.tar.bz2#egg=mmfutils-0.4.2>`_
 * `mmfutils-0.4.3 <https://bitbucket.org/mforbes/mmfutils/get/0.4.3.tar.bz2#egg=mmfutils-0.4.3>`_
 * `mmfutils-0.4.4 <https://bitbucket.org/mforbes/mmfutils/get/0.4.4.tar.bz2#egg=mmfutils-0.4.4>`_
 * `mmfutils-0.4.5 <https://bitbucket.org/mforbes/mmfutils/get/0.4.5.tar.bz2#egg=mmfutils-0.4.5>`_
 * `mmfutils-0.4.6 <https://bitbucket.org/mforbes/mmfutils/get/0.4.6.tar.bz2#egg=mmfutils-0.4.6>`_
 * `mmfutils-0.4 <https://bitbucket.org/mforbes/mmfutils/get/0.4.tar.bz2#egg=mmfutils-0.4>`_
 * `mmfutils-0.4.7dev <hg+https://bitbucket.org/mforbes/mmfutils-fork@0.4.7#egg=mmfutils-0.4.7dev>`_


persist Distributions
---------------------
 * `persist-0.9 <https://bitbucket.org/mforbes/persist/get/0.9.tar.bz2#egg=persist-0.9>`_
 * `persist-0.9b2 <https://bitbucket.org/mforbes/persist/get/0.9b2.tar.bz2#egg=persist-0.9b2>`_


pytimeode Distributions
-----------------------
Note: These are private.  You must have read permission to use them and ssh
access.

 * `pytimeode-0.2 <hg+ssh://hg@bitbucket.org/mforbes/pytimeode@0.2#egg=pytimeode-0.2>`_
 * `pytimeode-0.3 <hg+ssh://hg@bitbucket.org/mforbes/pytimeode@0.3#egg=pytimeode-0.3>`_
 * `pytimeode-0.4 <hg+ssh://hg@bitbucket.org/mforbes/pytimeode@0.4#egg=pytimeode-0.4>`_
 * `pytimeode-0.5 <hg+ssh://hg@bitbucket.org/mforbes/pytimeode@0.5#egg=pytimeode-0.5>`_
 * `pytimeode-0.6 <hg+ssh://hg@bitbucket.org/mforbes/pytimeode@0.6#egg=pytimeode-0.6>`_
 * `pytimeode-0.7 <hg+ssh://hg@bitbucket.org/mforbes/pytimeode@0.7#egg=pytimeode-0.7>`_

 * `pytimeode-0.8dev <hg+ssh://hg@bitbucket.org/mforbes/pytimeode@0.8#egg=pytimeode-0.8dev>`_
   
Not Mine
--------
Here are some packages that are not mine,:

* `ipy_client_usage-0.3dev <git+https://github.com/mforbes/ipy_client_usage.git#egg=ipy_client_usage-0.3dev>`_

* `pygsl-0.9.5 <http://downloads.sourceforge.net/project/pygsl/pygsl/pygsl-0.9.5/pygsl-0.9.5.tar.gz#egg=pygsl-0.9.5>`_

The following patch is required for use with IPython 3.0 and above:

* https://github.com/catherinedevlin/ipython_doctester/issues/6
* https://github.com/catherinedevlin/ipython_doctester/pull/5
* `ipython_doctester <git+https://github.com/jhamrick/ipython_doctester.git@update-display-data#egg=ipython_doctester>`_

The following fixes
[pytest-flake8](https://github.com/tholo/pytest-flake8) so that it
reads the configuration file:

* `pytest-flake8-0.1a <git+https://github.com/mdevlamynck/pytest-flake8.git#egg=pytest-flake8-0.1a>`_

Here is a package to strip output from a notebook:

* `nbstripout-0.1 <git+https://github.com/kynan/nbstripout.git#egg=nbstripout-0.1>`_
* `nbstripout-0.2.0 <git+https://github.com/mforbes/nbstripout.git@0.2.0#egg=nbstripout-0.2.0>`_

Development Notes
+++++++++++++++++

This uses the Downloads features of bitbucket, i.e.

* https://bitbucket.org/mforbes/mypi/get/0.1.tar.bz2

At some point it might be nice to automatic the generation of this with
something similar to the `basketweaver
<https://pypi.python.org/pypi/basketweaver/>`_ project.  The idea is to link
all distributions I want to manage into a common place, then inspect the
repos to get the tags and branches that form valid revisions.

One issue `discussed here
<https://groups.google.com/forum/#!topic/python-virtualenv/JO135HL9S7s>`_ is
that ``pip`` requires the content delivered over the web with Content-Type
``'text/html'`` whereas I would like to use the file

* https://bitbucket.org/mforbes/mypi/raw/tip/index.html

which is delivered as Content-Type ``'text/plain'``.  The use of the rendered
``README.rst`` (this file) is a functional workaround, but seems a bit
dangerous since it appears on a page with a bunch of other links from bitbucket
that might confuse ``pip``.
