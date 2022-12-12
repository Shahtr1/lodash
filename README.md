# HOW TO GUIDE FOR LODASH

**_Some useful functions_**

## Manipulating Strings

### 1. Deburr
```js
	> _.deburr("déjà vu");
	'deja vu'
```
* It strips the symbols that are not in normal latin set

### 2. Escape
```js
	> _.escape("this & string");
	'this &amp; string'
```
* It converts the charaters into their html equivalent.

### 3. Unescape
```js
	> _.unescape('&lt;h1&gt;tag&lt;/h1&gt;')
	'<h1>tag</h1>'
```
* It reverses the escape process.

### 4. Intersection
```js
	> _.unescape('&lt;h1&gt;tag&lt;/h1&gt;')
	'<h1>tag</h1>'
```
* 

