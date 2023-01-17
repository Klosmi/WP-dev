# WP Dev Notes

# Environment
An environment refers to the physical location where your code runs.   
It's a machine installed with software for executing a program.
WordPress needs additional programs to be fully functional.

2 types of environment:
1. __production environment__: (eg.: WordPress sites are hosted by a company with hundreds of servers (nemacheap for eg.))

2. __development environment__: they are only accessible for us, they are private (it can run in our machine).    
It is an environment that allows us to make as many breaking changes as possible.


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