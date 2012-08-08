Styled.js
=========

Styled is an easy way to get access to the CSS rules in Javascript using selectors.
It is a jQuery plugin. It is useful for instance if you do not have inserted the element in the page, you can still access its CSS properties easily. It depends on Underscore.
[Demo](http://felix.lovassy.hu/projects/gellert/styled/example.html)

Example
-------

``` js
var foo = $('.foo').styled()

console.log(foo.css)          // an object with all the styles
console.log(foo.get('width')) // a spesific style 
```

.styled(*filename*)
-------------------

The *filename* is optional, if there is a filename (or more separated by a comma, e.g `.styled('file1, file2')`), it just uses those files, but if it is empty, it uses all of the stylesheets.

Methods
-------

<h3>.get(*property*)</h3>
It returns a spesific style (all of them accessable in the `css` field in the return of `.styled()`).

<h3>.set(*key*, *value* || *options*)</h3>
You can pass in two strings (key, value) or an object, just in jQuery's `.css()`.

``` js
  var foo = $('.foo').styled()
  foo.set('width', '960px')
  
  foo.set({
    color: '#999'
    , 'font-size': '12px'
    , 'font-weight': 'bold'
  })
```

Further plans
-------------

 * wrapper functions for special stuffs