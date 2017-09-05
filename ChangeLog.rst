3.0.1
-----
It's a milestone for Pyarmor, from this version, use ctypes import
dynamic library of core functions, other than by python extensions
which need to be built with every python version.

Besides, in this version, a big change which make Pyarmor could avoid
soure script got by c debugger.
	
* Use ctypes load core library other than python extentions which need
  built for each python version.
* "\__main__" block not running in encrypted script.
* Avoid source code got by c debugger.
* Change default outoupt path to "build" in command "encrypt"
* Change option "--bind" to "--bind-disk" in command "license"
* Document usages in details

2.6.1
-----
* Fix encrypted scripts don't work in multi-thread framework (Django).

2.5.5
-----
* Add option '-i' for command 'encrypt' so that the encrypted scripts will be saved in the original path.

2.5.4
-----
* Verbose tracelog when checking license in trace mode.
* In license command, change default output filename to "license.lic.txt".
* Read bind file when generate license in binary mode other than text mode.

2.5.3
-----
* Fix problem when script has line "from __future__ import with_statement"
* Fix error when running pyarmor by 32bit python on the 64bits Windows.
* (Experimental)Support darwin_15-x86_64 platform by adding extensions/pytransform-2.3.3.darwin_15.x86_64-py2.7.so

2.5.2
-----
* License file can mix expire-date with fix file or fix key.
* Fix log error: not enough arguments for format string

2.5.1
-----
* License file can bind to ssh private key file or any other fixed file.

2.4.1
-----
* Change default extension ".pyx" to ".pye", because it confilcted with CPython.
* Custom the extension of encrypted scripts by os environment variable: PYARMOR_EXTRA_CHAR
* Block the hole by which to get bytescode of functions.

2.3.4
-----
* The trial license will never be expired (But in trial version, the
  key used to encrypt scripts is fixed).

2.3.3
-----
* Refine the document

2.3.2
-----
* Fix error data in examples of wizard

2.3.1
-----
* Implement Run function in the GUI wizard
* Make license works in trial version

2.2.1
-----
* Add a GUI wizard
* Add examples to show how to use pyarmor

2.1.2
-----
* Fix syntax-error when run/import encrypted scripts in linux x86_64

2.1.1
-----
* Support armv6

2.0.1
-----
* Add option '--path' for command 'encrypt'
* Support script list in the file for command 'encrypt'
* Fix issue to encrypt an empty file result in pytransform crash

1.7.7
-----

* Add option '--expired-date' for command 'license'
* Fix undefined 'tfm_desc' for arm-linux
* Enhance security level of scripts

1.7.6
-----

* Print exactaly message when pyarmor couldn't load extension
  "pytransform"

* Fix problem "version 'GLIBC_2.14' not found"

* Generate "license.lic" which could be bind to fixed machine.

1.7.5
-----

* Add missing extensions for linux x86_64.

1.7.4
-----

* Add command "licene" to generate more "license.lic" by project
  capsule.

1.7.3
-----

* Add information for using registration code

1.7.2
-----

* Add option --with-extension to support cross-platform publish.
* Implement command "capsule" and add option --with-capsule so that we
  can encrypt scripts with same capsule.
* Remove command "convert" and option "-K/--key"

1.7.1
-----

* Encrypt pyshield.lic when distributing source code.

1.7.0
-----

* Enhance encrypt algorithm to protect source code.
* Developer can use custom key/iv to encrypt source code
* Compiled scripts (.pyc, .pyo) could be encrypted by pyshield
* Extension modules (.dll, .so, .pyd) could be encrypted by pyshield