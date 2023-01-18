[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>

# Environment
An environment refers to the physical location where your code runs.   
It's a machine installed with software for executing a program.
WordPress needs additional programs to be fully functional.

2 types of environment:
1. __production environment__: (eg.: WordPress sites are hosted by a company with hundreds of servers (nemacheap for eg.))

2. __development environment__: they are only accessible for us, they are private (it can run in our machine).    
It is an environment that allows us to make as many breaking changes as possible.

---

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>

# [PHP](https://www.php.net/manual/en/intro-whatis.php)
PHP: Hypertext Preprocessor   
PHP is a programming language for the web.   
It focuses on web development.

<br>

## [How PHP works](https://www.devopsschool.com/blog/what-is-php-and-how-php-works/)  
PHP can be installed on a server.    
(A server is a computer that provides resources for running programs.)    

We can write PHP code inside a PHP file. The code written inside this file will perform any task we tell it to.

It never runs in the browser, only runs eg. in the server where it is installed PHP.

PHP produces an HTML file, which file is sent to the browser, and the browser will render the HTML file. (That is how the user can see it).

- eg.:   
  *Lets create a Test.php file*     
  *Inside lets wrote a simple htlm `<h1>Hello</1>`*    
  
  Php
  ```
  <h1>Hello</1>
  ```

Whenever we ask for a PHP file, the server will process the code inside the PHP file, and after it executes the code: __the output of a php file is HTML__.    
The HTML file is sent to the browser.    
Browsers will never see a line of PHP code, but it will always receive HTML.    
For this reason, the developer tools categorize the file as an HTML file.    


<br>

__Network Panel__    
  In chrome developer tool the network panel.    
  This panel allows us to view files received by the server: images, videos, CSS and HTML files are some examples of files that can be sent by a server.     

  Network Panel display a table of files.

---

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>


# [PHP Variables](https://www.php.net/manual/en/language.variables.basics.php)

## The `<?php p>` tag     

`<?php ?>` : When PHP parses a file, it looks for opening and closing tags, which are <?php and ?> which tell PHP to start and stop interpreting the code between them.

```
<?php ?>
<h1>Hello World</h1>
```

- We are not allowed to write HTML inside PHP tags (it gives us an error).  

- We can write multiple PHP tags.

- It's optional to close the PHP tag. If were to remove the closing tag, everything would work. Omitting the closing tag is allowed as long as the file ends with PHP code. But, if we put an HTML after, we would get an error.

- Only PHP code is allowed inside a PHP tag.

- A good practice not to include the closing PHP tag if we don't intend to write html after writing PHP.

<br>

## [Variables](https://www.php.net/manual/en/language.variables.basics.php)

- they allow us to store data

- starts with __`$`__" instruction for telling PHP to define a variable.

- The rules for a programming language are called its syntax (like grammer).

- The process of creating a variable is called a variable __declaration__.

- rule of nameing: it can only start with letter (no number or other signs). We're allowed to use alphanumeric characters, this includes the underscore character.

- variables are case sensitive.
  `$age` ang `$AGE` are 2 different variables.


- variabl ends with __`;`__

- assigning a value to the variable woth the `=`   
    ```
    <?php 
    
      $age = 18; 
    ```

- the __`echo`__ keyword: tells our machine to output the value written after it.  
  ```
  <?php 
    
    $age = 18; 
    echo $age;
  ```  

---

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>

# [Strings](https://www.php.net/manual/en/language.types.string.php) and [Booleans](https://www.php.net/manual/en/language.types.boolean.php)

  PHP has a category system for variables. __[data types](https://www.javatpoint.com/php-data-types)__: 

  A data type describes the type of data stored in a variable. Every variable has a data type. (In PHP assigning a data type to a variable is automated by the language.)
  These are:   
  - __intiger__
  - __float__
  - __string__ 
  - __boolean__
  - __array__
  - __object__
  - __null__ *(if a variable doesn't have a value)*


## Strings   
data type for raw text.

- __' ';__ inside single quotes, or __" ";__ inside double quotes we can write text.  
  ```
  $name = 'John Doe';

  // output the variable
  echo $name;

## Boolean
 is a data type where the value is either true or false.
 ```
  $isLoggedIn = true;
  echo $isLoggedIn;

  // output is 1
  ```

---

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>

# [Functions](https://www.simplilearn.com/tutorials/php-tutorial/php-functions)   

A function is a block of code that can perform a specific task to better understand.    

__`function`__ keyword: we use it to define a function

Defining a function:
__function__ + __space__ + __function name__ + __(argument)__ + __{body of the function}__

Invoking a function (calling a function)
__function's name__ + __()__  

```
<?php 
  
  function greeting() {
    echo 'Welcome user!';
  }

  greeting();

// output: Welcome user!
```

<br>

__Parameter__      
is a variable in the declaration of the function.     

Adding parameters to the function: in the parentheses of the function name we can store values passed on to the function.      

These variables can be configured during the functions execution inside the parentheses of the function.   

We can configure the value of a variable (as a parameter) by updating our function calls inside the parentheses.  

```
<?php 
  
  function greeting($message) {
    echo $message;
  }

  greeting('Hello!');
  greeting('Bonjour !');

// output: Hello!Bonjour !
```

__Argument__   
the value of the variable that gets passed to the funtion.


---

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>


# [Arrays](https://www.php.net/manual/en/language.types.array.php#:~:text=An%20array%20in%20PHP%20is,%2C%20queue%2C%20and%20probably%20more.)

What if we need to store multiple pieces of data?   
That's what an array is for.   
Arrays can store an unlimited amount of values.


The array function will return an array.    
__`$var = array('value01', true, 1.25);`__   
Here, `var` variable stores an array, not a copy of the array function.

The value returned by the function will be used as the variables value.

- We're allowed to store as many values and as many type as we'd like.

- Values must be comma separated.

- A shorthand for array's is only using `[]`, no need to write the word array.    
`$var = [1, 2, 3];`

```
<?php 
  
$food = array(
  'pizza', 'hamburger', 'spaghetti'
);

//We can input the index of the item we'd like to grab.

echo $food[1];


// output: hamburger
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>

# [Loops](https://www.tutorialspoint.com/php/php_loop_types.htm#)    
Loops in PHP are used to execute the same block of code a specified number of times.    

## [While loop](https://www.w3schools.com/php/php_looping_while.asp)
Loops through a block of code as long as the specified condition is true.
The basic form:

```
while (condition)
    statement  
```

*Loop through each item in the array.*   
*After the loop has gone through every value, it should stop running first.*    
*We need to keep track of how many times the loop has executed the block of code. → above the loop we create a variable `$count = 0`*  
*Inside the condition we use a `count()` function*    
```
<?php 
  
$food = array(
  'pizza', 'hamburger', 'spaghetti'
);

$count = 0;

while($count < count($food)) {
  // $food start at 0
  echo $food[$count];
  //update +1
  $count = $count + 1; // $count++
}

// output: pizza hamburger spaghetti
```


## [Comparison operators](https://www.php.net/manual/en/language.operators.comparison.php)
comparison operators compare two values.

- **$a == $b**	Equal	true if $a is equal to $b after type juggling. 
- **$a === $b**	Identical	true if $a is equal to $b, and they are of the same type. 
-**$a != $b**	Not equal	true if $a is not equal to $b after type juggling.
- **$a <> $b**	Not equal	true if $a is not equal to $b after type juggling.
- **$a !== $b**	Not identical	true if $a is not equal to $b, or they are not of the same type.
- **$a < $b**	Less than	true if $a is strictly less than $b.
- **$a > $b**	Greater than	true if $a is strictly greater than $b.
- **$a <= $b**	Less than or equal to	true if $a is less than or equal to $b.
- **$a >= $b**	Greater than or equal to	true if $a is greater than or equal to $b.
- **$a <=> $b**	Spaceship	An int less than, equal to, or greater than zero when $a is less than, equal to, or greater than $b, respectively.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>
