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

-------make empty object---------

let obj = { a: 10, b: 20};

delete obj.a;

console.log(obj);

-----------flatening array nested level ----------------

let arr = [1,2,[3,4],5,6,[7,8,[9,10],11],12];

console.log(arr.flat(Infinity));

--------flattening array without using inbuild method ----------------

function flattenedArray(arr) {

const flattened = [];

for(let item of arr){

    if(Array.isArray(item)){

      flattened.push(...flattenedArray(item))

    }

    else {

      flattened.push(item)

    }

}

return flattened;

}

const arr = [1,2,[3,4,[5,6],7,[8]],9];

console.log(flattenedArray(arr));

-----Find shortest word length in string ---------------

function findShort(str){

let arr = str.split(' ');

let shortest = arr[0];

for(let i=0;i<arr.length;i++){

    if(arr[i].length < shortest.length){

      shortest = arr[i]

    }

}

return shortest.length;

}

const str = 'This is my pen';

console.log(findShort(str));

-----------2nd largest element in array --------------------------

function secondLargest(arr) {

if(arr.length < 2) {

    return 'array doesnot have 2nd array';

}

let firstLargest = arr[0];

let secondLargest = -Infinity;

for(let i=1;i<arr.length;i++){

    if(arr[i] > firstLargest) {

      secondLargest = firstLargest;

      firstLargest = arr[i];

    } else if(arr[i]>secondLargest && arr[i] !== firstLargest){

      secondLargest = arr[i];

    }

}

if(secondLargest == -Infinity){

    return "no 2nd largest in array"

}

return secondLargest;

}

const array= [7,8,6,9];

console.log(secondLargest(array));

--------------split string --------------------

function splitString(str) {

if(str.length % 2 !==0) {

    str +="_";

}

const temp = [];

for(let i=0;i<str.length;i+=2){

    temp.push(str.slice(i,i+2))

}

return temp;

}

console.log(splitString('abc')); // ['ab','c_'];

----------sorting word in ascending order ------------------

function orderWords(words){

return words.split(' ').sort((a,b)=>{

    return a.match(/\d/) - b.match(/\d/)

}).join(' ')

}

const string = 'i2s Th1is pen4 3my';

console.log(orderWords(string));

-----------------------check panagram ----------------

function isPanagram(string) {

let letters = string.toLowerCase().match(/[a-z]/g);

const uniqueAlphabet = [...new Set(letters)];

return uniqueAlphabet.length === 26;

}

console.log(isPanagram('aBcdefghijklmnopqrstuvwwxyz'));

-----------------count no of chars in array or string-------------

let str = 'a,b,c,d,a,c,e,f,4,5,5';

let strs = str.split(',')

let charCount = {};

for(let count of strs) {

if(charCount[count]) {

    charCount[count] ++;

}

else {

    charCount[count] = 1

}

}

console.log(charCount)

---------cache in js -----------------

function memoize() {

let cache = {};

return (value) => {

    if(value in cache) {

      return cache[value];

    }

    else {

      let result = value + 10;

      cache[result] = value;

      return result;
    }

}
}

const memoizeAdd = memoize();

console.log(memoizeAdd(10));

-----------simple prototype example------------------

function Dog(name) {

this.name = name

}

Dog.prototype.bark = function () {

console.log(this.name)

}

const myDog = new Dog('buddy');

myDog.bark();

-------polyfill for map --------------

Array.prototype.myMap = function (cb) {

let temp = [];

for(let i=0;i<this.length;i++){

    temp.push(cb(this[i]))

}

return temp;

}

const arr = [1,2,3];

const result = arr.myMap((el)=>el \*2);

console.log(result);

---------------Polyfill for forEach -------------------

Array.prototype.myForEach = function (cb) {

for(let i=0;i<this.length;i++) {

    cb(this[i])

}

}

const arr = [1,2,3];

arr.myForEach((x)=>console.log(x))

--------------------polyfill for filter ---------------------

Array.prototype.myFilter = function (cb) {

let temp = [];

for(let i=0;i<this.length;i++) {

    if(cb(this[i])){

      temp.push(this[i])

    }

}

return temp;

}

const arr = [1,2,3,4,5];

const result = arr.myFilter((el)=>el > 3);

console.log(result);

----------polyfill for reduce----------------

Array.prototype.myReduce = function(cb,initialValue) {

let acc = initialValue;

for(let i=0;i<this.length;i++){

    acc = acc ? cb(acc,this[i]): this[i]

}

return acc;

}

const arr = [1,2,3];

const result = arr.myReduce((acc,curr)=>{

return acc+curr;

},0);

console.log(result)

for(var i=0;i<5;i++){

    setTimeout(()=>{

      console.log(i)

    },1000)

}

// output 5 5 5 5 5

for(let i=0;i<5;i++){

    setTimeout(()=>{

      console.log(i)

    },1000)

}

output 0 1 2 3 4
for(var i=0;i<5;i++){

(function(index){

    setTimeout(()=>{

      console.log(index)

    },1000 * i)

})(i)

}

// output every sec 0 1 2 3 4

---------remove duplicates element from array without using filter-------------

const arr = [2,3,4,5,2,3];

const temp = [];

for(let i=0;i<arr.length;i++){

if(temp.indexOf(arr[i]) == -1){

    temp.push(arr[i])

}

}

console.log(temp)

-------print console message after 1sec without using setInterval ------------

function printHello(count){

if(count>0){

    setTimeout(()=>{

      console.log('hello')

      printHello(count-1)

    },1000)

}

}

printHello(5)

---------------------reverse string except special and digit ---------------

function reverseString(str) {

let arr = str.split('');

let start = 0;

let end = str.length - 1;

while(start < end) {

    if(!/[a-zA-Z]/.test(arr[start])){

      start++;

    }

    else if(!/[a-zA-Z]/.test(arr[end])){

      end--;

    }

    else {

      [arr[start],arr[end]] = [arr[end],arr[start]]

      start++;

      end--;

    }

}

return arr.join('')

}

const str ="absc@de#1z";

const revStr= reverseString(str);

console.log(revStr);

----------split array in 3D array----------

function splitArray(arr) {

let temp = [];

for(let i=0;i<arr.length;i+=3) {

    temp.push(arr.slice(i,i+3))

}

return temp

}

const arr = [1,2,3,4,5];

console.log(splitArray(arr))

-----------max count in array ----------

function maxFrequency(arr) {

let arrayCount = {};

for(let i=0;i<arr.length;i++){

    let num = arr[i];

    if(arrayCount[num]){

      arrayCount[num]++

    }

    else {

      arrayCount[num] = 1;

    }

}

let maxCount =0;

let maxElement =null;

for(let key in arrayCount) {

    if(arrayCount[key]>maxCount) {

      maxCount=arrayCount[key];

      maxElement = key;

    }

}

return maxElement;

}

const array = [1,2,1,3,4,6,2,9,2];

const result = maxFrequency(array);

console.log(result);

-------------Least difference in array --------------------

function leastDiff(arr) {

arr.sort((a,b)=>a-b)

let minDiff = Infinity;

for(let i=0;i<arr.length;i++){

    let diff = arr[i] - arr[i-1];

    if(diff<minDiff){

      minDiff = diff;

    }

}

return minDiff;

}

const arr = [1,12,5,8];

const result = leastDiff(arr);

console.log(result)

-----------second highest number in array -------------------

let arr = [3,2,7];

let firstMax = 0;

let secondMax = 0;

for(let i=0;i<arr.length;i++) {

if(arr[i]>firstMax) {

    secondMax = firstMax;

    firstMax = arr[i];

}

else if(arr[i]>secondMax && arr[i] !==firstMax) {

    secondMax = arr[i];

}

}

console.log(secondMax)

----------count max consecutive number ----------------

let arr = [1,1,0,1,0,0,0,0,2,1,0];

let maxConsecutive =0;

let currentConsecutive =0;

for(let count of arr){

if(count==0){

    currentConsecutive++;

    if(currentConsecutive>maxConsecutive){

      maxConsecutive=currentConsecutive;

    }

}

else {

    currentConsecutive=0;

}

}

console.log(maxConsecutive)

--------------balanced string -----------

function isBalanced(str) {

let stack = [];

let openingBrackets = ['[','{','('];

let closingBrackets = [']','}',')'];

for(let char of str) {

    if(openingBrackets.includes(char)){

      stack.push(char)

    } else if(closingBrackets.includes(char)){

      const matchingOpeningBrackets = openingBrackets[closingBrackets.indexOf(char)];

      if(stack.length===0 || stack.pop() !== matchingOpeningBrackets){

        return false;

      }

    }

}

return stack.length === 0;

}

const string = "[{()}]";

const result = isBalanced(string);

console.log(result)

---------------two sum of array --------------------

function TwoSum(arr,target) {

for(let i=0;i<arr.length-1;i++){

    for(let j=i+1;j<arr.length;j++){

      if(arr[i]+arr[j]===target) {

        return [i,j]

      }

    }

}

return []
}

const arr = [1,2,3,5];
const target = 3;

console.log(TwoSum(arr,target));

-----------replace hyphen(-) and underscore(\_) to uppercase ---------

function toCamelCase(str) {

let arr = str.split('');

for(let i=0;i<arr.length;i++) {

    let letter = arr[i];

    if(letter=='-' || letter=='_'){

      arr[i+1] = arr[i+1].toUpperCase();

      arr[i]=""

    }

}

// arr[0].toUpperCase();

return arr.join('')

}

const result = toCamelCase('Oh_my-god');

console.log(result);

----------throttling simple example ----------------

function throttle(func,delay) {

let lastCall =0;

return function(...args) {

     const now = new Date().getTime();

     if(now-lastCall >=delay){

       func.apply(this,args);

       lastCall=now;

     }

}

}

function myFunction () {

console.log('throttle called')

}

const throttleFunction = throttle(myFunction,2000);

throttleFunction();

throttleFunction();

------------debounce simple example------------

function debounce(func,delay) {

let timeoutId;

return function(...args) {

    clearTimeout(timeoutId);

    setTimeout(()=>{

      func.apply(this,args)

    },delay)

}

}

function myFunction () {

console.log('debounced called')

}

const debouncedFunction = debounce(myFunction,2000);

debouncedFunction();
