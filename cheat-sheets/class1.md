Cheat Sheet: Intro to Javascript
--------------------------------

September 20 2016 / Blaine Booher

In the first class, we'll be covering the basics of javascript.

   - Syntax (the structure of the call)
   - The debugger console
   - Embedding javascript in html documents
   - Variables and Constants
   - Math Operators
   - String Operators
   - Functions

Requirements:
   - Text Editor (like SublimeText, Notepad++, Atom, etc.)
   - Google Chrome (or firefox)

Chrome Developer Tools
```
   If you press f12 in chrome (or firefox) you'll see the developer tools
   window. This is an excellent tool for exploring css properties,
   inspecting html objects, looking at network calls, simulating
   mobile devices, and more. What we care about is the 'console'
   window, which is an interactive javascript shell. Use this for
   testing out javascript in real time, debugging, calling functions,
   experimenting with new code, and for viewing console output, 
   such as console.log('hello world');
```

Inline Javascript lives between script tags. Notes:

   - ```<script></script>``` tags
   - semi-colon to separate lines
   - alert and console are simple ways to direct program output
   - multi-line comments: ``` /* */ ```
   - single line comments: ``` // ```

``` javascript
<script>
   alert('hello world!');
   console.log('hello world!'); // go to developer console to see this
   /* this is how you
      can write mult-line
      comments */
</script>
```

Linking to an external script file looks like this:
```
<script src="path/to/file.js"></script>
```

You can use document.write to output directly to the DOM:
``` 
document.write('hello world');
```


Variables look like this:
```
var myVariable; // this variable is not initialized (null value)
var myVariable = 5; // this variable has the value of 5 (integer)
myVariable = 10; // a new value is applied to myVariable

// proper way of doing "block level" scope
let numberOfKittens = 5;  // integer type (whole number)
let cutenessRating = 9.6; // float type (decimal number)

// proper way of making a read-only constant (can't be changed later)
const numberofCats = 5; 
var
 v// how to use a variable (or constant)
alert('I have ' + numberOfKittens + ' kittens!'); 
```

Number (float / integer) operators. Aka math.
```
var numberOfKittens = 5;
var numberOfPuppies = 4;
var totalCutenessMetric = numberOfKittens * cutenessRating; // math

/*
   -a    --> negation
   a * b --> multiply
   a + b --> addition
   a - b --> subtraction
   a / b --> division
   a % b --> modulus (remainder)
 */
```

Escaping apostrophes:
```
   console.log('I\'d more kitties please');
```

String operators
```
   var kittyName = 'Furry';
   var fullName = kittyName + ' McFluffyFace';
   console.log(fullName); // Outputs 'Furry McFluffyFace'

   var otherKittyName = 'Sir Kevin';
   otherKittyName += ' Purs-a-lot';
   console.log('otherKittyName'); // Outputs 'Sir Kevin Purs-a-lot'
```

Functions
```
   function kittyFacts() {
      console.log('Some kittens have extra fully functional toes.');
   }

   // call it three times, just to be sure.
   kittyFacts();
   kittyFacts();
   kittyFacts();
```

Functions: with input values. Aka arguments:
```
   function adoptKitty(kittyName) {
      var fullName = kittyName + ' McAllister';
      console.log('I choose you! Your new name is ' + fullName + '!');
   }
   var kitty = 'Jezabel';
   adoptKitty(kitty); // outputs 'I choose you! Your new name is Jezabel McAllister!'

   function doSomeMath(a, b) {
      // paranthesis help with order of operations
      console.log(2 * (a + b));
   }
   doSomeMath(10, 100); // outputs 220
   doSomeMath(0, 1); // outputs 2

   // return "ends" the function and returns the value for use
   function square(num) {
      return num * num;
   }

   console.log(square(10)); // outputs 100
   // will make howMuchILoveKitties equal 400000000
   var howMuchILoveKitties = square(100) * square (200);
   /* An example of using the output of functions as the input of another
      function call. Output: 100000000 */
   var howMuchIActuallyLoveKitties = square( square(100), square(200));
```