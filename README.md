<!-- swap 2 numbers without using third variable -->

let a = 10;

let b = 20;

a = a + b;

b = a - b;

a = a - b;

console.log(a); // 20

console.log(b); // 10

<!-- swap 2 numbers with using 3rd variable -->

let a = 10;

let b = 20;

let temp = a;

a = b;

b = temp;

console.log(a); // 20

console.log(b); // 10

<!-- Multiply 2 number without using \* symbol -->

function multiply(a,b){

let answer = a;

for(let i=0;i<b-1;i++){

answer += a;

}

return answer;

}

console.log(multiply(2,3))

<!-- check armstrong number or not -->

let num = 153;

let temp = num;

let sum =0;

while(temp>0){

let rem = temp%10;

sum += rem*rem*rem;

temp = parseInt(temp/10);

}

if(sum === num){

console.log('armstrong')

} else {

console.log('not armstrong')

}

<!-- check prime number -->

let num = 7;

let isPrime = true;

for(let i=2;i<=num;i++){

if(num % 2 ==0){

    isPrime=false;

    break;

}

}

if(isPrime){

console.log('prime');

}

else {

console.log('not prime');

}

<!-- Print all number between 1 to 20  -->

for(let i=1;i<=20;i++){

let isPrime = true;

for(let j=2;j<i;j++){

    if(i % j == 0) {

      isPrime = false;

      break;

    }

}

if(isPrime && i > 1) {

    console.log(i)

}

}

<!-- Fibonacci series  -->

let a = 0;

let b =1;

for(let i=0;i<5;i++){

let temp = a + b;

a =b ;

b =temp;

console.log(temp);

}

<!-- Fibonacci series alternative -->

let arr = [1,2];

for(let i=1;i<5;i++){

arr.push(arr[i]+arr[i-1])

}

console.log(arr);

<!-- first non-repeat string  -->

let str = 'absaadde';

for(let i=0;i<str.length;i++){

if(str.indexOf(str.charAt(i))===str.lastIndexOf(str.charAt(i))){

    console.log(str.charAt(i));

    break;

}

}
