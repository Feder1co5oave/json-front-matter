json-front-matter 
======

Extract JSON front matter from strings and files in the style of [Jekyll's YAML Front Matter](https://github.com/mojombo/jekyll/wiki/YAML-Front-Matter).

### Method

* `parse( s )` Parses string `s`, returning an object with properties `attributes`, containing the JSON front matter, and `body` containing the rest.

### Usage

```javascript
var fm = require('json-front-matter');

var string = '{{{ "title" : "some title", "array" : [ 1, 2, 3 ] }}} bodybodybody';
var out = fm.parse( string );

console.log( out.body ) // 'bodybodybody'
console.log( out.attributes.title ) // 'some title'
console.log( out.attributes.array ) // [ 1, 2, 3 ]
```
