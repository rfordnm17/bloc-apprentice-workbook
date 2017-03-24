# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for?
HTML stands for "Hypertext Markup Language" and is used as the foundational means of describing the structure of and content-tags for a webpage.
2. What is the difference between an ID and a class?
A class is used for html items that share traits and characteristics ( like CSS styles) with each other, and can be used more than once. An ID is used to refer to a unique html element that has its own CSS properties/valuse etc. 
3. What does it mean to write "semantic" HTML?
"Semantic" means "with meaning", so semantic html refers to structuring and utilizing html and specific tags in such a way that the tags express meaning as well as presentation and content. This is used to help organize the webpage, and for helps with clarity when someone else may be reading the code.
### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".
<p class="highlight">Watch Out!</p>
2. Write an HTML image tag to show an image called `profile-picture.jpg`.
<img src="profile-picture.jpg">
3. Write a link tag that links to http://google.com.
<a href="http://google.com">Google</a>
5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).
<!DOCTYPE html>
<html>
<head>
</head>
<body>
</body>



</html>


6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
<!DOCTYPE html>
<html>
<head>
</head>
<body>
</body>


<script src="main.js"></script>
</html>
7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
<html>
<head>
<link rel="stylesheet" href="main.css">
</head>
<body>
</body>


<script src="main.js"></script>
</html>
8. Write a numbered list in HTML and list three of your favorite books.

<ol>
  <li>Kingkiller Chronicles</li>
  <li>Selected Speeches of Haile Sellasie</li>
  <li>Ishmael</li>
</ol>

9. Fix the indentation of the following HTML sample:

  ```html
  <div>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for?
CSS stands for "Cascading Style Sheets" and is used to stylize elements in terms of color, size, background, etc. as well as influencing the layout and arrangement of the elements on a webpage.
2. What is the CSS box model?
The CSS box model refers to the idea that all html elements can be considered as boxes, with four corners and four sides, made up first of the content of the element, then padding, then border, then margin between elements. The box model is imperative to consider during the design and layout of a webpage. 
3. What's the difference between margin and padding?
Margin refers to the space between elements, outside of their respective borders. Padding, on the other hand, refers to the internal space between the elements content and border.

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.
h1 { color:red; }
2. Write a CSS rule to make the background color of the link with `class="btn"` blue:
.btn { background-color:blue; }
  ```html
  <a href="#" class="btn">Learn more</a>
  ```

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.
p:first-child {
  font-size:20px;

}

or 

header p {

font-size:20px;

}
  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```

## JavaScript

### Questions

1. What is a function? What are they used for?
A function is a block or line of code that "does something" i.e. calculates a mathmatical value, performs a task, etc. Functions are the foundation of getting programs to do what you want.
2. What is the difference between `==` and `===`?
'==' is a comparitive operator that will try to "help" by using type-coercion between the compared values, so the string "4" == 4 results in "true".
'===' is a comparitive operator that will only return "True" if the compared values are exactly equal AND of the same type.
3. What is the difference between global and local scope variables?
Global variables can be accessed from anywhere on the page or program, whereas local variables "belong" to the function or expression that created them, and cannot be accessed outside of the creating function or expression.
4. What is a boolean value?
"Boolean" values refer to lightswitch-like values (On, Off)(True, False)(0,1) etc.
5. What is an array?
An array is a grouping or list of related data that can be assigned to a single variable. Elements in an array are accessed by their index[i], index starting at [0]; 
### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.
var myName = "Ryan";
2. Write a loop that logs the numbers 1 through 10 to the console.
for (var i = 1; i < 11; i++){

  console.log(i);
}
3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".
if (score > 3 && lives > 0){

  alert("You win!");
}
4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.

function sayHello(name){

  console.log("Hello, " + name + "!");

};
5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  
  ```
  "Friday, Friday".

6. What would the following script log to the console?

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```
  10
7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name " !";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name " !";
  }

  console.log(helloGoodbye("Sarah"));
  ```
  An error, as there is no "+" to concatonate the string in sayHello() or sayGoodbye(). If the functions were correct, We'd get "Hello Sarah!" "Goodbye Sarah!"

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.
function findLongestWord (array) {
  var longestWord = 0;
  for (var i = 0; i < array.length; i++) {
  
    if (array[i].length > longestWord)
    longestWord = array[i].length;
  
  
  }
  
  return longestWord;


};

9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.

function sum(numArray){

var sum = 0;
for (var i =0; i < numArray.length; i++){

  sum += numArray[i];

  }

return sum;
};

10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.

function isVowel(char){
char = char.toUpperCase;
   if (char === "A" || char === "E" || char === "I" || char === "O" || char === "U"){

   return true;
 
 } else {
 
 
   return false;
 
 }


};

11. Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  ```
console.log(pet.speak());


12. Using the same script as above, write the correct line to log the dogs name to the console.

console.log(pet.name)


## Command Line

### Questions

1. What is the command line and what is it used for?
The command line is an efficient user interface for interacting directly with the computer files, directories, etc. It is used in development to quickly access, create, change, etc. necessary elements for a project.
2. What does the command `ls` do?
ls will list all files in current directory.
3. What does the command `pwd` do?
pwd prints the path to the currenty directory
4. What does the following command do: `cd my-cool-project`
takes the user inside the directory named `My-cool-project`.
### Exercises

1. Write the command to make a new directory called "my-cool-project".
mkdir my-cool-project

2. Write the command to create a file called "index.html".
touch index.html
3. Write the command to delete a file called "main.css".
rm main.css
## Git

### Questions

1. What is Git and what is it used for?
Git is a version control tool that allows developers to track specific changes to a project over time. It essentially organizes changes into a retrievable and examinable timeline for editing and collaboration.
2. Whats the difference between a local repository and a remote repository?
A local repository is a repo that is created and altered locally, that is, on the users computer, inside a specific directory. 
A remote repository is a repo stored in the "cloud", like gitHub, that allows users to make collaborative changes to their own local versions of the repository and "push" the changes to the remote repo.

### Exercises

1. Write the command that you would use to create a new local Git repository.
git init
2. Write the command to stage a file called `index.html` to be committed.
git add index.html
3. Write the command to view the current status of the git repository.
git status
