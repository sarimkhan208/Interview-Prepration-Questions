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

