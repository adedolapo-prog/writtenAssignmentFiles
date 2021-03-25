## Explain HOF with examples

# Higher Order Functions

Higher order functions are functions that receive another function as an argument and can return the function as an output.
Examples of Higher Order Functions include Map, reduce, filter etc.

    function authenticate (verify) {
        let array = [];
        for (let index = 0; index < verify; index++) {
        array.push(index);
        }
        console.log(array);
        return true;
    }

    function letAccess (person, fn) {
    if (person.level === 'admin') {
        fn(5000);
        } else if (person.level === 'user') {
        fn(10000);
        }
        console.log(person.name);
        return giveAccessTo(person.name);
    }

    function giveAccessTo (name) {
        console.log(`Access granted ${name}`)
    };

    letAccess({name: 'Ade', level:'admin'}, authenticate); //gives us "Access granted, Ade"

# MAP

The map method creates a new array by calling the call back function provided as an argument on every element in the input array.
It takes every returned value from the callback function and creates a new array using those values.

for example:
without using map, we have this block

    const initialArray = [1, 2, 3];
    const newArray = [];

    for (let index = 0; index < initialArray.length; index++) {
    newArray.push(initialArray[index] * 2);
    }

console.log(newArray); //prints out [2, 3, 4];

using map, we have the same result using

    const initialArray = [1, 2, 3];
    const newArray = initialArray.map(function(item) {
    return item * 2;
    })

console.log(newArray) //prints the same [2, 3, 4];
