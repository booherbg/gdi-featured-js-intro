Cheat Sheet: Intro to Javascript
--------------------------------

September 27 2016 / Blaine Booher

   - Block vs Global Scope
   - String Comparison (== === != !==)
   - Math Comparison (< <= > >= - == === != !==)
   - Boolean Variables (true, false)
   - Boolean Operators (&& || !)
   - for loops
   - while loops
   - arrays

``` javascript

// Variable Scope
var x = 5; // global scope
let x = 5; // block scope

// math and boolean
// || -- or
// && -- and
// > < >= <= - == === != !== !
var temperature = 50;
var name = 'blaine'
if (temperature < 50 && name == 'blaine') {
   console.log('blaine put on your coat!');
} else if (temperature < 50) {
   console.log('whoever you are, put on your coat')
} else {
   console.log('its warm, go enjoy the outdoors!');
}

// ! is a 'not' operator -- flips true to false, vice versa
var itscold = (temperature < 50);
if (!itscold) {
   console.log('its warm out!');
}

// while loop: countdown from 10 to 5
var i = 10;
while (i > 0) {
   if (i <= 5) {
      break; // breaks out of the loop
   }
   console.log('Count down... ' + i);
   i--; // same as: i = i-1;
}

// for loop
for (let i=0; i<100; i++) {
   if (i % 5 == 0) {
      console.log(i + ' is divisible by 5');
   }

   if (i % 3 == 0) {
      console.log(i + ' is divisible by 3');
   }
}

// arrays
var myArray = ['fruit', 'pizza', 'beer'];
myArray.push('hot sauce');

for (let i=0; i<myArray.length; i++) {
   console.log(myArray[i]);
}
```