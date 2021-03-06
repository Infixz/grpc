gRPC Python
=========
The Python facility of gRPC.

Status
-------
Alpha : Ready for early adopters

PREREQUISITES
-------------
- Python 2.7, virtualenv, pip
- [homebrew][] on Mac OS X, [linuxbrew][] on Linux.  These simplify the installation of the gRPC C core.

INSTALLATION
-------------
On Mac OS X, install [homebrew][]. On Linux, install [linuxbrew][].
Run the following command to install gRPC Python.
```sh
$ curl -fsSL https://goo.gl/getgrpc | bash -s python
```
This will download and run the [gRPC install script][], then install the latest version of the gRPC Python package.  It also installs the Protocol Buffers compiler (_protoc_) and the gRPC _protoc_ plugin for python.

BUILDING FROM SOURCE
---------------------
- Clone this repository
- Build the gRPC core from the root of the
  [gRPC Git repository](https://github.com/grpc/grpc)
```
$ make shared_c static_c
```

- Use build_python.sh to build the Python code and install it into a virtual environment
```
$ tools/run_tests/build_python.sh
```

TESTING
-------

- Use run_python.sh to run gRPC as it was installed into the virtual environment
```
$ tools/run_tests/run_python.sh
```

PACKAGING
---------

- Install packaging dependencies
```
$ pip install setuptools twine
```

- Push to PyPI
```
$ ../../tools/distrib/python/submit.py
```

[homebrew]:http://brew.sh
[linuxbrew]:https://github.com/Homebrew/linuxbrew#installation
[gRPC install script]:https://raw.githubusercontent.com/grpc/homebrew-grpc/master/scripts/install
