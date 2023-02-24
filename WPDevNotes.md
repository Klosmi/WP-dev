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

`<?php ?>` : When PHP parses a file, it looks for opening and closing tags `<?php and ?>` which tell PHP to start and stop interpreting the code between.

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

- starts with __`$`__ instruction for telling PHP to define a variable.

- The rules for a programming language are called its syntax (like grammer).

- The process of creating a variable is called a variable __declaration__.

- rule of naming: it can only start with letter (no number or other signs). We're allowed to use alphanumeric characters, this includes the underscore character.

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
A parameter refers to the name of the variable.

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

# [Constants](https://www.php.net/manual/en/language.constants.php)
Constants can be reliable for storing data that never needs to change.    
By using a constant, we are always guaranteed the value of a variable never changes.


- Constants are declared with the defined function.

- The defined function has 2 arguments:    
  `define('NAME', 'John');`
  1. name of the variable:
    - all caps (common practice)
    - space not allowed
    - string
  2. value for the variable


After deining a a constant the value never changes
We can read the value of the Constant (we don't need to use the `$` sign)   
```
<?php 
  
define('NAME', 'John');

echo NAME;

// output: John
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>

# [Comments](https://www.php.net/manual/en/language.basic-syntax.comments.php)    
They are a feature for providing notes and documentation in our code.

1. Syntax: single line commnets 
```
// This is a single line comment
```

2. Syntax: block comment: multiple lines of comment
```
/*
This is a multi 
line comment
*/
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>

---

<br>

---
# WP Theme in the perspective of PHP

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Configuration file](https://developer.wordpress.org/apis/wp-config-php/)
it is the `wp-config.php`

- it contains the core settings of WordPress.

- We can find info such as the database, login credentials, security keys, etc.

- Updates not affects the configuration file.

- The default settings are optimized for most WordPress apps.

- Word presses configuration settings are defined with __[constants]()__.

- WordPress disables debugging mode. (It's considered good practice to hide errors in a __production environment__.)

Configure the [WP_DEBUG](https://developer.wordpress.org/apis/wp-config-php/#wp-debug) option to enable debugging while we developing WP.
- in the [documentation](https://developer.wordpress.org/apis/wp-config-php/#wp-debug):
```
define( 'WP_DISABLE_FATAL_ERROR_HANDLER', true );   
define( 'WP_DEBUG', true ); // in production environment it is false
```
In the `wp-config` file we will hav e to add our line to enable deubbing. 
*Lets go to the comment part where it says:*
```
 * For information on other constants that can be used for debugging,
 * visit the documentation.
 *
 * @link https://wordpress.org/support/article/debugging-in-wordpress/
 */

  if ( ! defined( 'WP_DEBUG' ) ) {
    define( 'WP_DEBUG', false );
  }
 ```
 *By setting WP_DEBUG constant to "true", this code is enabling the display of error messages, which can be useful for troubleshooting issues on the site.*
 ```
  if ( ! defined( 'WP_DEBUG' ) ) {
    define( 'WP_DEBUG', true );
  }
 ```
 *Lets deine another error handler for PHP's special type of error called a fatal error. Fatal errors will cause the server to produce a blank page. WordPress has implemented a feature to produce a __friendlier page__ if we have a fatal error.*
```
define('WP_DISABLE_FATAL_ERROR_HANDLER', true);
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Files and Folders of Wordpress](https://www.wpbeginner.com/beginners-guide/beginners-guide-to-wordpress-file-and-directory-structure/)

The files in the root directory contain code for preparing WordPress.     
These files are responsible for delivering the pages on the front side of WordPress.

The files in the root directory are __responsible for loading a page on the browser__.

We have also 3 directories (folders): 
- wp-admin
- wp-content
- wp-includes

## [wp-includes](https://qodeinteractive.com/magazine/wordpress-file-structure/#:~:text=The%20wp%2Dincludes%20folder%20is,your%20website%20to%20function%20properly.)
WordPress defines tons of functions. We can find most of them inside this folder.

The files inside the `wp-includes` folder contains function definitions that WordPress uses to process data.

Many of the files inside this folder can't do anything by themselves (They do not render pages.)

## [wp-admin](https://kinsta.com/knowledgebase/wordpress-admin/#:~:text=The%20WordPress%20admin%20dashboard%2C%20often,%2C%20and%20lots%2C%20lots%20more.)   
This folder contains code for the WordPress admin dashboard. WordPress will separate the code for loading a landing page and the admin dashboard.   

## [wp-content](https://www.elegantthemes.com/blog/tips-tricks/wp-content-a-beginners-guide-to-wordpress-most-important-directory)   
In this direcotory we can find: plugins, themes, and media files.
Not recommended to edit files outside of this directory (because WP may override our changes - except the `wp-config` file).

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [File Headers](https://developer.wordpress.org/themes/basics/main-stylesheet-style-css/)   
File headers are pieces of additional information for describing your theme. (Has information like who is the author of the theme, etc.)

When createing a Theme for WP, first we have to register it with WP.   

WordPress is ultimately frontend agnostic.   
We're not required to use a specific framework.   
We have complete freedom over which libraries are incorporated into our theme.

WordPress has three requirements for registering a new theme. The file names are very important.
1. index.php
2. style.css
3. File Header


First, in the `themes` in `wp-content` we create a folder, to separate our custom theme(s) from the rest of WP's own themes.

__File Header__ must be defined in the `style.css` file. This block comment is the file header, in our `style.css` file.     
So, a file header can be created by adding a block comment in CSS (it has to be on the top of the css file).   

*It's a block comments or information about our theme.*   
*Every piece of information follows a key value format.*   
*The format is the name of the property, followed by the value.*  
*They're separated with a colon.*
```
/*
Theme Name: Twenty Twenty
Theme URI: https://wordpress.org/themes/twentytwenty/
Author: the WordPress team
Author URI: https://wordpress.org/
Description: Our default theme for 2020 is designed to take full advantage of the flexibility of the block editor. Organizations and businesses have the ability to create dynamic landing pages with endless layouts using the group and column blocks. The centered content column and fine-tuned typography also makes it perfect for traditional blogs. Complete editor styles give you a good idea of what your content will look like, even before you publish. You can give your site a personal touch by changing the background colors and the accent color in the Customizer. The colors of all elements on your site are automatically calculated based on the colors you pick, ensuring a high, accessible color contrast for your visitors.
Tags: blog, one-column, custom-background, custom-colors, custom-logo, custom-menu, editor-style, featured-images, footer-widgets, full-width-template, rtl-language-support, sticky-post, theme-options, threaded-comments, translation-ready, block-styles, wide-blocks, accessibility-ready
Version: 1.3
Requires at least: 5.0
Tested up to: 5.4
Requires PHP: 7.0
License: GNU General Public License v2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Text Domain: twentytwenty
This theme, like WordPress, is licensed under the GPL.
Use it to make something cool, have fun, and share what you've learned with others.
*/
```
The most important property is the name of the theme.
```
/*Theme Name: My 1st theme */
```

Now, we can login to our admin Dahboard, and under *Appearance/Themes* we can see our new theme's name  `My 1st theme`

When we visit the site it's empty, because we haven't created a template yet.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>


# [Additional File Headers](https://developer.wordpress.org/themes/functionality/custom-headers/)

in our `style.css` which is in the the *theme* folder, we add the following:    
 - the Name of our theme   
 - the URL of our theme where developers can see or buy it
 - author of the theme
 - Author URI: author's own site
 - Description: desription of the theme
 - Tags: we have the option of uploading our theme to the official repository of themes on WordPress. Tags are words or phrases we can associate with our theme. (Safe to exclude this property)
 - Version: This option should be regularly updated whenever our theme receives updates.
 - Requires: we may want to set this option if our theme requires newer features of WordPress.
 - Tested up to: it lets the user know which version of WordPress the theme was tested on. (Recommended to use the latest WP version) 
 - Reuires PHP: this property should be set to the minimum PHP version required for a theme to be functional.
 - License, License URI: developers use the GNU license, which is the same license used by WordPress.
 - Text domain: it is very important in regards to translations. W e can think of the text domain as a unique ID for our translations. (It's common practice to set the text domain to the same name as our folder.)
 - last, we can add any notes, WP wont check it
```
/*
Theme Name: My 1st theme
Theme UTI: https://example.com
Author: Me
Author URI: https://mysite.com
Description: A simple WP theme.
Tags: example, cool, WP
Version: 1.0
Requires at least: 5.9
Tested up to: 6.0
Reuires PHP: 8.0
License:
License URI:
Text domain: mytheme
*/ 
```
Also, we can se an __image of our theme__, WP search for `screenshot.png` in our theme directory (recommended 1200 x 900 px).

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Full-site Editing](https://developer.wordpress.org/block-editor/getting-started/full-site-editing/) (FSE)

It's difficult to design an interface that allows users to modify elements on a page. So, __page builders__ were introduced into the WordPress ecosystem to solve that problem.   
Such as:     
- [Elementor](https://elementor.com/)
- [Beaver Builder](https://www.wpbeaverbuilder.com/)
- [Oxygen](https://oxygenbuilder.com/)
- [Divi](https://www.elegantthemes.com/gallery/divi/)
- [Visual Composer](https://visualcomposer.com/)   
 

There are downsides of page builders, price, licencig, no standardisation and other limits.

 - __[Gutemberg](https://wordpress.org/gutenberg/)__    
it is WP's own FSE    
Gutenberg development requires knowledge of JavaScript and React.

The main drawback of full site editing is the development experience.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Index Template](https://developer.wordpress.org/themes/getting-started/your-first-theme/#step-3-create-an-index-php-file)
The purpose of the index template is to display content.
Whatever we add on this `index.php` file is displayed on the site.    
   
There are two steps for enabling full site editing.
- 1st step is to create a directory called `templates` in our theme folder.
- 2nd step is to create an `index.html` file inside the `templates` directory

After added the `index.html` WP admin bar at the page appears.    
The `index.php` file is ignored.  

Writing plain HTML into the `index.html` __can break a theme.__ ❗️

FSE does not support plain HTML and it supports blocks.   
__Templates may contain only blocks.__   

<br>

*(If it doesn't work when we click on the `edit` button - we see a blank plage - to solve this, we can add a `theme.json` file to our theme folder. Note that JSON has to contain something, like the name of our theme `{ name: "theme" }` or something like that, because we can not leave it empty (it may give us an error).*

<br> 

__Blocks are written with HTML comments__    
inside a comment we must write the name of the block.  
*Let's add an HTML comment with the following code in to our `index.html` file*    

index.html
```
<!-- wp:site-title /-->
```
The __`/`__ indicates the block is self closing. 

Now we can see, that the FSE has detected that we're using a block called site `title`.    
This block renders the name of our site as a clickable link.   

Building a site involves converting a regular HTML file into blocks.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Recreating the Index Template](https://developer.wordpress.org/themes/template-files-section/page-template-files/)
Continuing the previous chapter, if we check the source of the page (right click and click on View Page Source) we can see that WordPress has returned dozens of tags and classes by using full site editing.
     
This is how WordPress help us with some basic starter content that is required for a fully functioning theme.
    
How is WordPress generating those extra HTML tags?    
This is how WP generate our page:
```
<!DOCTYPE html>
<html <?php language_attributes(); ?>>
<head>
  <meta charset="<?php bloginfo( 'charset' ); ?>" />
  <?php wp_head(); ?>
</head> 

<body <?php body_class(); ?>>
<?php wp_body_open(); ?>

(template)

<?php wp_footer(); ?>
</body>
</html>
```    

<br>

__Let's recreate the base template that surrounds the indexed HTML file.__  

If WordPress can't find an indexed HTML file, it'll fall back to the indexed PHP file. We can verify that by renaming our `index.html` file to smoething else.

<br>

 ### Classic site editing  

<br>

 Let's open the `index.php` file and place this code inside to that file:
 ```
 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  
</body>
</html>
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Language Attribute](https://developer.wordpress.org/reference/functions/language_attributes/)   

The purpose of the language attribute is to help the browser identify the language.   
Also, search engines can correctly index the website and screen readers will be able to pick the correct language profile for reading a site.
```
 <!DOCTYPE html>
<html lang="en">
...
```
- eg.:   
 *Let's change our site to arabic, so it will be read from left to right.*     
 *In the `style` attribute we can add the [languge code](https://www.sitepoint.com/iso-2-letter-language-codes/) and the direction of the text.*    
 *Text will appear on the right side of the sxcreen.*  
 ```
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    :lang(ar) {
      direction: rtl;
    }
  </style>
</head>
<body>
  <h1>Lorem ipsum dolor</h1>
</body>
</html>
 ```
    
In WP As a function grabs the language of the current WordPress installation:      
`language_attributes( string $doctype = 'html' )` 

- eg.:    
*If a site is using French, it will set the language attribute to French.*  
*Replace the `<html lang="ar">` with a PHP function `language_attributes()`.*   
```
<!DOCTYPE html>
<html <?php language_attributes(); ?>>
<head>
...
```
💡 We don't need to define this function, because by registering and activating a theme, WP automatically defines this function for us.


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Character Set](https://developer.wordpress.org/reference/functions/bloginfo/)

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

