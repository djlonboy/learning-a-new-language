# Learning a New Language

Although there are various approaches to learning a new programming
language, my own personal preference follows four broad steps which can be
broken down as __"the 4 R's"__, as follows:
```
1. Research
2. Read
3. Render (translate)
4. Rewrite (challenges)
```
### Step 1: Research
My first step when approaching a new language is to spend some time familiarising
myself with its structure, history and etymology. To begin with, I try to find
answers to these questions:

* What is the language mostly used for?
* What do developers consider to be its strengths and weaknesses?
* Is it statically or dynamically typed? *(Does it require a compiler? Is the
  language checked at runtime or compile time?)*
* Is it loosely or strongly typed? *(Do you have to define data types specifically?
  How and when are variables defined?)*
* Is the language Procedural, Object-Orientated, or something else?

### Step 2: Read
Once I  have familiarised myself with the general structure of the language, my
next step is to look at some examples of code written in it. A good resource for
this is to look up some questions on StackOverflow, or find some open-source
projects written in the language on GitHub.

Although I may not understand all of the syntax at this point, it's still a good
way of learning about the general layout of the code, and how various objects
within it are notated. It also allows me to get a sense of the "flavour" of the
language: How is it indented? Does it make use of brackets? Are there standard
headers and footers to be observed? How are project folders organised?

### Step 3: Render (translate)
The first two steps, while important, are both passive - they involve spending
time reading and looking at examples. It is well-documented that the best way
to consolidate learning is to practice it oneself. Therefore, steps 3 and 4
are about taking physical action.

In Step 3, I list out some common objects and functions in a language I
already know, and then translate these code snippets into the new language.
Often, this requires looking up specific articles or questions online which deal
with these specific code parts.

Here is an example of a table I made to translate Ruby into JavaScript:

| Name                                | Ruby                                                                             | JavaScript                                                                                                                                                       |
|-------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commenting                          | ```# This is a comment```                                                        | ```// This is a comment```                                                                                                                                       |
| Variable                            | ```my_var = "hello"```                                                           | ```let myVar = "hello";```<br>```[let variables are local scope only]```                                                                                                  |
| Instance Variable                   | ```@my_var = "hello"```                                                          | ```var myVar = "hello";```                                                                                                                                       |
| Global Variable                     | ```@@my_var = "hello"```                                                         | ```var myVar = "hello";```                                                                                                                                       |
| Environment Variable                | ```ENV['MY_VAR'] = "hello"```                                                    | [Several Steps](https://dev.to/deammer/loading-environment-variables-in-js-apps-1p7p)                                                                                                                                              |
| Integer                             | ```my_int = 6```                                                                 | ```No integer, just a floating point number:num myNum = 6;parsInt(myNum);```<br>```[converts number value to integer]```                                                  |
| String                              | ```"Hello world"```                                                              | ```"Hello world";```                                                                                                                                             |
| Convert string to integer           | ```“34”.to_i```                                                                  | ```Number("34");```                                                                                                                                              |
| Convert integer to string           | ```34.to_s```                                                                    | ```num myNum = 34;myNum.toString();```                                                                                                                           |
| String Interpolation                | ```"Hello #{world}"```                                                           | ``` `Hello ${world}`;```<br>```[ES6 onwards. Note use of backticks: ``] ```                                                                                                 |
| Constant                            | ```MY_VAR = 6```                                                                 | ```const MYVAR = 6;```<br>```[case is not essential but standard convention]``` [Constants in constructors not iterated to instances](https://stackoverflow.com/questions/32647215/declaring-static-constants-in-es6-classes)                             |
| Array                               | ```my_array = ["hello”, "world"]```<br>```my_array[0] # => hello```                        | ```var myArray = ["Hello", "world"];```<br>```myArray[0] // => hello```                                                                                                    |
| Hash                                | ```my_hash = [:word1 => "hello", :word2 => "world"] My_hash[:word1] # => hello``` | ```var myHash = { word1: "hello", word2: "world" }; myHash["word1"] // => hello```                                                                                |
| Print to terminal/console           | ```puts "Hello world"```                                                         | ```console.log("Hello world");```                                                                                                                                |
| Input from user (terminal/console)  | ```my_var = gets.chomp```                                                        | ```var myVar = window.prompt("Enter your name: ");[only works in browsers]Use readline...[Only works with node,``` [Requires 'readline' module](https://flaviocopes.com/node-input-from-cli/) ]                   |
| Class                               | ```class My_Class```<br>```end```                                                          | [Not easily defined in classical JS](https://raganwald.com/2013/02/10/prototypes.html)<br>```function MyClass() {}```<br>```MyClass.prototype.myMethod = function(argument) {};```<br>```ES6 onward:class MyClass {}```<br>[Good explanation here](https://manuel.kiessling.net/2012/03/23/object-orientation-and-inheritance-in-javascript-a-comprehensive-explanation/) |
| Initialize Class                    | ```class My_Class```<br>```def initialize(name, date)```<br>```@name = name```<br>```@date = date```<br>```end```<br>```end``` | ```class MyClass { constructor(name, date) {```<br>```this.name = name; this.date = date; ```<br>```} ```<br>```}```<br>```};```                                                                        |
| Instance of Class                   | ```instance = My_Class.new(argument)```                                          | ```const instance = new MyClass(argument);```                                                                                                                    |
| Method / Function (explicit return) | ```def my_method(argument)```<br>```return ...```<br>```end```                                      | ```const myFunction = function(argument) { return ...};```<br>```[full syntax]```                                                                                          |
| Method / Function (implicit return) | ```def my_method(argument) value```<br>```end```                                           | ```const myFunction = () => { value};```<br>```[ES6 arrow function - allows implicit return]```                                                                            |
| Calling a Method / Function         | ```my_class_instance.method```                                                   | ```myClassInstance.function();```                                                                                                                                |
| Predicate Method                    | ```def method?(argument) true```<br>```end```                                              | ```const isFunction = () => { true};```                                                                                                                          |
| Do Loop                             | ```while true do stuff```<br>```end```                                                     | ```do stuff while (true);```                                                                                                                                      |
| If Statement                        | ```if x == y do stuff```<br>```elsif x >= z do other_stuff```<br>```else all_the_other_stuff```<br>```end```   | ```if (x == y) { stuff } else if (x >= z) { otherStuff } else { allTheOtherStuff };```                                                                              |
| If Shorthand                        | ```do_stuff if x == y```                                                         | ```if (x == y) doStuff; (x == y) ? doIfTrue : doIfFalse;```                                                                                                      |


In addition to the obvious benefit of building a cheat-sheet which I can refer
to when writing in the new language, there is another really useful
advantage to this step, which is that it highlights any variations or idioms
which are specific to that language.

As an example, when learning JavaScript for the first time after working in Ruby
for a while, I only became aware of the lack of distinct Classes in JS while
working through the translations in the table above. This allowed me to do more
research in this area and to look at more specific examples of how other developers
tackle this variation.

However, it must be remembered that a translation table is not foolproof. This is
because every language has its own unique idiosyncrasies which are not always
explained properly in little snippets of code. Also, just because code *can* be
written in a directly-translatable manner, this doesn't mean that it *should*.
This is where the final step comes in.

### Step 4: Rewrite Challenges
For the final step, I take the knowledge that I've gained through my research and
rendering of code snippets in the new language, and apply this to some coding
challenges. I like to begin with exercises that I've completed recently, so that
the logic is still fresh in my mind. The idea is not to spend too much time
having to re-think the logic of the challenge, but to focus more on writing the
same logic, but in the new language.

This final step allows further consolidation of the knowledge gained in the
previous steps, but in a 'live' environment where I can actually see the code
in action. Often, code which I think is correct in the translation table actually
turns out not to work in the way that I expected, prompting me to update my
entries there once I've figured out a workaround in real code.

An example of this could be re-writing FizzBuzz in the new language:

__FizzBuzz in Ruby:__
```Ruby

i = 0
output = ""

until i >= 20 do
  i += 1
  output = ""
  divisible = false

  if i % 3 == 0
    output << "Fizz"
    divisible = true
  end
  if i % 5 == 0
    output << "Buzz"
    divisible = true
  end

  if divisible == false
    output = i
  end

  puts output

end
```

__FizzBuzz in JavaScript__
```javascript
function Fizzbuzz() {
};

Fizzbuzz.prototype.fb = function(number) {
  let output = "";
  if (number % 3 == 0) { output = "Fizz" };
  if (number % 5 == 0) { output += "Buzz" };
  if (number % 3 != 0 && number % 5 != 0) { output = number };
  return output;
};

Fizzbuzz.prototype.run = function() {
  var fizzbuzz = new Fizzbuzz();
  let x = 1;
  let fboutput = [];
  do {
    fboutput += Fizzbuzz.fb(x).toString() + " "
    x += 1
  } while (x < 101);
  return fboutput.trim();
};
```
