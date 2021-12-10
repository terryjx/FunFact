# Welcome to the documentation of FunFact!

[![CI](https://github.com/yhtang/FunFact/actions/workflows/ci.yml/badge.svg?branch=develop)](https://github.com/yhtang/FunFact/actions/workflows/ci.yml)
[![Coverage](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/yhtang/839011f3f7a6bab680b18cbd9a45d2d3/raw/coverage-develop.json)](https://badge.fury.io/py/funfact)
[![PyPI version](https://badge.fury.io/py/funfact.svg)](https://badge.fury.io/py/funfact)
[![Documentation Status](https://readthedocs.org/projects/funfact/badge/?version=latest)](https://funfact.readthedocs.io/en/latest/?badge=latest)
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

## Features

The overall goal of FunFact is to provide a tool to compute the *functional factorization* of algebraic tensors, a.k.a. multidimensional arrays. A functional factorization, in our context, is a generalization of the (linear) factorization of tensors. By generalization, we meant to replace the standard inner/outer product between the factor tensors with some nonlinear operations.

For example, a rank-1 matrix can be factored into the outer product between a column vector and a row vector:

$$
M \approx \mathbf{u} \mathbf{v}^\mathsf{T},
$$

where $M$ is an $n \times m$ matrix, $\mathbf{u}$ is a $n$-dimensional column vector, and $\mathbf{v}$ is a $m$-dimensional row vector. This can be equivalently represented in indexed notation as

$$
M_{ij} \approx \mathbf{u}_i \mathbf{v}_j.
$$

Moreover, if we relace the standard multiplication operation between $\mathbf{u}_i$ and $\mathbf{v}_j$ by an RBF function $\kappa(x, y) = \exp\left[-(x - y)^2\right]$, we then obtain an *RBF approximation* of $M$ such that:

$$
M_{ij} \approx \kappa(\mathbf{u}_i, \mathbf{v}_j).
$$

Given the rich expressivity of nonlinear operators and functional forms, we expect that a proper functional factorization of a tensor can yield representations that are more compact than what is possible withtin the existing linear framework. However, there is (obviously) no free lunch. the challenges to obtain the functional factorization of a tensor is two fold and involves
- Finding the most appropriate **functional form** given a specific piece of data,
- Finding the **component tensors** given the functional form for a specific data.


## How to cite

If you use this package for a publication (either in-paper or electronically), please cite it using the following DOI: https://doi.org/10.11578/dc.20210922.1


## Indices and tables

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`


## Contributors

Current developers:

- [Yu-Hang "Maxin" Tang](https://github.com/yhtang)
- [Daan Camps](https://github.com/campsd)

Previou contributors:

- [Elizaveta Rebrova](https://github.com/erebrova)


## Copyright

FunFact Copyright (c) 2021, The Regents of the University of California,
through Lawrence Berkeley National Laboratory (subject to receipt of
any required approvals from the U.S. Dept. of Energy). All rights reserved.

If you have questions about your rights to use or distribute this software,
please contact Berkeley Lab's Intellectual Property Office at
IPO@lbl.gov.

NOTICE.  This Software was developed under funding from the U.S. Department
of Energy and the U.S. Government consequently retains certain rights.  As
such, the U.S. Government has been granted for itself and others acting on
its behalf a paid-up, nonexclusive, irrevocable, worldwide license in the
Software to reproduce, distribute copies to the public, prepare derivative 
works, and perform publicly and display publicly, and to permit others to do so.

## Funding Acknowledgment

This work was supported by the Laboratory Directed Research and Development Program of Lawrence Berkeley National Laboratory under U.S. Department of Energy Contract No. DE-AC02-05CH11231.



<!-- For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files. -->
