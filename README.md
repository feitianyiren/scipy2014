# Using Fatiando a Terra to solve inverse problems in geophysics

[Leonardo Uieda](http://www.leouieda.com),
[Vanderlei C. Oliviera Jr](http://fatiando.org/people/oliveira-jr),
[Valéria C. F. Barbosa](http://lattes.cnpq.br/0391036221142471)

Inverse problems haunt the nightmares of geophysics graduate students.
I'll demonstrate how to conquer them using Fatiando a Terra.
The new machinery in Fatiando
contains many ready-to-use components
and automates as much of the process as possible.
You can go from zero to regularized gravity inversion
with as little as 30 lines of code.
I'll walk through an example to show you how.

## Poster

![The poster.](https://raw.githubusercontent.com/leouieda/scipy2014/master/poster-low-res.png)

The notebook
[gravity_inversion.ipynb](http://nbviewer.ipython.org/github/leouieda/scipy2014/blob/master/gravity_inversion.ipynb)
was used to create all figures and code in the poster.

A PDF of this poster is permanently archived at figshare: [doi:10.6084/m9.figshare.1089987](http://dx.doi.org/10.6084/m9.figshare.1089987)

[poster_summary.ipynb](http://nbviewer.ipython.org/github/leouieda/scipy2014/blob/master/poster_summary.ipynb)
is a short version of the above notebook.

## Scipy2014

The notebook
[scipy_hashtag.ipynb](http://nbviewer.ipython.org/github/leouieda/scipy2014/blob/master/hashtag/scipy_hashtag.ipynb)
uses the finite-difference wave propagation module of Fatiando to make an
animated gif of #Scipy2014.

![#Scipy2014](https://raw.githubusercontent.com/leouieda/scipy2014/master/hashtag/scipy2014.gif)

## Abstract

The inner properties of the Earth
can usually only be inferred
through indirect measurements of their effects.
For example,
density variations
cause disturbances in the gravity field
and seismic velocity variations
affect the path of seismic waves.
From a mathematical point of view,
this inference is an inverse problem.
To complicate things, geophysical inverse problems are usually ill-posed,
meaning that a solution:

* doesn't exist;
* exists but is non-unique;
* exists and is unique but is unstable;

These problems can usually be resolved
through least-squares estimation and regularization.

Research in geophysical inverse problems
involves the development of:
new methodologies for parametrization,
different approaches to regularization,
new algorithms to handle large-scale problems,
combinations of existing methods,
etc.
All of the aforementioned developments
require the creation of software,
usually from scratch.
Furthermore,
most scientific software
are not designed with reuse in mind,
making remixing published methods difficult,
if not impossible.

We tackled these problems
by developing `fatiando.inversion`,
a framework for solving inverse problems
in [Fatiando a Terra](http://www.fatiando.org).
The goals of `fatiando.inversion` are:

* Enable writing code that
  intuitively maps to the theory (equations);
* Provide a consistent interface for all solvers
  (similar to that adopted by [scikit-learn](http://scikit-learn.org/));
* Automate the process of implementing a new inverse problem;
* Allow reuse and remixing with as little code as possible;

In this talk,
I'll briefly cover
the mathematics involved
and the design of our new API.
I'll walk through the process of
implementing a new inverse problem
(in about 30 lines of code)
using the example of
estimating the relief of a sedimentary basin
from its gravity anomaly.
Finally,
I'll conclude by outlining
how we are using this framework in our own research,
what we are currently working on,
and our plans for the future.
