### es6features
---
https://github.com/lukehoban/es6features

```js
var odds = evens.map(v => v + 1);
var nums = evens.map((v, i) => v + i);
var pairs = evens.map(v => ({even: v, odds: v + 1}));
nums.forEach(v => {
  if (v % 5 === 0)
    fives.push(v);
});
var bob = {
  _name: "Bob",
  _friends: [],
  printFriends() {
    this._friends.forEach(f =>
      console.log(this._name + " knows " + f));
  }
}

class SkinnedMesh extends THREE.Mesh {
  constructor(geometry, matrials) {
    super(geometry, materials);
    
    this.idMatrix = SkinnedMesh.defaultMatrix();
    this.bones = [];
    this.boneMatrices = [];
  }
  update(camera){
    super.update();
  }
  get boneCount() {
    return this.bones.length;
  }
  set matrixType(matrixType) {
    this.idMatrix = SkinnedMesh[matrixType]();
  }
  static defaultMatrix() {
    return new THREE.Matrix4();
  }
}

var obj = {
  __proto: theProtoObj,
  handler,
  toString() {
    return "d " + super.toString();
  },
  [ 'prop_' + (() => 42)() ]: 42
};

var name = "Bob", time = "today";
`Hello ${name}, how are you ${time}?`
POST `http://goo.org/bar?a=${a}&b=${b}
      Content-Type: application/json
      X-Credentials: ${credentials}
      { "foo": ${foo},
        "bar": ${bar}}`(myOnReadyStateChangeHandler);

var [a, , b] = [1,2,3];
var { op: a, lhs: { op: b }, rhs: c }
  = getASTNode()
  
var  {op, lhs, rhs} = getASTNode()

funciton g({name: x}){
  console.log(x);
}
g({name: 5})

var [a] = [];
a === undefined;

var [a = 1] = [];
a === 1;

function f(x, y=12){
  return x + y ;
}
f(3) == 15

function f(x, ...y){
  return x * y.length;
}
f(3, "hello", true) == 6

function f(x, y, z){
  return x + y + z;
}
f(...[1,2,3]) == 6

function f() {
  {
    let x;
    {
      const x = "sneaky";
      x = "foo";
    }
    let x = "inner";
  }
}

let fibonacci = {
  [Symbol.iterator]() {
    let pre = 0, cur = 1;
    return {
      next() {
        [pre, cur] = [cur, pre + cur];
        return { done: false, value: cur }
      }
    }
  }
}

for (var n of fibonacci) {
  if (n > 1000)
    break;
  console.log(n);
}

interface IteratorResult {
　  done: boolean;
  value: any;
}
interface Iterator {
  next(): IteratorResult;
}
interface Iterable {
  [Symbol.iterator](): Iterator
}

var fibonacci = {
  [Symbol.iterator]: function*() {
    var pre = 0, cur = 1;
    for (;;) {
      var temp = pre;
      pre = cur;
      cur += temp;
      yield cur;
    }
  }
}
for(var n of fibonacci){
  if (n > 1000)
    break;
  console.log(n);
}

interface Generator extends Iterator {
  next(value?: any): IteratorResult;
  throw(exception: any);
}

"".length == 2
"".match()[].length == 2
""=""="\uD842\uDFB7"
"".codPointAt(0) == 0x20BB7
for(var c of ""){
  console.log(c);
}

export function sum(x, y){
  return x + y;
}
export var pi = 3.141593;

import * as math from "lib/math";
alert("" + math.sum(math.pi, math.pi));

import {sum, pi} from "lib/math";
alert("" + sum(pi, pi));

export * from "lib/math";
export var e = 2.61828182846;
export default function(x){
  return Math.log(x);
}

import ln, {pi, e} from "lib/mathplusplus";
alert("" + ln(e)*pi*2);
```

```
```

```
```

