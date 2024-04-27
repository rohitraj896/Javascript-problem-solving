1.swap 2 numbers without using third variable

let a = 10;

let b = 20;

a = a + b;

b = a - b;

a = a - b;

console.log(a); // 20

console.log(b); // 10

2.swap 2 numbers with using 3rd variable

let a = 10;

let b = 20;

let temp = a;

a = b;

b = temp;

console.log(a); // 20

console.log(b); // 10

3.Multiple 2 number without using \* symbol

function multiply(a,b){
let answer = a;

for(let i=0;i<b-1;i++){
answer += a;
}
return answer;
}

console.log(multiply(2,3))
