NodeJS Chinese Remainder Theorem solver
=======================================

If you come here you probably already know what the chinese remainder theorem is.
Here you can find a NodeJS implementation.


**USAGE**

You can fetch this library directly from npm:
```
npm install nodejs-chinese-remainder
```

and then use it on your code like:

```
var crt = require('nodejs-chinese-remainder');

console.log( 'Suppose we have a system of congruences: ' );
console.log( '   x = 5 mod4' );
console.log( '   x = 3 mod5' );
console.log( '   x = 7 mod11' );
console.log( '  The solution is: ' + crt([5,3,7], [4,5,11]));
```

if you are getting trouble because your integer numbers are too large you can use the power of libgmp.
I choose to use *bigint* libs from https://github.com/substack/node-bigint

Here an example:

```
var a1=bigint('507483274265132509471575639764027');
var m1=bigint('269916455047188404153874847098609926219');
var a2=bigint('27723967616827289286920296659419136');
var m2=bigint('170141183460469231731687303715884105728');
var result = crt_bigint([a1, a2],[m1, m2]);
console.log( result.toString() );
```

**References**

- http://en.wikipedia.org/wiki/Chinese_remainder_theorem
- http://rosettacode.org/wiki/Chinese_remainder_theorem
