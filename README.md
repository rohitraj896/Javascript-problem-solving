1. swap 2 numbers without using third variable

let a = 10;
let b = 20;

a = a + b;
b = a - b;
a = a - b;

console.log(a); // 20
console.log(b); // 10

2. swap 2 numbers with using 3rd variable

let a = 10;
let b = 20;

let temp = a;
a = b;
b = temp;

console.log(a); // 20
console.log(b); // 10
