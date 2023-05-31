# JavaScript Interview Questions


## 1) What is Block Scope ?
Whenever we declare any variable with let and const it can access to that scope only not another scope 

Example

if(true){
    let a = 10  ----> Block Scope Declaration
    console.log(a) --> (Output will 10)
}

console.log(a) --> (Output gives a refrence error Becouse a is not declare in this scope)
