PScript
========

PScript is a Python to JavaScript compiler, and is also the name of the subset
of Python that this compiler supports. It was developed as a part of
[Flexx](http://flexx.live) (as `flexx.pyscript`) and is now represented
by its own project. Although it is still an important part of Flexx, it can
also be useful by itself.


Installation
------------

PScript requires Python 2.7 or 3.5+ and also works on pypy. 

* ``conda install pscript -c conda-forge``, or
* ``pip install pscript``


Short example
-------------

```py

   from pscript import py2js
   
   def foo(a, b=2):
      print(a - b)
   
   print(py2js(foo))
```

Gives:

```js
   var foo;
   foo = function flx_foo (a, b) {
      b = (b === undefined) ? 2: b;
      console.log((a - b));
      return null;
   };
```

License
-------

PScript makes use of the liberal 2-clause BSD license. See LICENSE for details.
