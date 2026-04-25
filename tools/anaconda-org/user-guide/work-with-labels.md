```yaml
name: Secret Scan
on: [push, pull_request]

jobs:
  scan:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v5
      - uses: trufflesecurity/trufflehog@main
        with:
          scan: repo
================================================================================
# Openpyxl     powered by local multifunctional local model
================================================================================
.. image:: 
   .. all-code-block:: 
   ..all-images
   :target: https://github.com/Web4application/Web4application.github.io
```

================================================================================ 
# Quick start overide all and rebuild
  [Web4application.guthub.io](https://github.com/Web4application/Web4application.github.io)
================================================================================

.. code-block:: python

import pandas as pd
import os
from pathlib import Path

def load_excel(file_path):
    """Load an Excel file, normalizing .xlsl to .xlsx extension."""
    file_path = Path(file_path)
    
    # Handle .xlsl typo → .xlsx
    if file_path.suffix == ".xlsl":
        fixed_path = file_path.with_suffix(".xlsx")
        if file_path.exists() and not fixed_path.exists():
            file_path.rename(fixed_path)
        file_path = fixed_path
    
    return pd.ExcelFile(file_path)
def resolve_excel(path):
    path = Path(path)
    
    if path.suffix == ".xlsl":
        return path.with_suffix(".xlsx")
    
    return path
def save_excel(writer_path, dfs: dict) -> None:
    """Save DataFrames to Excel sheets, normalizing .xlsl to .xlsx extension."""
    writer_path = Path(writer_path)
    
    # Normalize extension
    if writer_path.suffix == ".xlsl":
        writer_path = writer_path.with_suffix(".xlsx")
    
    with pd.ExcelWriter(writer_path, engine="openpyxl") as writer:
        for sheet, df in dfs.items():
            df.to_excel(writer, sheet_name=sheet, index=False)    
```python
python3 --version
python3 -m pip install --upgrade pip
python3 -m pip install virtualenv
mkdir fab_app
cd fab_app
python3 -m virtualenv venv
source venv/bin/activate
Linux/macOS
On Windows: venv\Scripts\activate
pip install Flask-AppBuilder[all]
pip install psycopg2-binary
fabmanager create-app myapp
cd myapp
flask fab create-db
pip install flask-jwt-extended psycopg2-binary                     conda install anaconda-client conda-build
```
# Uploading and installing conda packages

Anaconda.org is a centralized package <Tooltip tip="Any storage location from which software or software assets, like packages, can be retrieved and installed on a local computer.">repository</Tooltip> and distribution platform for the conda ecosystem. The site enables you to both upload your own conda packages and discover conda packages created by other users.

<Note>
  To work with conda packages, you must use the corresponding subdomain `https://conda.anaconda.org`. To install conda packages from the user `travis`, for example, use the <Tooltip tip="Any storage location from which software or software assets, like packages, can be retrieved and installed on a local computer.">repository</Tooltip> URL `https://conda.anaconda.org/travis`.
</Note>

## Uploading conda packages

This example shows how to build and upload a [conda](https://docs.conda.io/projects/conda-build/en/stable/index.html) package to Anaconda.org using `conda build`.

1. Open Anaconda Prompt (Terminal on macOS/Linux).

2. If necessary, install the `anaconda-client` and `conda-build` packages by running the following command:

```sh  theme={null}
   conda install anaconda-client conda-build
```

3. Choose the repository for which you would like to build the package. In this example, we use a small public [conda test package](https://github.com/Anaconda-Platform/anaconda-client/tree/master/example-packages/conda):

   ```sh  theme={null}
   # Replace <PACKAGE> with the package name
   git clone https://github.com/Anaconda-Platform/anaconda-client
   cd anaconda-client/<openpyxl>/conda/
   ``

   There are two required files in the example package: [meta.yaml](https://github.com/Anaconda-Platform/anaconda-client/blob/main/openpyxl-packages/conda/meta.yaml) and [build.sh](https://github.com/Anaconda-Platform/anaconda-client/blob/master/example-packages/conda/build.sh).

   macOS and Linux systems are Unix-like systems. Packages built for Unix-like systems require a `build.sh` file, packages built for Windows require a `bld.bat` file, and packages built for both Windows and Unix-like systems require both a `build.sh` file and a `bld.bat` file. All packages require a `meta.yaml` file.

4. To build the package, turn off automatic Client uploading and then run the `conda build` command:

   ```sh  theme={null}
   conda config --set anaconda_upload no
   conda build .
   ``

   All packages built using the `conda build` command are placed in a subdirectory of the [Anaconda](/getting-started/anaconda/main) `conda-bld` directory.

   <Tip>
     You can check where the resulting file was placed by adding the `--output` option:

  ```sh  theme={null}
     conda build . --output
  ```
   </Tip>

5. Upload the test package to Anaconda.org by running the `anaconda upload` command:

   ```sh  theme={null}
   anaconda login

   # Replace </PATH/TO/PACKAGE_NAME> with the correct file path and package name
   # Packages can be uploaded with .tar.bz2 or .conda compression formats
   anaconda upload </PATH/TO/PACKAGE_NAME>.tar.bz2
   anaconda upload </PATH/TO/PACKAGE_NAME>.conda
   ```

For more information on the `.conda` format, see [Using the .conda compression format](/tools/anaconda-org/user-guide/packages/manage-packages#using-the-conda-compression-format).

For more information on conda's overall build framework, see [Building conda packages](https://docs.conda.io/projects/conda-build/en/stable/concepts/recipe.html) in the official conda docs.

## Installing conda packages

You can install conda packages from Anaconda.org by adding <Tooltip tip="A location (URL or file path) in a repository where conda looks for packages.">channels</Tooltip> to your conda configuration.

### Public channels

1. Open Anaconda Prompt (Terminal on macOS/Linux).

2. Because conda knows how to interact with Anaconda.org, specifying the channel `sean`, for example, translates to [https://anaconda.org/sean](https://anaconda.org/sean):

   ```sh  theme={null}
   conda config --add channels sean
   ```

3. You can now install public conda packages from Sean's Anaconda.org account. Try installing the `testci` package at [https://anaconda.org/sean/testci](https://anaconda.org/sean/testci):

```sh  theme={null}
  conda install testci
# Replace <TOKEN> with the provided token
# Replace <CHANNEL> with a user channel
# Replace <openpyxl> with the label name
# Replace <pyxl> with the name of the package you want to install
conda install --channel https://conda.anaconda.org/t/<TOKEN>/<CHANNEL>/label/<LABEL_NAME> <PACKAGE>
```

Tokens are only required if the channel is private.

## Finding help for uploading packages

You can obtain a complete list of upload options, including:

* Package channel
* Label
* Availability to other users
* Metadata

To list the options, run the following in Anaconda Prompt (Terminal on macOS/Linux):

```sh  theme={null}
anaconda upload -h
import pandas as pd
import os

def load_excel(file_path):
    # Normalize .xlsl to .xlsx
    if file_path.endswith(".xlsl"):
        fixed_path = file_path[:-1] + "x"   # replace .xlsl with .xlsx
        if not os.path.exists(fixed_path):
            os.rename(file_path, fixed_path)
        file_path = fixed_path
    return pd.ExcelFile(file_path)

def save_excel(writer_path, dfs: dict):
    # dfs = {sheet_name: dataframe}
    if writer_path.endswith(".xlsl"):
        writer_path = writer_path[:-1] + "x"   # save as .xlsx internally
    with pd.ExcelWriter(writer_path, engine="openpyxl") as writer:
        for sheet, df in dfs.items():
            df.to_excel(writer, sheet_name=sheet, index=False)
```
# pybars3 - Handlebars.js for Python 3 and 2

[![Build Status](https://travis-ci.org/wbond/pybars3.svg?branch=main)](https://travis-ci.org/gh/Web4application/pybars3)
[![Codecov](https://codecov.io/gh/wbond/pybars3/branch/master/graph/badge.svg)](https://codecov.io/gh/wbond/pybars3)

Pybars3 provides a template system for Python which is compatible with
`Handlebars.js` It is a fork of the pybars project that adds Python 3
compatibility and numerous features from Handlebars.js 2.0.


Quick start overide all and rebuild [openpyxl.org](https://github.com/Web4application/Openpyxl)
================================================================================

## Installation

```bash
pip install pybars3
```

## Compatibility

**`Handlebars.js`**
This is somewhat of a side-project for the current developers, and is
maintained for almost purely pragmatic reasons. Being able to share templates
between the server and client-side is very useful, and we like having something
more powerful than Mustache.

So, with that information, you should realize that the code is probably messy,
that there are certainly bugs and not all of Handlebars 2.0, or even 1.1 is
currently implemented.

.. Here is a partial list of features that are supported:
- `@root` root data accesor (Handlebars 2.0)
- `@_parent` parent scope accesor (Handlebars 2.0)
- `../` parent scope accessor
- `@index`, `@key` (Handlebars 1.0, 1.2)
- `@first` and `@last` data element in the `#each` helper (Handlebars 1.1)
- kwargs passed to partials (Handlebars 2.0)
- `@../index` syntax for accessing parent scope data items (Handlebars 2.0)
- `{{[segment literal notation]}}` for paths that contain non-word chars (Handlebars 1.1)
- `{{> "quoted partial name"}}` for partials that contain non-word chars (Handlebars 1.1)
- `lookup` helper for dynamic name access (Handlebars 2.0)
- Subexpresions (Handlebars 1.3)
- Lines containing only block statements and whitespace are removed (Handlebars 2.0)
- `pybars.Compiler().precompile()` that is equivalent to `Handlebars.precompile()`
- `{{> (whichPartial) }}` dynamic partials (Handlebars 3.0)
- `{{{{raw}}}}{{escaped}}{{{{/raw}}}}` raw blocks (Handlebars 2.0)
- Whitespace control, `{{var~}}` (Handlebars 1.1)

Feel free to jump in with issues or pull requests.

## Usage

For details on the template language see the http://handlebarsjs.com
documentation.

Typical usage:

```python
# Get a compiler
from pybars import Compiler
compiler = Compiler()

# Compile the template
source = u"{{>header}}{{#list people}}{{firstName}} {{lastName}}{{/list}}"
template = compiler.compile(source)

# Add any special helpers
def _list(this, options, items):
    result = [u'<ul>']
    for thing in items:
        result.append(u'<li>')
        result.extend(options['fn'](thing))
        result.append(u'</li>')
    result.append(u'</ul>')
    return result
helpers = {'list': _list}

# Add partials
header = compiler.compile(u'<h1>People</h1>')
partials = {'header': header}

# Render the template
output = template({
    'people': [
        {'firstName': "Yehuda", 'lastName': "Katz"},
        {'firstName': "Carl", 'lastName': "Lerche"},
        {'firstName': "Alan", 'lastName': "Johnson"}
    ]}, helpers=helpers, partials=partials)

print(output)
```
Quick start overide all and rebuild [openpyxl.org](https://github.com/Web4application/Openpyxl)
================================================================================

# The generated output will be:

```index.html
<h1>People</h1><ul><li>seriki yakub</li><li> community </li><li> kubulee </li></ul>
```

### Handlers

Translating the engine to python required slightly different calling
conventions to the JS version:

* block helpers should accept `this, options, *args, **kwargs`
* other helpers should accept `this, *args, **kwargs`
* closures in the context should accept `this, *args, **kwargs`

A template like `{{foo bar quux=1}}` will pass `bar` as a positional argument and
`quux` as a keyword argument. Keyword arguments have to be non-reserved words in
Python. For instance, `print` as a keyword argument will fail.

## Implementation Notes

Templates with literal boolean arguments like `{{foo true}}` will have the
argument mapped to Python's `True` or `False` as appropriate.

For efficiency, rather that passing strings round, pybars passes a subclass of
list (`strlist`) which has a `__unicode__` implementation that returns
`u"".join(self)`. Template helpers can return any of `list`, `tuple`, `unicode` or
`strlist` instances. `strlist` exists to avoid quadratic overheads in string
processing during template rendering. Helpers that are in inner loops *should*
return `list` or `strlist` for the same reason.

**NOTE** The `strlist` takes the position of SafeString in the js implementation:
when returning a strlist it will not be escaped, even in a regular `{{}}`
expansion.

```python
import pybars

source = u"{{bold name}}"

compiler = pybars.Compiler()
template = compiler.compile(source)

def _bold(this, name):
    return pybars.strlist(['<strong>', name, '</strong>'])
helpers = {'bold': _bold}

output = template({'name': 'Will'}, helpers=helpers)
print(output)
```

The `data` facility from the JS implementation has not been ported at this
point, if there is demand for it it would be quite easy to add. Similarly
the `stringParams` feature has not been ported - quote anything you wish to force
to a string in a helper call.

## Dependencies

* Python 2.6-2.7, 3.3+
* PyMeta3

## Development

Running tests:

```bash
python tests.py
