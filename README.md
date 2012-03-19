## What is This?

The [API reference](https://github.com/mbostock/d3/wiki/API-Reference) for [D3.js](http://mbostock.github.com/d3/) is quite thorough. However, its formatting does not make it easy for me personally to easily see the big picture of what 'classes' of objects are available, what each returns, the legal values for parameters of methods that may be called in many forms, etc.

A specific (and common) example is that `selection.enter()` is not available on a `selection` until you first call `data()`, and the return value of `selection.enter()` does not have all the methods of a real `selection` available to it.

This project aims to create a rigorous and exacting representation of the objects and methods available at various stages. My goal is to import it into [ObjJob](http://objjob.phrogz.net/d3) and further to create some data-driven visualizations.

## How Can I Help?

Fork this project, add some YAML files, and send me a pull request. A few items of note to content authors:

* You can put more than one object/property/method in a file if you like. By convention I'm putting each logical item in its own file, grouping only methods that differ in invocation.

* Objects, methods, and properties (but not parameters) can use a `details` property for large amounts of prose. At this point I have not opted to spend time on examples or regurgitating the wiki, instead relying on the `url` property to link back to the official API docs.

* As seen in the documentation for many methods (e.g. [d3-Selection-attr.yaml](https://github.com/Phrogz/d3hierarchy/blob/master/methods/d3-Selection-attr.yaml)) you can give many flavors of a method the same name and disambiguate them by appending a section symbol and unique identifier (e.g. `attr§value` versus `attr§func`). These names are not shown to the user on ObjJob; they are only to provide unique references for the `seealso` links.

* The `summary` and `details` fields allow Markdown markup to be included. To include a link to another item in the documentation, use a URI like `objjob:language/objectName/methodName§flavor`; the importer will properly convert it to a link within the site.