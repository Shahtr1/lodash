# HOW TO GUIDE FOR LODASH

```js
const _ = require('lodash');
```

**_<ins>Some useful functions:</ins>_**

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

## Manipulating Arrays

### 1. Intersection
```js
	> _.intersection([1,2,3,4,5],[3,4,5])
	[3,4,5]
```
* It gives the array of values that occur in all the given arrays

### 2. IntersectionBy
```js
	> _.intersectionBy([2,4,5,6],[4,8,10], i=>i/2)
	[4]
```
* It takes an additional parameter where we can supply a function which determines how elements are compared

### 3. IntersectionWith
```js
	> var obj1 = [{a:1,b:2},{a:2,b:3}]
	> var obj2 = [{a:1,b:1},{a:1,b:2}]
	> _.intersectionWith(obj1, obj2, _.isEqual)
	[{a:1,b:2}]
```
* It can compare objects inside array

### 4. Union
```js
	> _.union([1,2,2,3],[2,2,3,4])
	[1,2,3,4]
```
* It gives us union of unique elements

##### Same is for _<ins>UnionWith</ins>_ and _<ins>UnionBy</ins>_ as for _<ins>IntersectionWith</ins>_

### 5. Zip
```js
	> _.zip([1,2,3,4], [10,20,30,40,50], [2,4,6,8])
	[[1,10,2], [2,20,4], [3,30,6], [4,40,8], [undefined,50,undefined]]
```
* flips rows and columns

##### _<ins>Unzip</ins>_ does the opposite

### 6. Chunk
```js
	> _.chunk(['a','b','c','d'], 2)
	[['a','b'], ['c','d']]
```
* Splits array as defined

### 7. Compact
```js
	> _.compact([undefined,null,0,1,2,3])
	[1,2,3]
```
* Removes falsy values from array like 0, false, '', null, undefined, NaN

### 8. Uniq
```js
	> _.uniq([1,2,3,4,5,5])
	[1,2,3,4,5]
```
* It gives a unique value only from the first array, so it differs from _union_ there

##### Same is for _<ins>UniqWith</ins>_ and _<ins>UniqBy</ins>_ as for _<ins>IntersectionWith</ins>_
##### We also have _<ins>SortedUniq</ins>_ and _<ins>SortedUniqBy</ins>_ which only work on Sorted arrays, to make it fast 

### 9. Xor
```js
	> _.xor([1,2], [3,4])
	[1,3]
```
* It gives a different values from arrays

##### Same is for _<ins>XorWith</ins>_ and _<ins>XorBy</ins>_ as for _<ins>IntersectionWith</ins>_

### 10. Difference
```js
	> _.difference([1,2,3,4,5], [3,4,5])
	[1,2]
```
* It gives the difference between the first and second array, elements of first array which do not appear on the second

##### Same is for _<ins>DifferenceWith</ins>_ and _<ins>DifferenceBy</ins>_ as for _<ins>IntersectionWith</ins>_

### 11. Flatten
```js
	> _.flatten([1,[2,[3,4]],5])
	[1,2,[3,4],5]
```
* It flattens an array by one level

### 12. FlattenDeep
```js
	> _.flattenDeep([1,[2,[3,[4]]],5])
	[1,2,3,4,5]
```
* It flattens an array by all levels

##### For _<ins>FlattenDepth</ins>_ we can give number for levels as second argument

### 13. ZipObject
```js
	> _.zipObject(['a','b','c'], [1,2,3])
	{a:1,b:2,c:3}
```
* It zips keys and values together as an object

### 14. ZipObjectDeep
```js
	> _.zipObjectDeep(['a.b'], [1])
	{a:{b:1}}
```
* It supports property paths too


## Manipulating Collections

### 1. FlatMap
```js
	> _.flatMap([1,2,3,4], i=>[i,i])
	[
		1,1,2,2,
		3,3,4,4
	]
```
We can also pass index along with value
```js
	> _.flatMap([1,2,3,4], (v,i)=>`${i}:${v}`)
	[ '0:1', '1:2', '2:3', '3:4' ]
	
```
* It returns an array which has been flattenend by running all the elements through the iteratee function and then flattening the results

### 2. FlatMapDeep
```js
	> _.flatMapDeep([1,[[2],[22]],[3],4], i=>[[[i,i]]])
	[
		1,1,2,22,2,
		22,3,3,4,4
	]
```
* It recursively flattens the result that has been mapped

##### For _<ins>FlatMapDepth</ins>_ we can give number for levels as second argument

## Language Functions

### 1. Eq and isEqual
```js
	> _.eq("a","a")
	true
	> _.eq({a:1},{a:1})
	false
	> _.isEqual({a:1},{a:1})
	true
```

### 2. Clone
```js
	> _.clone({a:1,b:2})
	{a:1,b:2}
```
* It makes a shallow copy of a given object

##### For _<ins>CloneDeep</ins>_ it does a deep clone rather than a shallow clone

## Util & Date Functions







