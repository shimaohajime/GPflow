# GPflow documentation

## This is based on GPflow 1.5.1, modified to work with tensorflow.compat.v1 and python3.9 and later.
## The Modifications made are
- In _settings.py, quadrature.py, session_manager.py, misc.py, actions.py, training/tensorflow_optimizer.py, change "import tensorflow" to "import tensorflow.compat.v1".
- In quadrature.py, change "from collections" to "from collections.abc".
- In _settings.py, change "collections.Mapping" to "collections.abc.Mapping".

## Online

[![Documentation Status (master)](https://readthedocs.org/projects/gpflow/badge/?version=master)](http://gpflow.readthedocs.io/en/master/?badge=master)
[![Documentation Status (develop)](https://readthedocs.org/projects/gpflow/badge/?version=develop)](http://gpflow.readthedocs.io/en/develop/?badge=develop)

We use readthedocs to build the online documentation, and have separate versions for the `master` and `develop` branches: https://gpflow.readthedocs.io/en/master/ (for the latest official release e.g. on PyPI) and https://gpflow.readthedocs.io/en/develop/ (for the latest cutting-edge code available from the develop branch on github).

## Compiling documentation

To compile the GPflow documentation locally:

1. Install doc dependencies
```
pip install sphinx sphinx_rtd_theme numpydoc nbsphinx
```
2. Install pandoc 
```
pip install pandoc
```
If pandoc does not install via pip, or step 4 does not work, go to pandoc.org/installing.html

3. Change directory to `doc`
```
cd doc
```

4. Compile the documentation as html
```
make html
```

5. Check documentation locally by opening (in a browser) doc/build/html/index.html
