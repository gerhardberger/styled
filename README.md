Styled.js
=========

Styled is an easy way to get access to the CSS rules in Javascript using selectors.
It is a jQuery plugin. It is useful for instance if you do not have inserted the element in the page, you can still access its CSS properties easily. It depends on Underscore.

Example
-------

``` js
var foo = $('.foo').styled()

console.log(foo.css)          // an object with all the styles
console.log(foo.get('width')) // a spesific style 
``

.styled(*filename*)
-------------------

The *filename* is optional, if there is a filename (or more separated by a comma, e.g `.styled('file1, file2')`), it just uses those files, but if it is empty, it uses all of the stylesheets.

Methods
-------

>  <h3>.get(*property*)</h3>
>> It returns a spesific style (all of them accessable in the `css` field in the return of `.styled()`).

Further plans
-------------

 * .set(*property*,*value*)
 * wrapper functions for special stuffs