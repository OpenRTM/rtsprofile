rtsprofile
===============================================================================

rtsprofile is a Python library providing an interface to the RT System Profile
specification. This specification describes a complete RT system and can be
used to reconstruct that system at a later time.

This software is developed at the National Institute of Advanced Industrial
Science and Technology. Approval number H22PRO-1087. The development was
financially supported by the New Energy and Industrial Technology Development
Organisation Project for Strategic Development of Advanced Robotics Elemental
Technologies.  This software is licensed under the Eclipse Public License -v
1.0 (EPL). See LICENSE.txt.


Requirements
------------

rtsprofile uses the new string formatting operations that were introduced in
Python 2.6. It will not function with an earlier version of Python. It has not
been tested with Python 3 and it is likely that several changes will be
necessary to make it function using this version of Python.


Installation
------------

There are several methods of installation available:

1. Download the source (either from the repository or a source archive),
extract it somewhere, and run the commands from that directory.

2. Download the source (either from the repository or a source archive),
extract it somewhere, and use distutils to install it into your Python
distribution:

 a. Extract the source, e.g. to a directory /home/blag/src/rtsprofile

 b. Run setup.py to install rtsprofile to your default Python installation:

    $ python setup.py install

 c. If necessary, set environment variables. These should be set by default,
    but if not you will need to set them yourself. On Windows, you will need to
    ensure that your Python site-packages directory is in the PYTHONPATH
    variable and the Python scripts directory is in the PATH variable.
    Typically, these will be something like C:\Python26\Lib\site-packages\ and
    C:\Python26\Scripts\, respectively (assuming Python 2.6 installed in
    C:\Python26\).

3. Use the Windows installer. This will perform the same job as running
   setup.py (see #2), but saves opening a command prompt. You may still need to
   add paths to your environment variables.


Using the library
-----------------

The library has one main entry point: the RtsProfle class. Create an instance
of this class, giving the constructor just one data source. The library will
parse that source and give you a complete RT System Profile. You can then use
the properties (they're Python properties, not class methods) to access
information about the RT System. For further details, see the doxygen-generated
documentation.


API naming conventions
----------------------

rtsprofile follows the standard Python naming conventions as laid out in PEP8
(http://www.python.org/dev/peps/pep-0008/).

Most importantly, the private, internal API functions begin with an underscore
(_). If a function begins with an underscore, it is not intended for use
outside the class and doing so could lead to undefined behaviour. Only use
those API functions that do not begin with an underscore and have a docstring
in your programs.


Further documentation and examples
----------------------------------

For further documentation, see the Doxygen-generated API documentation.

For examples of using the library, see the "rtresurrect" and "rtcryo" tools.


Future features
---------------

The following features are planned for future releases:

- Complete unit tests.
- Reading and writing in YAML format.
