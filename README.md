## What is This?

The [API reference](https://github.com/mbostock/d3/wiki/API-Reference) for [D3.js](http://mbostock.github.com/d3/) is quite thorough. However, its formatting does not make it easy for me personally to easily see the big picture of what 'classes' of objects are available, what each returns, the legal values for parameters of methods that may be called in many forms, etc.

A specific (and common) example is that `selection.enter()` is not available on a `selection` until you first call `data()`, and the return value of `selection.enter()` does not have all the methods of a real `selection` available to it.

This project aims to create a rigorous and exacting representation of the objects and methods available at various stages. Once complete my goal is to import it into [ObjJob](http://objjob.phrogz.net/) and further to create some data-driven visualizations.