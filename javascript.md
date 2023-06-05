# JavaScript Interview Questions

## 1) What is Block Scope ?
## 2) What is Functional Scope ?
## 3) What is Global Scope ?
## 4) What is Lexical Scope ?
## 5) What is mean by This Keyword?
## 6) What is mean by new Keyword?
## 7) What is Difference bw Call apply and bind?
## 8) What are closures?
## 9) Difference bw var,let and const?




## 1) What is Block Scope ?
Whenever we declare any variable with let and const it can access to that scope only not another scope 

let and const provide block level scope which means the varibal declare insde { let a=208} is not able to uccused outside of the scope
Example

if(true){
    let a = 10  ----> Block Scope Declaration
    console.log(a) --> (Output will 10)
}

console.log(a) --> (Output gives a refrence error Becouse a is not declare in this scope)

## 2) What is Functional Scope ?
Function Scope is same as the Block scope
Whenever we declare a variabe inside the function the variable functional scope and it cannot access outide of the function 

## 3) What is Global Scope ?
Varibale which can access from any scope is known as global scope
Example 

let a = 208

if(true){
    console.log(a) -->(Output : 208)
}

function call(){
    console.log(a) -->(Output : 208)
}

console.log(a) -->(Output : 208)


## 4) What is Lexical Scope ?
lexical scope provides a predictable and reliable way of managing variable visibility and accessibility based on the hierarchical structure of the source code, enhancing code clarity and maintainability.

## 5) What is mean by This Keyword?
The keyword "this" in programming languages refers to a special variable or context that represents the current object or instance. It is a way to refer to the object on which a method or function is being called or accessed.

The This key word has different scope for different function such that 
the ES5 function the this keyword refers to global Object while ES6 arrow function doesnot have internally this keyword it adapt this keyword from there parent

Example 

let obj = {
    list  : "friend",
    names : ["ironman","thor","cap"],
    display1 : function(){
        console.log(this.names,this.list)
    },
    display2 : function(){
        this.names.map(function(el)=>{
            console.log(this.list ,  el)
        })
    },
    display3: function(){
        this.name.map((el)=>{
            console.log(this.list,el)
        })
    }
}


display1() --> (["ironman","thor","cap"],"friends)

display2() --> (
    undefined  ironman
    undefined thor
    undefined cap
)
 it gives undefined becouse of function scope this keyword does not have any value inmap function

 display3() --> (
    friends  ironman
    friends thor
    friends cap
)
it does not gives any undefined becouse arrow function does not have its own this keyword it inherit from parent function

## 6) What is mean by new Keyword

In programming, the "new" keyword is used to create an instance or object of a class or constructor function. It is commonly used in object-oriented languages such as JavaScript, Java, C++, and C#.

When the "new" keyword is used followed by a constructor function or a class name, it initiates the process of creating a new object based on the definition provided by the constructor or class. This object is often referred to as an instance.

function Person(name, age) {
  this.name = name;
  this.age = age;
}

var john = new Person("John", 25);
console.log(john.name); // Output: John
console.log(john.age); // Output: 25


## 7) What is Difference bw Call apply and bind?

call, apply, and bind are methods in JavaScript that allow you to control the execution context (the value of this) of a function. While they serve a similar purpose, there are some differences between them.

1-> call: The call method is used to invoke a function immediately. It allows you to pass arguments to the function individually. The first argument is the value that will be used as this inside the function, and the subsequent arguments are the function arguments.

2-> apply: The apply method is similar to call, but it accepts arguments as an array or an array-like object. The first argument is still the value of this, and the second argument is an array (or array-like object) containing the function arguments.

3-> bind: The bind method creates a new function with a fixed value for this. It does not invoke the function immediately but returns a new function that you can invoke later. bind also allows you to pre-fill some or all of the arguments of the original function.


Example

function Person(name,age){
    this.name = name
    this.age = age
}

// Using Call Method
function PersonCall(name,age,grade){
    Person.call(this,name,age)
    this.grade = grade
}
let callMethod = new PersonCall("Bruce Wayne",48,"A Class")
console.log(callMethod) 


// Using Apply Method
function PersonApply(name,age,rollNo){
    Person.apply(this,[name,age])
    this.rollNo = rollNo
}

let applyMethod = new PersonApply("Sarim",20,"33")
console.log(applyMethod)

// Using Bind Method

function PersonBind(name,age,classs){
    let result = Person.bind(this,name,age)
    result()
    this.classs = classs
}

let bindMethod = new PersonBind("Sarim",20,"12th")
console.log(bindMethod)

## 8) What are closures?
A closure is a function that retains access to variables from its containing scope even after the outer function has finished executing. It "closes over" these variables, allowing the function to access and manipulate them. Closures are powerful for creating functions with persistent state and private data, and they are commonly used in scenarios involving encapsulation and asynchronous programming.

function outerFunction() {
  var outerVariable = 'Hello';

  function innerFunction() {
    var innerVariable = ' world!';
    console.log(outerVariable + innerVariable);
  }

  return innerFunction;
}

var closure = outerFunction();
closure(); // Output: Hello world!

## 9) Difference bw var,let and const?
var ->  * origin ES2015
        * var has functional or Global scope
        * var has hoisted at the top of execution and initialised as undefined
        * redecleration are allow

Let ->  * origin ES2016
        * let has block scope
        * let has hoisted at the top of execution and left as uninitialised
        * redecleration are allow

const-> * origin ES2016
        * const has block scope
        * const has hoisted at the top of execution and left as uninitialised
        * redecleration are not allow