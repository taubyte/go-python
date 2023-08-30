go-python
=====

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Go Report Card](https://goreportcard.com/badge/github.com/taubyte/go-python)](https://goreportcard.com/report/github.com/taubyte/go-python)

Call Python 3 functions and methods from within your Go program while exposing Go functions and
methods to Python.

This is *not* an implementation of Python in Go. Rather, py4go works by embedding the CPython
runtime into your Go program using [cgo](https://github.com/golang/go/wiki/cgo) functionality.

The expected use cases are not low-latency integration, but rather *tight* bidirectional
integration. You can combine the full Go ecosystem with the full Python ecosystem.

Though you can achieve some integration by using Go's [exec](https://pkg.go.dev/os/exec)
package to run `python`, with py4go you get fine-grained access to individual functions, objects,
methods, and variables.

To get started try running [`scripts/example`](scripts/example/). Note that you need the Python
development libraries installed. E.g. in Fedora:

    sudo dnf install python3-devel

