About python-feedstock
======================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/python-feedstock/blob/main/LICENSE.txt)

Home: https://www.python.org/

Package license: Python-2.0

Summary: General purpose programming language

Development: https://docs.python.org/devguide/

Documentation: https://www.python.org/doc/versions/

Python is a widely used high-level, general-purpose, interpreted, dynamic
programming language. Its design philosophy emphasizes code
readability, and its syntax allows programmers to express concepts in
fewer lines of code than would be possible in languages such as C++ or
Java. The language provides constructs intended to enable clear programs
on both a small and large scale.

We provide some meta packages for convenience.
To get a CPython flavour, use:

    conda install cpython

To get the freethreading build (i.e. without the Global Interpreter Lock - GIL):

    conda install python-freethreading

To get the default build (i.e. with the GIL):

    conda install python-gil

To enable the use of the experimental JIT compiler in CPython:

    conda install python-jit

or set the environment variable PYTHON_JIT=1. Note that the JIT support
is available for x86_64 builds only.


Current build status
====================


<table>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-cpython-green.svg)](https://anaconda.org/jaimergp/cpython) | [![Conda Downloads](https://img.shields.io/conda/dn/jaimergp/cpython.svg)](https://anaconda.org/jaimergp/cpython) | [![Conda Version](https://img.shields.io/conda/vn/jaimergp/cpython.svg)](https://anaconda.org/jaimergp/cpython) | [![Conda Platforms](https://img.shields.io/conda/pn/jaimergp/cpython.svg)](https://anaconda.org/jaimergp/cpython) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-libpython--static-green.svg)](https://anaconda.org/jaimergp/libpython-static) | [![Conda Downloads](https://img.shields.io/conda/dn/jaimergp/libpython-static.svg)](https://anaconda.org/jaimergp/libpython-static) | [![Conda Version](https://img.shields.io/conda/vn/jaimergp/libpython-static.svg)](https://anaconda.org/jaimergp/libpython-static) | [![Conda Platforms](https://img.shields.io/conda/pn/jaimergp/libpython-static.svg)](https://anaconda.org/jaimergp/libpython-static) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-python-green.svg)](https://anaconda.org/jaimergp/python) | [![Conda Downloads](https://img.shields.io/conda/dn/jaimergp/python.svg)](https://anaconda.org/jaimergp/python) | [![Conda Version](https://img.shields.io/conda/vn/jaimergp/python.svg)](https://anaconda.org/jaimergp/python) | [![Conda Platforms](https://img.shields.io/conda/pn/jaimergp/python.svg)](https://anaconda.org/jaimergp/python) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-python--freethreading-green.svg)](https://anaconda.org/jaimergp/python-freethreading) | [![Conda Downloads](https://img.shields.io/conda/dn/jaimergp/python-freethreading.svg)](https://anaconda.org/jaimergp/python-freethreading) | [![Conda Version](https://img.shields.io/conda/vn/jaimergp/python-freethreading.svg)](https://anaconda.org/jaimergp/python-freethreading) | [![Conda Platforms](https://img.shields.io/conda/pn/jaimergp/python-freethreading.svg)](https://anaconda.org/jaimergp/python-freethreading) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-python--gil-green.svg)](https://anaconda.org/jaimergp/python-gil) | [![Conda Downloads](https://img.shields.io/conda/dn/jaimergp/python-gil.svg)](https://anaconda.org/jaimergp/python-gil) | [![Conda Version](https://img.shields.io/conda/vn/jaimergp/python-gil.svg)](https://anaconda.org/jaimergp/python-gil) | [![Conda Platforms](https://img.shields.io/conda/pn/jaimergp/python-gil.svg)](https://anaconda.org/jaimergp/python-gil) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-python--jit-green.svg)](https://anaconda.org/jaimergp/python-jit) | [![Conda Downloads](https://img.shields.io/conda/dn/jaimergp/python-jit.svg)](https://anaconda.org/jaimergp/python-jit) | [![Conda Version](https://img.shields.io/conda/vn/jaimergp/python-jit.svg)](https://anaconda.org/jaimergp/python-jit) | [![Conda Platforms](https://img.shields.io/conda/pn/jaimergp/python-jit.svg)](https://anaconda.org/jaimergp/python-jit) |

Installing python
=================

Installing `python` from the `jaimergp/label/zlib-ng-compat_debug` channel can be achieved by adding `jaimergp/label/zlib-ng-compat_debug` to your channels with:

```
conda config --add channels jaimergp/label/zlib-ng-compat_debug
conda config --set channel_priority strict
```

Once the `jaimergp/label/zlib-ng-compat_debug` channel has been enabled, `cpython, libpython-static, python, python-freethreading, python-gil, python-jit` can be installed with `conda`:

```
conda install cpython libpython-static python python-freethreading python-gil python-jit
```

or with `mamba`:

```
mamba install cpython libpython-static python python-freethreading python-gil python-jit
```

It is possible to list all of the versions of `cpython` available on your platform with `conda`:

```
conda search cpython --channel jaimergp/label/zlib-ng-compat_debug
```

or with `mamba`:

```
mamba search cpython --channel jaimergp/label/zlib-ng-compat_debug
```

Alternatively, `mamba repoquery` may provide more information:

```
# Search all versions available on your platform:
mamba repoquery search cpython --channel jaimergp/label/zlib-ng-compat_debug

# List packages depending on `cpython`:
mamba repoquery whoneeds cpython --channel jaimergp/label/zlib-ng-compat_debug

# List dependencies of `cpython`:
mamba repoquery depends cpython --channel jaimergp/label/zlib-ng-compat_debug
```




Updating python-feedstock
=========================

If you would like to improve the python recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`jaimergp` channel, whereupon the built conda packages will be available for
everybody to install and use from the `jaimergp` channel.
Note that all branches in the conda-forge/python-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks, and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@chrisburr](https://github.com/chrisburr/)
* [@isuruf](https://github.com/isuruf/)
* [@jakirkham](https://github.com/jakirkham/)
* [@katietz](https://github.com/katietz/)
* [@mbargull](https://github.com/mbargull/)
* [@msarahan](https://github.com/msarahan/)
* [@ocefpaf](https://github.com/ocefpaf/)
* [@pelson](https://github.com/pelson/)
* [@scopatz](https://github.com/scopatz/)
* [@xhochy](https://github.com/xhochy/)

