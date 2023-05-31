# JavaScript Interview Questions


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
