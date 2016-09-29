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
// Two ways to make a function
function sayHello(name) {
   console.log('hello ' + name);
}
sayHello('blaine');

// assign directly to a variable!
var sayHello = function(name) {
   console.log('hello ' + name);
}
sayHello('blaine');


// An object is a way of storing a collection of properties
var myKitty = {
   name: 'fluffy',             // you can have strings
   age: 12,                    // you can have integers
   healthy: true,              // you can have booleans
   nicknames: [                // you can have arrays
      'smoochie', 
      'darling', 
      'luigi'
   ], 
   birthday: {                 // you can have other objects!
      month: 8,
      day: 30,
      year: 2004
   }, 
   meow: function() {          // you can have functions!
      console.log('meow!');
   },

   eat: function(food) {
      console.log('i am eating ' + food + ' -- thanks!');
   }
}

// interact with the variable using dot notation or key notation
console.log(myKitty.name);
console.log(myKitty['name']);

// call functions, etc.
myKitty.meow()
myKitty.eat('tuna');

// interact with object's internal variables just like anything else
for (let i=0; i<myKitty.nicknames; i++) {
   console.log('Kitty Nickname: ' + myKitty.nicknames[i]);
}
```

When interacting with the DOM (Document Object Model), javascript
gives us tools that do all the work. These tools return objects 
that represent the various html tags, aka nodes.

``` javascript
// <img id="kitten" src="http://placekitten.com/200/300" />
var imgKitten = document.getElementById('kitten');

// now we can interact with it just like an object, including
// updating properties
imgKitten.src = 'http://placekitten.com/200/100';

// or interact with special functions inside the object
imgKitten.setAttribute('src', 'http://placekitten.com/200/100');

// others:
document.getElementsByTagName(name); // returns an array!
document.getElementsByClassName(name); // modern browsers only
document.querySelector(cssQuery); // like 'li.red p'
document.querySelectorAll(cssQuery);

// modify the css directly by hooking into the .style property:
var h1 = document.getElementsByTagName('h1');
h1.style.color = 'blue';

// for css properties with hyphens, like font-family, use the
// 'camelCase' version: lowercase first letter, uppercase second letter
h1.style.fontFamily = 'Helvetica';

// innerHtml is the text in between tags, like <p>This Text Here</p>
h1.innerHtml = 'new title!';
h1.innerHtml += '... and more!';

// create things:
document.createElement(tagName);
document.createTextNode(text);
document.appendChild(myNode);

// add paragraph to the end of the body
var body = document.getElementsByTagName('body')[0];
var paragraph = document.createElement('p');
paragraph.innerHtml = 'This is my text';
body.appendChild(paragraph);
```