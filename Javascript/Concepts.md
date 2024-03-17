1. prototype chain:

prototype - mechanism by which js objects inherit features from on another 

A - it is used to build new types of objects based on existing ones. similar to inheriatnce in a class based language 



2. possible ways to create object in js :
A. 1. object literal :
    - is a comma separated set of name value pair that is wrapped in curly braces.
    var object = {
        name: 'A',
        age: 24
    }

    2. object constructor:
    - Object() - built in constructor function
    var object = Object()

    3. object's create method:
    var object = Object.create(null);

    4. function constructor:
    - example :
    function person (name) {
        this.name = name;
        this.age = 21;
    }
    var object = new person ("A")

    5. function constructor with prototype:
    function person (){}
    person.prototype.name = "A";
    var object = new person();

    6.ES6 class:
    - class person {
        constructor(name){
            this.name = name;
        }
    }
    var object = new person("A");


3. Call, Apply and Bind 
A. Call - invokes a function with given this value and arguments are provided one by one 
Apply - invokes a function with given this value and argumets are parsed in an array format 
Bind - returns a new function, allowing you to pass any no. of arguments


4. JSON  - text based data format, useful for transmit data across a network 
parsing - JSON.parse(text); (converting a string to a native object)
stringification - JSON.stringify(object); (converting object to a string)

5. array slice():
- used to return selected elements in an array 

6. array splice()
- modifies the original array and returns the deleted array 
let arrayIntegersOriginal1 = [1, 2, 3, 4, 5];
let arrayIntegersOriginal2 = [1, 2, 3, 4, 5];
let arrayIntegersOriginal3 = [1, 2, 3, 4, 5];

let arrayIntegers1 = arrayIntegersOriginal1.splice(0, 2); // returns [1, 2]; original array: [3, 4, 5]
let arrayIntegers2 = arrayIntegersOriginal2.splice(3); // returns [4, 5]; original array: [1, 2, 3]
let arrayIntegers3 = arrayIntegersOriginal3.splice(3, 1, "a", "b", "c"); //returns [4]; original array: [1, 2, 3, "a", "b", "c", 5]


7. compare object and map :
both map and object have key and values 
map is preferable in certain cases :
- keys in map are ordered and in on=bject they are not 
- map is iterable directly and object reuires keys to iterate 
- map may perform better in scenarios where frequent addition or removal of key pair happens


8. == vs ===
== checks if they have same value - as it is a non strict operator makes type conversion 
=== checks for both type and value 


9. lambda expressions or arrow functions
- concise syntax for writing fucntion expressions

// Traditional function expression
let add = function(a, b) {
    return a + b;
};

// Arrow function
let add = (a, b) => {
    return a + b;
};
 - do not have their own 'this' context 
 - no arguments object 


10. first class function - it can be assigned a value, can be passed as argument, can be returned by anotehr function 
first order function - does not accept another function as an argument and doesnt return a fucntion as its return value 
high order function - accepts function as an argument , returns function or both 
unary function - accepts exacatly one argument 
currying function - n-ary function turns into a unary funciton
currying is a priocess of taking a fucntion with multiple arguments anf turning it into a sequence of functions each with only single argument 

11. let keyword - 
block scoped local variable 

let vs var 
var - function scope will be hoisted , possibel to re declare the variables in same scope 
let - block scope , hoiseted but not intialised, not possibel to redeclare


12. temporal dead zone :
variable is inaccesible until it has been initialised with a value 
if u use let or const - then this happens 


13. memoization:
- used to inc function's performance by caching previously computed results 


14. Hoisting 
- where variables, function  and classes are moved to the top of their containing scope before code execution

console.log(message); //output : undefined
var message = "The variable Has been hoisted";

var message;
console.log(message);
message = "The variable Has been hoisted";


15. Closures:
closures are powerful because they allow inner functions to access variables from their containing (outer) functions even after those outer functions have finished executing. This allows for data encapsulation and helps in creating modular and maintainable code.