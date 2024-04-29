---------swap 2 numbers without using third variable---------

let a = 10;

let b = 20;

a = a + b;

b = a - b;

a = a - b;

console.log(a); // 20

console.log(b); // 10

---------swap 2 numbers with using 3rd variable-----------

let a = 10;

let b = 20;

let temp = a;

a = b;

b = temp;

console.log(a); // 20

console.log(b); // 10

---------Multiply 2 number without using \* symbol---------------

function multiply(a,b){

let answer = a;

for(let i=0;i<b-1;i++){

answer += a;

}

return answer;

}

console.log(multiply(2,3))

---------check armstrong number or not-------------

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

----------check prime number-----------

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

---------Print all prime number between 1 to 20----------

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

---------Fibonacci series-----

let a = 0;

let b =1;

for(let i=0;i<5;i++){

let temp = a + b;

a =b ;

b =temp;

console.log(temp);

}

----Fibonacci series alternative-----

let arr = [1,2];

for(let i=1;i<5;i++){

arr.push(arr[i]+arr[i-1])

}

console.log(arr);

-----first non-repeat string----

let str = 'absaadde';

for(let i=0;i<str.length;i++){

if(str.indexOf(str.charAt(i))===str.lastIndexOf(str.charAt(i))){

    console.log(str.charAt(i));

    break;

}

}

-----------reverse string ----------------

let str = 'This is my pen';

let revStr = str.split('').reverse().join('');

console.log(revStr);

-----------reverse string without using inbuild method -----------

let str = 'This is my pen';

let revStr = '';

for(let i=str.length - 1; i>0;i--){

revStr += str[i];

}

console.log(revStr)

---------reverse string only word---------

let str = 'This is my pen';

let revStr = str.split(' ').reverse().join(' ');

console.log(revStr);

--------reverse string word by word -----------

let str = "This is my pen";

let revStr = str.split(' ').map((word)=>{

return word.split('').reverse().join('')

}).join(' ');

console.log(revStr);

-------------remove duplicate string-------------

let str = "This is my pen";

let removeDuplicate = str.split('').filter((element,index,self)=>{

return self.indexOf(element) == index;

}).join('')

console.log(removeDuplicate);

----------------check number is integer or not ------------------

function checkInteger(n){

if(Number.isInteger(n)){

    return true;

} else {

    return false;

}

}

console.log(checkInteger(8));

---------simple callback function example ----------

function callbackFunction (name) {

console.log(name)

}

function outerFunction (callback) {

let name = "Rohit";

callback(name)

}

outerFunction(callbackFunction);

------------number of character count in string---------

let string = "this is my pen";

let letter = 'i';

let count =0;

for(let i=0;i<string.length;i++){

if(string[i] === letter) {

    count++;

}

}

console.log(count);

---------check string is palindrome or not -----------------------

function checkPalindrome(str){

for(let i=0;i<str.length;i++){

    if(str[i] !==str[str.length-1-i]){

      return 'not palindrome'

    }

}

return 'palindrome'

}

console.log(checkPalindrome('madam'));

-------------check palindrome for all element in array ------------------------

function checkPalindrome(str){

for(let i=0;i<str.length;i++) {

    let temp = str[i];

    let isPalindrom = true;

    for(let j=0;j<temp.length-1;j++){

      if(temp[j] !== temp[temp.length-1-j]) {

        isPalindrom = false;

        break;
      }

    }

    if(isPalindrom) {

      console.log('Palindrom')

    } else {

      console.log('not palindrome')

    }

}

}

checkPalindrome(['mam','madam','pen','ada']);

--------------factorial using recursion ----------------

function factorial(n) {

if(n==0 || n==1) {

    return 1;

} else {

    return n * factorial(n-1)

}
}

console.log(factorial(4));

-----------factorial without using recursion -----------------

let num = 4;

for(var fact =1 ; num > 1 ; num--) {

fact \*= num;

}

console.log(fact);

------------currying simple example ---------------

let sum = a => b => c => a+b+c;

console.log(sum(4)(3)(2));
