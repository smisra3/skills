#JS -> High level prog lang, which is interpreted on the runtime and is single threaded.
ES5 vs ES6
Intepreted - Execute code line by line -> done during runtime.

2 Major runtimes for JS -> 1- Browser(chrome, firefox, safari) 2- Node.js(servers) (Bun.js / Deno.js / Winter.JS)

Express is a library which provides web sever to run your app.
Node.js is a JS runtime.

Both Node.js and broswer have a single Common JS Engine (V8) , developed and maintained by google.

function abc(a,b) {
    var a  = c + a;
    return a+b;
}

abc();
 
single threaded -> JS (One)
Multi threaded -> Java, Python, R, C, C++

JS in node.js is capable on handling ~100,000 incoming reqs/ sec (I/O model)
Java server -> 10,000 req/sec

1- Variable declaration

int a = 1;
string b = 'b';

ES -> Ecmascript5 (2014) 
var a = ''
var a = 1;
var a = {}
var a  = []
var a = false;

ES6 -> 2015
const a = 'ua';
a = 'a';

let a = 'um';
a = 'a';

var a = 'um';
a = 'a';

2- Scoping of variables

function add(a, b) {
    var a = a + b + 1;
    if (c > 1) {
        let a = c + a;
        return a;
    }
}
var  -> is function scoped
let -> is block scoped
const -> block scoped

3- Variable hoisting.

function add(a, b) {
    if (a > 1) {
        var a = c + a;
        return a;
    }
}

function add(a, b) {
    var a;
    if (a > 1) {
        a = c + a;
        return a;
    }
}


function add(a, b) {
    console.log(a1);
    if (a > 1) {
        let a1 = b + a;
        return a;
    }
}

function add(a, b) {
    console.log(a1);
    if (a > 1) {
        let a1;
        a1 = b + a;
        return a;
    }
}

4- For loop 

for (let i = 0; i< 10; i+= 1 ) {

}

5- if () {

} else {

}

6- switch case

switch(a) {
    case 'abbc': {
        return '';
    };
    default: return 'default';
}

7- Callbacks -> functions

<button id="primary-button">Click me!!</button>
const button = document.getElementById('primary-button'); // query-selectors sinle elemrnt
                documnet.getElementByClassName('abc') -> array
                documnet.getElementByTagName('div') -> array

button.addEventListener('click', function(event) {
    console.log('Hi !! I am clicked');
})

page is loading your JS
User clicks on the prmiary button ->

8- closures

variables which are present in the runtime memory even after the function in which they are declared are executed / finished

function add(a, b) {
    var c = a + b;
    return c;
}
console.log(c); -> this will give error

function increment() {
    let c = 0;
    return function () {
        let c = 0;
        console.log(c + 1);
    }
}

const val = increment()



