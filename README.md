About
=====

Cubes.js is a JavaScript framework for online analytical processing (OLAP) server Cubes - Slicer.

Cubes: http://databrewery.org/cubes.html
Server documentation: http://packages.python.org/cubes/server.html

Namespaces and object prototypes:

* cubes - top level namespace
* cubes.Server - Slicer server connection (based on root URL)
* cubes.Model - logical model
* cubes.Dimension
* cubes.Hierarchy
* cubes.Level
* cubes.Attribute
* cubes.Cell - browsing context (has multiple cuts)
* cubes.PointCut
* cubes.SetCut
* cubes.RangeCut

This library supports the extended features of cuts -- inversion, full escaping of sensitive characters --
as implemented in the Squarespace fork of Cubes at https://github.com/Squarespace/cubes .

Not yet fully implemented:

* cubes.Browser - aggregation browser, only supports aggregate() so far


Requirements
============

Squarespace's version of cubes.js does not require any external library, neither underscore.js nor jQuery.
However, to use the query() function or to fetch the model JSON, you must provide a jQuery-compatible ajax function
to the cubes.Server constructor.

Tests
=====

Tests are provided in the test/ folder. Use node and the vows node module to run them:

    $ npm install
    $ vows

The vows tool will run all the .js test files it finds in the test/ folder.

Author
======

Stefan Urbanek, <stefan.urbanek@gmail.com>, @Stiivi, December 2011

Follow @DataBrewery on Twitter for updates.

License
=======

Cubes.js is licensed under MIT license with following addition:

    If your version of the Software supports interaction with it remotely through a computer network, the
    above copyright notice and this permission notice shall be accessible to all users.

Simply said, that if you use it as part of software as a service (SaaS) you have to provide the copyright notice in an about, legal info, credits or some similar kind of page or info box.

For full license see the LICENSE file.
