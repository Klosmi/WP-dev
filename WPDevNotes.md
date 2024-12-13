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

# [Return values from within a function](https://www.php.net/manual/en/functions.returning-values.php)   
Our `test.php` file, which is to experiment with php, we create a function to add 2 values.   
We're adding the values, but they're not accessible outside the function → therefore we are using the `return` keyword. The value written after it will be returned by the function, thus allowing it to be accessible.
```
<?php
  // add 2 numbers
  function sum($a, $b) {
  return $a + $b;
  }
```
We create a variable `$total`. It is the sum of the 2 numbers in our function.
```
<?php
  // add 2 numbers
  function sum($a, $b) {
  return $a + $b;
  }

  $total = sum(5, 5);
  echo $total;
```
If we add something after the `return` it will never going to be executed, because PHP will cease execution after the value has been returned.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-dev)

<br>

<br>

<br>

---
# WP Theme in the perspective of PHP

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-theme-development-with-php)

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
In the `wp-config` file we will have to add our line to enable debugging. 
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
 *Lets define another error handler for PHP's special type of error called a __fatal error__* ❗️    
 *Fatal errors will cause the server to produce a blank page. WordPress has implemented a feature to produce a __friendlier page__ if we have a fatal error.*
```
define('WP_DISABLE_FATAL_ERROR_HANDLER', true);
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-theme-development-with-php)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-theme-development-with-php)

<br>

# [File Headers](https://developer.wordpress.org/themes/basics/main-stylesheet-style-css/)   
File headers are pieces of additional information for describing your theme. (It has information like who is the author of the theme, etc.)

When creating a Theme for WP, first we have to register it with WP.   

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

Now, we can login to our admin dashboard, and under *Appearance/Themes* we can see our new theme's name  `My 1st theme`

When we visit the site it's empty, because we haven't created a template yet.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-theme-development-with-php)

<br>


# [Additional File Headers](https://developer.wordpress.org/themes/functionality/custom-headers/)

in our `style.css` which is in the *theme* folder, we add the following:    
 - the Name of our theme   
 - the URL of our theme where developers can see or buy it
 - author of the theme
 - Author URI: author's own site
 - Description: desription of the theme
 - Tags: we have the option of uploading our theme to the official repository of themes on WordPress. Tags are words or phrases we can associate with our theme. (Safe to exclude this property)
 - Version: This option should be regularly updated whenever our theme receives updates.
 - Requires: we may want to set this option if our theme requires newer features of WordPress.
 - Tested up to: it lets the user know which version of WordPress the theme was tested on. (Recommended to use the latest WP version) 
 - Requires PHP: this property should be set to the minimum PHP version required for a theme to be functional.
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
Also, we can set an __image of our theme__, WP search for `screenshot.png` in our theme directory (recommended 1200 x 900 px).

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-theme-development-with-php)

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

 - __[Gutenberg](https://wordpress.org/gutenberg/)__    
it is WP's own FSE    
WordPress's Full Site Editing (FSE) using Gutenberg requires JavaScript and React expertise, making development complex. <br> 
A key drawback is the editing experience: block editors must provide a UI for content editing, leading to elements appearing differently in edit mode compared to the front end. <br>
Another issue is that custom HTML often differs from Gutenberg's generated HTML. <br> For example, unordered lists in regular HTML can end up as multiple `<div>` tags when WordPress processes them, plus WordPress adds its own CSS. These differences can make our custom CSS not work as expected. The fix? Add extra CSS specifically for the editor so we can get the look we want.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-theme-development-with-php)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-theme-development-with-php)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#wp-theme-development-with-php)

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
 *Let's change our site to arabic, so it will be read from right to left.*     
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
    
In WP the following function grabs the language of the current WordPress installation:      
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

WP stores the character set for a site in its database.
The character set should be dynamic.   

WP's function `bloginfo()` can retrieve data from the database.

<br>
 
In the [documentation](https://developer.wordpress.org/reference/functions/bloginfo/) the [parameters section](https://developer.wordpress.org/reference/functions/bloginfo/#parameters) provides a __list of values we can pass into a function__.   
 
- The `show` : parameter allows us to specify the type of value to display on the page.

- [Values](https://developer.wordpress.org/reference/functions/bloginfo/#possible-values-for-show) for the `show` parameter:

  - `charset` : displays the “Encoding for pages and feeds” set in Settings > Reading. This data is retrieved from the “blog_charset” record in the wp_options table. 

  eg.:  
  *We write the `bloginfo()` function inside the character set attribute, in the meta tag (`<meta charset="UTF-8">`).
).*   
  ```
  !DOCTYPE html>
  <html lang="ar">
  <head>
    <meta charset= <?php bloginfo('charset'); ?>>
  ```
  We can check in the developer tool: the character set has been correctly configured (`<meta charset="UTF-8">`).


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Additional tags](https://developer.wordpress.org/themes/basics/template-tags/#what-is-a-template-tag)

The WP core and third party plugins may want to add meta tags, load style sheets and load scripts.

By default WP does not inject tags into our template. Therefore, we need to provide a location for safely loading additional tags.

<br>

### adding the [header](https://developer.wordpress.org/reference/functions/wp_head/)   
The `wp_head()` function allows WP and plugins to load tags into the `<head>` section of our documents.   

Good practice to add the `wp_head()` function after adding your own tags. 

In most cases, developers call the `wp_head()` function at the end of the `<head>` tag.

```
<head>
  <meta charset= <?php bloginfo('charset'); ?>>
  <?php wp_head(); ?>
</head>
```

<br>

### adding [scripts](https://developer.wordpress.org/reference/functions/wp_footer/)

WP does not automatically inject scripts into our documents.    
We need to provide a location for loading scripts before the closing body tag.

The `wp_footer()` allows plugins to begin loading scripts into the documents.

```
<body>
  <h1>Lorem ipsum dolor</h1>

  <?php wp_footer(); ?>
</body>
```

<br>

After loading our page we can see in the dev.tool/elements that WP has injected several tags into the head and body sections of our document, which is great.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Body tag]()
 A helpful feature is generating a set of classes for the body tag.  
 Useful for styling pages. 


On the `<body>` tag lets place the `body_class()`function.

In some cases, we may want to add classes to the body tag. The `body_class()` function has an optional parameter, which is a list of classes. (These classes  added alongside the classes generated by WP)

```
<body <?php body_class(); ?>>
  <h1>Lorem ipsum dolor</h1>

  <?php wp_footer(); ?>
</body>
```
*Lets give a random class name, like `'exampleclass'` into the `body_class()` function as a parameter.*
```
<body <?php body_class('exampleclass'); ?>>
  <h1>Lorem ipsum dolor</h1>
...
```
Our `exampleclass` has been added.    

When we run the page we can see under the elements panel, that the body tag contains a series of classes.   
They are not random classes!  
These classes tell us information about the page and user.   
- eg.:   
  *We can see a class called `admin-bar`, which only appears if the current user is an administrator.*   
  *`home` class, if the user is viewing the home page.*
```
<body class="home blog logged-in admin-bar exampleclass customize-support">
```

When we are viewing a post, the classes are different: a `singl-post` class is added.
```
<body class="post-template-default single single-post postid-1 single-format-standard logged-in admin-bar exampleclass customize-support">
```

<br>

There are 2 functions for injecting tags into the body tag.  
  - the `wp_footer()` : it allows plugins to load content at the bottom of the document.
  - __`wp_body_open()`__ : it allows plugins to load content at the beginning of the document.  
  ```
  <body <?php body_class('exampleclass'); ?>>
  <?php wp_body_open(); ?>
  ```

  <br>

Here is the complete template: 
```
<!DOCTYPE html>
<html <?php language_attributes(); ?>>
<head>
  <meta charset= <?php bloginfo('charset'); ?>>
  <?php wp_head(); ?>
</head>
<body <?php body_class('exampleclass'); ?>>
  <?php wp_body_open(); ?>
  
  <h1>Lorem ipsum dolor</h1>

  <?php wp_footer(); ?>
</body>
</html>
```

<br>

If we add the `index.html` file into our templates folder, WP switches back to full site editing behind the scenes.

The `index.php` file however, for our themes should always be empty.


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Documentation and sources](https://developer.wordpress.org/)

- The [developer docs of wordpress](https://developer.wordpress.org/)
- The [official WP site](https://wordpress.org/) (.org)
- The [WP hosting platform](https://wordpress.com/) (.com)
- [Codex](https://codex.wordpress.org/Main_Page), old dev. docs, it's not updated 
- [automattic](https://automattic.com/): they run wordpress.org, contribution to WP

## [Best practices coding standards](https://developer.wordpress.org/coding-standards/)
To develop WP is recommended to follow the WP coding guidelines and standards.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>



# [Global Styles](https://make.wordpress.org/design/handbook/focuses/global-styles/)
It allows users to modify a site styles on a global level.

Go to dashboard/themes/editor   
Our site appears in editor mode. On the up right corner click on the "Styles" button.    
A side bar appears. In the side bar we can modify things of our site's appearance.   

- eg.:     
Change the background color to blue. The changes apply in a global level, meaning that every page in our website will have blue background.   
We can also fine tune our changes to specific blocks: eg. all paragraph blocks' background will change to pink (selecting on the side bar we click on blocks/background/color/pink). 

<br>

### The [`theme.json`](https://developer.wordpress.org/block-editor/how-to-guides/themes/theme-json/)   

We can extend the global styles with a single file, to configure the editor that enables a finer-grained control and managing styles.

In our editor, inside our themes folder, we are create a file called __`theme.json`.__    
We can configure the editor by adding colors, fonts, spacing rules, etc.   
(*The name of our file is very important, because WP is looks at the specific file name in our `themes` root directory. When WP finds this file, the settings from this file will be applied to the full site editor.*)    

If we change our templates in the Editor (so not in the `theme.json`), the copy in the database will have priority over the original).    
If we don't like the change, we can revert: in the middle of our site (in editor mode), we can click on the name of our page (eg. index)click to "Clear Customization".

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

## [JSON Schema](https://make.wordpress.org/themes/2021/11/30/theme-json-schema/)   
JSON Schema is a content specification language used for validating the structure of a JSON data.       
It helps us specify the objects and what values are valid inside the object’s properties. [JSON schema](https://www.geeksforgeeks.org/json-schema/) is useful in offering __clear, human-readable, and machine-readable documentation__.

<br> 

Apply a schema into our JSON. It can double check our file to avoid mistakes.   
[WP docs give us an example](https://developer.wordpress.org/block-editor/how-to-guides/themes/theme-json/#developing-with-theme-json) by using `"https://schemas.wp.org/trunk/theme.json"`    
If this doesn't work, we can use the original source:   
`"https://raw.githubusercontent.com/WordPress/gutenberg/trunk/schemas/json/theme.json"`
```
{
"$schema" : "https://schemas.wp.org/trunk/theme.json"
}
```

<br>

In our editor, inside our themes folder, open the __`theme.json`.__ 
The first property in your themed JSON file should always be version, so lets add it (backward compatibility reasons).
*(We are using double quotes, single quotes in json causes error)*   
```
{
  "$schema" : "https://schemas.wp.org/trunk/theme.json",
  "version" : 2
}
```

Mistakes go unnoticed(eg. using capital letter), that is why we use schemas. 
A schema is available to help us address these issues, and it is not specific for WP.  
Here is [the docs for the schema](https://developer.wordpress.org/block-editor/how-to-guides/themes/theme-json/#developing-with-theme-json).

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>  

## [Changing WP default settings](https://fullsiteediting.com/lessons/theme-json-color-options/#h-what-color-values-can-you-use-in-theme-json) eg. the color palette
[adding color to the defalult palette](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#adding-color-to-the-defalult-palette)   
[color palette or css properties](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#color-palette-or-css-properties)        
[custom colors](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#custom-colors)      
[duotone colors](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#duotone-colors)      
[gradient colors](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#gradient-colors)     
[applying colors](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#applying-colors)    
[border colors](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#border-colors)

<br>

Resources to check out for the `theme.json`'s settings:
- [beginners guide to the `theme.json`](https://developer.wordpress.org/block-editor/how-to-guides/themes/theme-json/)
- [less beginner friendly (list of all availabel options)](https://developer.wordpress.org/block-editor/reference-guides/theme-json-reference/theme-json-living/)

So, with the `theme.json` file we can modify, change WP default color palette.
```
{
  "$schema" : "https://schemas.wp.org/trunk/theme.json",
  "version" : 2,
  "settings" : {
    "color" : {
      "defaultPalette" : true
    }
  }
}
```

By default, "defauletPalette" property is set to true. Setting this property to true will allow WordPress to recommend colors. Lets chang it to false.
```
{
  "$schema" : "https://schemas.wp.org/trunk/theme.json",
  "version" : 2,
  "settings" : {
    "color" : {
      "defaultPalette" : false
    }
  }
}
```

<br>

Let's try __enabling the default palette for the site's title block__ in the `theme.json` file. So when we click on the color palette when the `<h1>Site title</h1>` is selected, we can see the default color palette.    
We use a prtoperty `"blocks"` which value is an object, and it can apply settings to specific blocks.   

List of names for the `blocks` property are [here](https://www.udemy.com/course/wordpress-development-create-wordpress-themes-and-plugins/learn/lecture/32593150#notes).
```
{
  "$schema" : "https://schemas.wp.org/trunk/theme.json",
  "version" : 2,
  "settings" : {
    "color" : {
      "defaultPalette" : false
    },
    "blocks": {
      "core/site-title" : {
        "color" : {
          "defaultPalette" : true
        }
      }
    }
  }
}
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### [Adding color to the defalult palette](https://developer.wordpress.org/themes/advanced-topics/theme-json/)   

Lets add a pinkish color.   
We add a property called `palette` with an initial value of an empty array `[]`. Inside that array we can insert objects for the colors we want.    
Each obejct has 3 properties:    
 - "slug" : is an ID for our theme    
 - "color" :  can Hex, RGB, RGBA, Color Names (red, blue, etc.), Keywords (transparent, currentColor), HSL, HSLA
 - name: this property is a human readable name of our colour (what the user can read)


```
{
  "$schema" : "https://schemas.wp.org/trunk/theme.json",
  "version" : 2,
  "settings" : {
    "color" : {
      "defaultPalette" : false,
      "palette": [
        {
          "slug": "a-pink",
          "color": "#FFC0CB",
          "name": "Pinkish"
      }, 
      {
          "slug": "m-gray-100",
          "color": "rgb(243 244 246)",
          "name": "Grayish 100"
        },  
      ]
    },
    "blocks": {
      "core/site-title" : {
        "color" : {
          "defaultPalette" : true
        }
      }
    }
  }
}
```

We can add custom __colors to a specific block__.   
Inside the `"block"` we add the `"palette"` property.

```
{
  "$schema" : "https://schemas.wp.org/trunk/theme.json",
  "version" : 2,
  "settings" : {
    "color" : {
      "defaultPalette" : false,
      "palette": [
        {
          "slug": "a-pink",
          "color": "#FFC0CB",
          "name": "Pinkish"
      }, 
      {
          "slug": "m-gray-100",
          "color": "rgb(243 244 246)",
          "name": "Grayish 100"
        },  
      ]
    },
    "blocks": {
      "core/site-title" : {
        "color" : {
          "defaultPalette" : true,
          "palette" : [
            {
              "slug" : "m-primary", "color": "#ef4444", "name" : "My-Primary"
            }
          ]
        }
      }
    }
  }
}
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### Color palette or CSS properties

WP allows us to toggle the palette for backgrounds, text and links, these settings can be modified on a global level or block level.   

We can modify the colour of the background, text, links, by adding 
```
"color" : {
      "background" : true,
      "text" : true,
      "link" : true
}
```
The background and text properties are enabled, lets disable the link for the global setting.   
For the block setting make the link property available by setting it true in the `"block"` section:

```
{
  "$schema" : "https://schemas.wp.org/trunk/theme.json",
  "version" : 2,
  "settings" : {
    "color" : {
      "defaultPalette" : false,
      "palette": [
        {
          "slug": "a-pink",
          "color": "#FFC0CB",
          "name": "Pinkish"
      }, 
      {
          "slug": "m-gray-100",
          "color": "rgb(243 244 246)",
          "name": "Grayish 100"
        },  
      ],
 ►    "background" : true,
 ►    "text" : true,
 ►    "link" : false
    },
    "blocks": {
      "core/site-title" : {
        "color" : {
          "defaultPalette" : true,
          "palette" : [
            {
              "slug" : "m-primary", "color": "#ef4444", "name" : "My-Primary"
            }
          ],
 ▶︎        "link" : true
        }
      }
    }
  }
}
```   
Setting the background and text properties to true is overkill for our theme.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### Custom colors

Users are not forced to use our recommended colors if they would like, so they can select a custom color.       
__We can disable the color picker on a global level or block level__.

Adding the  `"custom" : false` to the `"color"` object can disable the color picker.

```
...
  "palette": [
      {
        "slug": "a-pink",
        "color": "#FFC0CB",
        "name": "Pinkish"
    }, 
    {
        "slug": "m-gray-100",
        "color": "rgb(243 244 246)",
        "name": "Grayish 100"
      },  
    ],
    "background" : true,
    "text" : true,
    "link" : false,
  ▶︎ "custom": false
  },
...
```
--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### [Duotone colors](https://fullsiteediting.com/lessons/theme-json-color-options/#h-how-to-add-duotone-colors)   

A duotone is a filter that can be applied to images or videos, the filter applies 2 colors.    
A duotone filter will completely override the colors of an image.

Inside the color object, we add a property called `"duotone" : [ ]`. Its value will be an array.   
This format for adding a duotone is similar to registering a colour (slug, __color__, name).

The "color" property has an array, because duotones are created with 2 colors: shadow and highlight (the order is important).

● shadow:   
represents the dark color and the    
● highlight: represents the lighter color

Only Hex and RGB values are accepted.
```
...
 "duotone": [
				{
					"colors": [ "#cc1871", "#f9449e" ],
					"slug": "pink-and-light-pink",
					"name": "Pink and light pink"
				}
			]
...
```
Add duotone for a single block
```
...
"blocks": {
      "core/site-title": {
        "color": {
          "defaultPalette": true,
          "palette" : [
            {
              "slug" : "m-primary", "color": "#ef4444", "name" : "My-Primary"
            }
          ],
          "link" : true,
 ►        "core/cover" : {
            "color" : {
              "duotone":[],
              "customDuotone": false
            }
          }
        }
      }
    }
  }
...
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### [Gradient colors](https://fullsiteediting.com/lessons/theme-json-color-options/#h-gradients) 

If a user has gradients and switches themes, the original gradients will survive from older themes.   

- hide default gradients      
  theme.json
  ```
  ...
  "color" : {
    "defaultGradients": false
  }
  ```   
- adding cutom set of gradients (here in global level)
  theme.json
  ```
    "color" : {
       "gradients": [
        {
          "slug" : "winter",
          "name" : "Winter",
          "gradient" : "linear-gradient(#a8ff78, #78ffd6)" 
        }
      ]
    }
  ```
  - disabeling gradients completely for the block.   
  By adding an empty array WP doesn't present the user with a set of gradients to select from.  
  ```
      "blocks": {
      "core/site-title": {
        "color": {
          "gradients": []
        }
      }
    }
  ```
  - disabeling the custom colour picker by adding the custom gradient property with a value of false.
  ```
        "blocks": {
      "core/site-title": {
        "color": {
          "gradients": [],
          "customGradient": false
        }
      }
    }
  ```
--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

  ### [Applying colors](https://fullsiteediting.com/lessons/theme-json-color-options/#h-applying-colors-with-theme-json)   
  Here are some practical examples of applying colors in the styles section of `theme.json`.

  Add the `styles` property at the root level of the object.   
  `"syles"` property is an object of styles that we can apply to our theme. This option gives us the opportunity to configure the styles, values for different elements and blocks.   
  theme.json
  ```
  {
    "$schema": "https://schemas.wp.org/trunk/theme.json",
    "version" : 2,
    "settings" : {...},
    "styles" : {
    }
  }
  ```

  - changing the Text color of the theme   
    theme.json  
    ```
    "styles": {
      "color" : {
          "text": "rgb(55 65 81)"
      } 
    }
    ```
    Let's try __using a variable__ since this color already exists as a variable under the `"color" / "palette"`

    In the developer tools by clickong on the `<body class = "...">`
    we can see all the colors added to WordPress as list of variables.   All variables are prefixed with the WP preset colour keyword.   
    Let's pick one color from the list, and copy the entire variable name `--wp--preset--color--my-gray-400`   
    *Replace the hardcoded value for the text color with our variable, the variable should be wrapped with the var function.*   
    theme.json
    ```
    "styles": {
      "color" : {
          "text": "var(--wp--preset--color--my-gray-400)"
      } 
    }
    ```
    Let's change the __background color__      
    theme.json
    ```
    "styles": {
      "color" : {
          "text": "var(--wp--preset--color--my-gray-400)",
          "background" : "var(--wp--preset--color--pale-gray-100)"
      } 
    }
    ```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### [Border colors](https://fullsiteediting.com/lessons/theme-json-color-options/#h-border-color)

Most blocs support borders by default.   

Configuring borders is slightly different from other settings.

We have to enable borders through the `"settings"` object. Inside this object, we can add an object called `"border"`.   
A border has a style, width, colour, radius.   

- If we want to enable border settings for a specific block, we must do it from the `"settings"` object.    
	theme.json
	```
	"version": 2,
		"settings": {
			"border": {
	      "color" : true,
	      "radius" : true,
	      "style" :  true,
	      "width" : true
	     }
	  },
	```
The value for these properties is booleans, by default, they're all false.

- let's modify the border settings for the pull quote block.   
We add our object to the `"blocks"` object with the name `" core/pullquote"`. Here we can add the styling.       
	theme.json
	```
	 "version": 2,
	 "settings": {
	    "border": {
		"customColor": true,
		"customRadius": true,
		"customStyle": true,
		"customWidth": true
		}
	   },
	   "styles": {
		"blocks": {
		 "core/pullquote":{
		      "border": {
			  "width": "4px",
			  "radius": "10px",
			   "style": "dotted",
			   "color": "var(--wp--preset--color--vivid-purple)"
		       }
		  }
	       }
	    }
	```
 The border settings are freely modifiable from the sidebar in the editor by enabling all border settings. Users can modify the width, color, style and radius of a border.


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>


 ## [WP Typography - font settings](https://fullsiteediting.com/lessons/theme-json-typography-options/)    
 The `theme.JSON` file does not provide an option for loading fonts.
 
- [font sizes](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#font-size)    
- [line height, drop cap, font weight, font style, text transformation, text decoration](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#line-height--drop-cap-font-weight-font-style-text-transformation-text-decoration)  
- [applying typography styles](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#applying-typography-styles)  


 Let's add font family in the global level. First, we add `"typography"` object inside the `"settings"` object. Inside the `"typography"` object we add `"fonFamilies"` which has an array, where can add our custom fonts.    
	theme.json
```
 ...
    "settings": {
      "typography": {
	"fontFamilies": [
	{ 
	  "fontFamily" : "Rubik, sans-serif", 
	  "slug": "my-rubik",
	  "name": "My Rubik" 
	}
	]
      }
    }
  ...
```
Let's add a font family in the object specific level.   
Inside the `"blocks"` object we place the `"typography"` object.     
theme.json
```
  ...
    "blocks": {
      "typography": {
	"fontFamilies": [
	{ 
	  "fontFamily" : "Lato, sans-serif", 
	  "slug": "my-Lato",
	  "name": "My Lato" 
	}
	]
      }
    }
  ...
```
  (* We haven't loaded the font into our theme, so it won't change at the moment.*)
  
--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### [Font Size](https://fullsiteediting.com/lessons/theme-json-typography-options/#h-font-size)
  
Font sizes can be recommended on a global level or block specific level.

- __global level :__        
`"settings"` __>__ `"typography"` __>__ `"fontSizes"`    
  theme.json
  ```
  "settings": {
      "typography": {
        "fontSizes": [
          {"slug" : "small", "size" : "0.75rem", "name" : "Small"},
          {"slug" : "medium", "size" : "1.25rem", "name" : "Medium"},
          {"slug" : "large", "size" : "2.25rem", "name" : "Large"},
          {"slug" : "x-large", "size" : "3rem", "name" : "X-Large"},
          {"slug" : "gigantic", "size" : "3.25rem", "name" : "Gigantic"}
        ]
      }
  ```

  - __block level :__    
    `"blocks"` __>__ "`core/preformatted"` __>__ `"typography"` __>__ "`fontSizes"`    
    theme.json
    ```
    "blocks" : {
    "core/preformatted" : {
            "typography" : {
              "fontSizes" : [],
              "customFontSizes"  : false
            }
          }
    }
    ```
    By setting the `"customFontSizes"` property to `false` the option to configure a custom font size will be hidden (so users won't be able to configure custom fontsizes).


 WordPress community strongly encourages developers to override the font sizes for WordPress existing variables.    
- --wp--preset--font-size--small:  13px;   
- --wp--preset--font-size--medium: 20px;   
- --wp--preset--font-size--large:  36px;   
- --wp--preset--font-size--x-large: 42px;     

*Useful resource is the: [about the font size topic](https://richtabor.com/standardizing-theme-json-font-sizes/)*

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### [Line height](https://fullsiteediting.com/lessons/theme-json-typography-font-styles/#h-line-height) , [drop cap](https://fullsiteediting.com/lessons/theme-json-typography-font-styles/#h-drop-cap), [font weight](https://fullsiteediting.com/lessons/theme-json-typography-font-styles/#h-font-weight), [font style](https://fullsiteediting.com/lessons/theme-json-typography-font-styles/#h-font-style), [text transformation](https://fullsiteediting.com/lessons/theme-json-typography-font-styles/#h-text-transform), [text decoration](https://fullsiteediting.com/lessons/theme-json-typography-font-styles/#h-text-decoration)
By default customizing the line height is disabled, let's enable it by setting it to true. Under `"typography"` add `"lineHieght"`
```
"typography" {
     "lineHeight": true
    }
``` 
The `"dropCap"` property will enable the option of enlarging the first letter of a paragraph.   
```
"typography" {
     "lineHeight" : true,
     "dropCap" : true
    }
``` 
We can enable the `"fontWeight"` option by setting it to true.
```
"typography" {
     "lineHeight": true,
     "dropCap": true,
     "fontWeight" : true
    }
``` 
The `"fontStyle"` property allows users to add italic text, enable it by setting it to true.
```
"typography" {
     "lineHeight" : true,
     "dropCap" : true,
     "fontWeight" : true,
     "fontStyle" : true
    }
```
The `"textTransform"` property changes text casing such as uppercase, lowercase or capitalization.
```
"typography" {
     "lineHeight" : true,
     "dropCap" : true,
     "fontWeight" : true,
     "fontStyle" : true,
     "textTransform" : true
    }
```
The spacing between letters can be enabled by setting the `"letterSpacing"` property to true.
```
"typography" {
     "lineHeight" : true,
     "dropCap" : true,
     "fontWeight" : true,
     "fontStyle" : true,
     "textTransform" : true,
     "letterSpacing" : true
    }
```
The underlines and strike through can be enabled by adding the `"textDecoration"` property with a value of true.
```
"typography" {
     "lineHeight" : true,
     "dropCap" : true,
     "fontWeight" : true,
     "fontStyle" : true,
     "textTransform" : true,
     "letterSpacing" : true,
     "textDecoration" : true
    }
```
These settings can be modified on a block level too.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

### [Applying typography styles](https://fullsiteediting.com/lessons/theme-json-typography-font-styles/#h-applying-typography-styles-with-theme-json)  

We can apply styles on a global level or block level.    
Good practice to establish default values for our theme.

Inside the `"styles"` object we can add the typography style by adding the `"typography"` object.      

We can modify the font family, size, style, wight, line-height, text decoration, text transformation.
```
"styles" : {
  "typography" : {
     "fontFamily" : "var(--wp--preset-font-family--u--rubik)",
     "fontSize" : "16px",
     "fontStyle" : "normal",
     "fontWeight" : "normal",
     "lineHeight" : "inherit",
     "textDecoration" : "none",
     "textTransform" : "none"
  }
}
```
Let's configure the site title block to use our custom font as the default font family.   
Inside the `"blocks"` section, we update the `"core/site-title"` object and the `"typography"` object to the block.
```
"blocks" : {
  "corse/site-title" : {
     "typography" : {
          "fontFamily" : "var(--wp--preset--font--family--u-pacifico)"
      }
  }
}
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>


## [Content width](https://fullsiteediting.com/lessons/theme-json-layout-and-spacing-options/#h-how-to-set-content-width-using-theme-json)  

When we want our post's width to be fixed, we can use 
WP's options for changing the width of the content.  

WordPress provides theme developers with 2 options for changing the width of the content. These settings apply to posts, but not the full site editor.

But we want the full site editor to have complete control of the editor, not a portion.     

<br>

__content width__ refers to the width of the main content area, while __wide width__ refers to the maximum width of wider elements on your website.    

We can provide layout settings by using the `"layout"` object in the `"settings"`.    
  - `"contentSize"` property configures the __default width for all blocks.__    
  (Instead of having a block stretch from one side of the page to the other, we can set the maximum width for our theme.)   
 Btw. most posts should have a max width.     
 - `"wideSize"` property is optional.    
 __We can configure how wide a block can stretch.__   
 If we add it in, WP will allow blocks to extend outside the bounds of the content.
 
    ```
    "settinngs" : {
      "layout": {
          "contentSize": "800px",
          "wideSize": "1100px"
        }
    }
    ```
The __content width__ is the maximum width of the main content area, typically the area where our blog posts or pages are displayed. This width is usually narrower than the overall width of our website, in order to make reading easier and more comfortable.    
On the other hand, the __wide width__ is the maximum width of elements that are wider than the *content width*, such as images or video embeds. This width is often used to create full-width or wide-width sections on our website.    
    
So, the __content width__ sets the maximum width of our posts, while the __wide width__ sets the maximum width for stretched content in our posts. We can say that both settings will set the maximum width for our blocks.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>


## [Margin and Padding](https://fullsiteediting.com/lessons/theme-json-layout-and-spacing-options/#h-margin-and-padding)
Margin and padding settings are disabled (false) by default.    
We can enable these settings on a global level and block level.

<br>

Insinde the `"settings"` we add a new property "`spacing"`.   
By setting the "margin" and "padding" true, u
sers will be able to configure the margin and padding for all blocks that support spacing.
```
"settings" : {
  "spacing" : {
      "margin": true,
      "padding": true
  }
}
```

Let's try adding some default styles to our theme. Let's reset the the "margin" and "padding".    
In `"styles"` we add `"spacing"` property with the `"margin"` and `"padding"` properties.   
```
"styles" : {
  "spacing" : {
    "margin" : {
      "top" : "0px",
      "bottom" : "0px",
      "left" : "0px",
      "right" : "0px"
    },
    "padding" : {
      "top" : "0px",
      "bottom" : "0px",
      "left" : "0px",
      "right" : "0px"
    }
  }
}
```
💡 If we want to apply padding on the y axis of an element we can omit the "right" and "left" properties.


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

## [Custom Units for margin and padding](https://fullsiteediting.com/lessons/theme-json-layout-and-spacing-options/)   
 
 Let's view the padding settings, and let's disable the EM unit, so user can not use it *can use REM, PX, %, etc.). To achieve this, we have to modify the `"spacing"` option in the `"settings"` object.    
 We add the __`"units"`__ property (which has an array of units) to the `"spacing"`.  
 ```
 "settings" : {
    "spacing" : {
      "margin" : true,
      "padding" : true,
      "units" : [
        "px", "em", "rem", "vh", "vw", "%"
      ]
    }
 }
 ```
 If we exclude the "EM" unit, we disable it.
  ```
 "settings" : {
    "spacing" : {
      "margin" : true,
      "padding" : true,
      "units" : [
        "px", "rem", "vh", "vw", "%"
      ]
    }
 }
 ```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

 ## [Block Gaps](https://fullsiteediting.com/lessons/theme-json-layout-and-spacing-options/#h-blockgap)
 A block gap refers to the space between blocks that are aligned side by side.   

 Eg.: the columns block is a block that implements gaps.

In the `"settings"` object we add the __`"blockGap"`__ property in the `"spacing"` option.    
```
"settings" : {
  "spacing" : {
    "blockGap" : true
  }
}
```
By turning this setting on (true), users will be allowed to customize the gap.    

If we want to give more breathing room to our columns, we can set it in the `"styles"` object, we have to modify the `"spacing"` property: we add the `"blockGap"` property with a size, eg. `"4rem"`.    
```
"styles" : {
  "spacing" : {
    "blockGap" : "4rem"
  }
}
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

## [Enabling everything: appearance tools](https://developer.wordpress.org/themes/advanced-topics/theme-json/#enabling-and-disabling-settings)   

A quick way of enabling everything, is to add the __`"appearanceTools"`__ in the `"settings"` object, and set it to `true`.
```
"settings" : {
  "appearanceTools" : true 
}
```
It give complete freedom to the users.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#13-global-styles)

<br>

<br>
<br>

# [Managing Asset Files](https://developer.wordpress.org/plugins/wordpress-org/plugin-assets/)

[Adding a static template as a theme](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#adding-a-static-template-as-a-theme)   
[Action Hooks](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#action-hooks)   
[Writing hooks - functions.php](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#writing-hooks---functionsphp)    
[Adding a hook](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#adding-a-hook)    


## [Adding a static template as a theme](https://www.cloudways.com/blog/html-to-wordpress/)
process of adding our static template to WordPress as a theme.

In the theme folder we create a folder `assets`.   
(The `assets` directory is not required by WP, because WP is very flexible with the structure of a theme, however we're allowed to define additional folders and files.)    
- Here we create our `index.html` file (and basically everything we would have in our html static website, such as CSS, and JS files).    
This is our __static__ template.   
In the `index.html` in templates folder, we create the content: 
it has a `<header>`, `<main>` and a `<footer>` section.         

Now we copy the __static__ index.html contents to the __`template/index.html`__'s body.   

Next step, is to load our CSS file (presumably we already have it).   

To add the CSS, we __avoid__ hard coded paths (because our content file's name can change, the http/https can change, and maybe we don't want to looad every single stylesheet).

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#14-managing-asset-files)

<br>

## [Action Hooks](https://developer.wordpress.org/plugins/hooks/)
__WordPress hooks are a way to modify or add functionality to WordPress without directly modifying the Core code__.     
Hooks are actions and filters that we can use to change the behavior of WP in different ways.

❗️A __hook is an event to run a PHP function__.

__Event systems__:    
an event system allows developers to execute code at specific moments in time.   
So, when we don't want to execute a code immediately (eg. wait until a specific action has occured).


💡 Naturally, PHP does not have an event system, therefore the WP created an event system called the Hooks API.   
(By using hooks, we can completely overhaul WordPress behavior.)

❗️ We can and should use a WP event for registering CSS and JavaScript files. 

We use the `functions.php` file to store the hooks. (We have to create this file)

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#14-managing-asset-files)

<br>

## [Writing hooks - `functions.php`](https://developer.wordpress.org/themes/basics/theme-functions/#:~:text=The%20functions.,modular%2C%20extensible%2C%20and%20functional.)    

WordPress prioritizes the `templates/index.html` file as the template for the home page.   
But the  loogic is saved in the `functions.php` file.   

Using different files for different things , separate code into different sections is a programming principle and it is called the separation of concerns.    

Outside the template folder we create a `functions.php` file (not function.php  → not the plural `s`).   
(This file completely optional, however, WP will automatically load it if defined in our theme.)

__`functions.php`__ : is responsible for the logic of a theme      
__`index.php`__ : is responsible for displaying the content, __unless__ an `index.html` file is available,

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#14-managing-asset-files)

<br>

## [Adding a hook](https://wpsites.net/genesis-tutorials/add-custom-hooks-to-theme/)

A *hook* as a way for us to listen to an event, if an event occurs, we can run a function during the event.    

There are 2 types of hooks:   
__[filter](https://codex.wordpress.org/Plugin_API/Filter_Reference)__ and __[action hook](https://codex.wordpress.org/Plugin_API/Action_Reference)__

Let's check out the action hooks, within that lets focus on the [`wp_enqueue_scripts`](https://developer.wordpress.org/reference/hooks/wp_enqueue_scripts/)   
it is used for enqueing both __scripts__ and __styles__.   
The word *enque* means to add something to a queue.   

The way it works:    
- when it's time to render the templates, WP starts processing the queue. If we add our scripts and styles to a queue, it will be loaded in to the document. All this happens before the WP template is rendered.

- In the `functions.php` file we are adding the [action hook](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#action-hooks) by adding the [`add_action()`](https://developer.wordpress.org/reference/functions/add_action/) function. 
(This function tells WP to run a function when a specific hook runs.)    
*We will want to load CSS and JavaScript files (wp_enqueue_scripts)*   
It can have 4 arguments, but only the first 2 are required.   
- 1st argument: the name of the hook that allows us to perform this action is called `wp_enqueue_scripts`
- 2nd argument: is the name of the function that will run during the event: `m_enqueue`.    
The name of our function can be anything we want. It should be unique, because functions cannot be defined twice.

  *functions.php*
  ```
  <?php 
  // 💡 There isn't a reason to close the app tag if we're not going to add HTML.

  // Variable declarations


  // Include statements


  // Hoooks
  add_action('wp_enqueue_scripts', 'm_enqueue');
  ```

To keep things organized, it is recommended dedicating a directory for the logic of our theme. So let's create a separate file where we define our functions. We can use PHP's `include` function to include spearate files.   

- Let's create a folder `includes` inside our WP theme. Best practice to outsource the logic of our theme to this folder.  
- inside the `includes` folder let's create a folder called `front`. Files related to the front end of a site will be defined within this directory.
- inside this folder let's create a file `enqueue.php`, where we define our `m_enqueue()` functions.     

  *enqueue.php*
  ```
  <?php

  function m_enqueue() {
    
  }
  ```

- To include our m_enqueue.php, we're going go to the `functions.php` and write the `include()` function.     
💡It is recommended to use absolute path.  
 Using the `get_theme_file_path()` function (defined by WP) provides the absolute path to the current activated theme on the site. `include(get_theme_file_path);`    
 This function returns a full system path to a file, the path that returns is based on the name of the file we pass in. (*It has one argument which is the path to the file relative to the theme*)   

  *funcitons.php*    
  ```
  <?php 
  // Variable declarations


  // Include statements
  include(get_theme_file_path('includes/front/enqueue.php'));

  // Hoooks
  add_action('wp_enqueue_scripts', 'm_enqueue');
  ```
  In this file, we're telling WP we would like to run a function during the `wp_enqueue_scripts` hook, here WordPress will run the `m_enqueue` function.
  
--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#14-managing-asset-files)

<br>

## [Registering styles](https://developer.wordpress.org/reference/functions/wp_register_style/)  

  WP has a queue for a list of files that should be loaded on the site.
  When add our files to this queue, they will get loaded.   

  There are 2 steps for queuing a file:    
  ❗️ we need to __register__ the file:    
    it  means we're telling WP the existence of a file: telling WP where to find the file with other details.

   - after registering the file, we can add it to the queue 

   - 2 types of files can be registered: CSS and JS files

<br> 

  The [`wp_register_style()`](https://developer.wordpress.org/reference/functions/wp_register_style/) function can register a CSS file.   
  This function has a bunch of [paramters](https://developer.wordpress.org/reference/functions/wp_register_style/#parameters), they describe the values that can be passed into the function.   

<br>

  Let's examin this `wp_register_style()` fuctions:    
  - WP will document the name of the parameter. (eg. `$src`)
  - Then it is followed by the data type of a parameter. (eg. `string|bool`)
  - WP tells us if the parameter is required or not (eg. `$src string|false Required`)
  - when it's not `required` it's `optional`, it means WP provide optional, default values

  Let's register a CSS file:    

  in the assets/index.html template file: we can see a lot of styles.    
  We are going to add the the `enqueue.php` file the google fints style.
  *index.html*
```
  <!DOCTYPE html>
   <html lang="en">
     <head>
        <meta charset="UTF-8" />
        <link rel="icon" type="image/svg+xml" href="/public/favicon.svg" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Udemy Static Template</title>
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
      ► <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap" rel="stylesheet"> 
        <link href="/bootstrap-icons/bootstrap-icons.css" rel="stylesheet"> 
        <link rel="stylesheet" href="/public/index.css">
     </head>
```
  Open the __`enqueue.php`__  
  `wp_register_style()`:    
  - the 1st parameter of the `wp_register_style()` is the [`$handle`](https://developer.wordpress.org/reference/functions/wp_register_script/#parameters) name. The `$handle` name can be thought of as a unique ID for reference, good to prefix it.      
           
  *enqueue.php*
```
  <?php

  function m_enqueue() {
    wp_register_style(
      'm_font_rubik_and_pacifico',
    )
  }
```

  Add a 2nd parameter, which is the URL ([$src](https://developer.wordpress.org/reference/functions/wp_register_script/#parameters)) to the file. (Must be a valid `http` url, system paths are not accepted ). Here it's the Gogole Font CDN's URL.

```
    <?php

    function m_enqueue() {
      wp_register_style(
        'm_font_rubik_and_pacifico',
        `https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap`
      )
    }
```  

  The  `wp_register_style()` must be called for each style sheet.      
  Let's add the Bootstrap: 1st lets set the ID to `m_bootstrap_icons` then add the path to the file. 

  Since our link is not `HTTP` url, we have to generate: using the __`get_theme_file_uri()`__ function  (this function will return a URL to our theme).   
  After we regaister the `index.css` styleshett.
```
    <?php

    function m_enqueue() {
      wp_register_style(
        'm_font_rubik_and_pacifico',
        `https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap`
      );
       wp_register_style(
        'm_bootstrap_icons',
        get_theme_file_uri('assets/bootstrap-icons/bootstrap-icons.cs')
       );

       wp_register_style(
          'm_theme',
          'get_theme_file_uri('assets/public/index.css');
       );
    }
```
So, 2 paramteres a required, but there are other paramters. Eg. the 3rd paramter is the __dependicies__.    
eg.:   
our theme.css file needs the icon file. The icon file can be considered a dependency. In that case, we can pass an array to the 3rd parameter in this array. We need to add a list of handle names to this array. 


```
    <?php

    function m_enqueue() {
      wp_register_style(
        'm_font_rubik_and_pacifico',
        `https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap`
      );
       wp_register_style(
        'm_bootstrap_icons',
        get_theme_file_uri('assets/bootstrap-icons/bootstrap-icons.cs')
       );

       wp_register_style(
          'm_theme',
          'get_theme_file_uri('assets/public/index.css'),
          '[m_bootstrap_icons]'
       );
    }
```
If the theme file gets enqueued, the bootstrap icons file will get enqueued too.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#14-managing-asset-files)

<br>

## [Enqueuing Styles](https://webdesign.tutsplus.com/tutorials/loading-css-into-wordpress-the-right-way--cms-20402)    
 
 The [`wp_enqueue_style()`](https://developer.wordpress.org/reference/functions/wp_enqueue_style/) function enques a CSS file.  

 This is the next step to adding our assets to the document.

 The __difference between registering or enqueuing__ a style:
  - when a file is registered, WP becomes aware of it. It doesn't do anything with the file, it just stores the location of the file in memory.
  - queuing a file tells WP to load the file in the browser!

  (It is a good practice to register a file before queing it. However it is optional.)

  `wp_enqueue_style()` function has only 1 required parameter if we registered the file before.  This paramter is the: __[`$handle`](https://developer.wordpress.org/reference/functions/wp_enqueue_style/#parameters)__   
  The `$handle` must correspond with the name stored during registration.
     
  (The other parameters are the same parameters for the WP register style function. If we decide not to register a file, we need to provide this information.)   

  The `wp_enqueue_style` function will search through the list of registered files to get the rest of the information.

   Open the __`enqueue.php`__ file.   
   We are calling the `wp_enqueue_style` after the `wp_register_style()` function.    
   We're going to load the files in the same order we registered them.  
   The value must match the value passed into the 1st argument of the `wp_register_style` function.

   `enqueue.php`
   ```
    <?php

    function m_enqueue() {
      wp_register_style(
        'm_font_rubik_and_pacifico',
        `https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap`
      );
       wp_register_style(
        'm_bootstrap_icons',
        get_theme_file_uri('assets/bootstrap-icons/bootstrap-icons.cs')
       );

       wp_register_style(
          'm_theme',
          'get_theme_file_uri('assets/public/index.css')       
        );

  ►    wp_enqueue_style(
          'm_font_rubik_and_pcifiko'
       );
       wp_enqueue_style(
          'm_bootstrap_icons'
       );
       wp_enqueue_style(
          'm_theme'
       );
    }
   ```
Now WP should load our files in the `<head>` section of the document.   

WP creates the base template for our theme.   
This includes calling the [`wp_head()`](https://developer.wordpress.org/reference/functions/wp_head/) function, which is responsible for creating a location for our theme to load files.

<br>

When eg. looking for the font, we can find it by the ID which matches the 1st value passed into the `wp_register_style()` function → `'m_font_rubik_and_pcifiko'`. In the `<head>` we can find `<link rel="stylesheet" id="u_font_rubik_and_pacifico-css" href=...>`   

__WP modifies our URL in 2 ways:__   
1.
  - We can see in the developer console, that the __URL__ of the font is different compared what we gave in `function m_enqueue()` / `wp_register_style`.   
  The original URL: `https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap`

  - The modified by WP URL: (`ver=6.2` at the end, the version of our WP) 
  `https://fonts.googleapis.com/css2?family=Rubik%3Awght%40300%3B400%3B500%3B700&display=swap`__`&ver=6.2`__    

2. 
  - WP removes duplicate parameters. For this reason, both fonts aren't loaded, only 1 font loads.    
  (Here the `family` has been added twice.)
  Original URL: `https://fonts.googleapis.com/css2?`__`family=`__ `Pacifico&`__`family=`__ `Rubik:wght@300;400;500;700&display=swap`

*A URL query parameter refers to a value added to a URL. Query parameters allow us to send data in the URL.    
After the __`?`__ we can add key-value pairs diveded by the __`&`__ symbol. Like: `example.com?key=value&key=value`*

<br>

To fix our site, __we need to prevent the version query parameter from being added to the URL__.
Navigate to:   

`includes/front/enqueue.php`  

*We need to specifiy the 4th argument: it allows us to specify a version before adding it.*   

*To add a 4th argument we have to give a 3rd argument before. Here we pass an empty array `[]`* 

*For the 4th argument, we can pass in a string to set a custom version. Here we add `null` instead of string - by this we tell WP that nothing should be stored*

`enqueue.php`
```
  <?php

    function m_enqueue() {
      wp_register_style(
        'm_font_rubik_and_pacifico',
        `https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap`,
  ►     [], 
  ►     null 
      );
       wp_register_style(
        'm_bootstrap_icons',
        get_theme_file_uri('assets/bootstrap-icons/bootstrap-icons.cs')
       );

       wp_register_style(
          'm_theme',
          'get_theme_file_uri('assets/public/index.css')       
        );
     ...
```
Now can see the URL remained unmodified (the version query paramter is not applied)
`https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap`


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#14-managing-asset-files)

<br>

## [Loading Additional Head Tags](https://developer.wordpress.org/reference/hooks/wp_head/)

In the íassets/index.htmlí file's header we can see the <links> tag with the attribute `preconnect`. (they can boost the performance of our site by including them.)

index.html
```
<!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <link rel="icon" type="image/svg+xml" href="/public/favicon.svg" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Udemy Static Template</title>
►     <link rel="preconnect" href="https://fonts.googleapis.com">
►     <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
      <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap" rel="stylesheet"> 
      <link href="/bootstrap-icons/bootstrap-icons.css" rel="stylesheet"> 
      <link rel="stylesheet" href="/public/index.css">
    </head>
```

Unfortunately, the browser doesn't know what files are hosted locally or on another server: eg. our google fonts are hosted on the google server, while other things hosted in our server. It can take a while for the browser to figure it out.   

We  can tell the browser to connect to Google servers ahead of time. Let's try adding these tags to the head section of the documents.    

<br>

*Let's add an `action` hook into our `functions.php` file, with the action hook called [`wp_head`](https://developer.wordpress.org/reference/functions/wp_head/)* 

*During this hook, we can add content to the document: name the function as `m_head`*   

*Then, we can define the `m_head` function in a separate file (best practice).*      
__functions.php__
```
  <?php 
    // Variable declarations


    // Include statements
    include(get_theme_file_path('includes/front/enqueue.php'));

    // Hoooks

    add_action('wp_enqueue_scripts', 'm_enqueue');
►   add_action('wp_head', 'u_head');
```

In the `assets/includes/front/` we careate the `head.php` file.   
__head.php__
```
<?php 
function m_head() {

}
```
Then we include the `head.php` file in the `functions.php` file's `include` section.    
__functions.php__
```
  <?php 
    // Variable declarations

    // Include statements
    include(get_theme_file_path('includes/front/enqueue.php'));
►   include(get_theme_file_path('includes/front/head.php'));

    // Hoooks
    add_action('wp_enqueue_scripts', 'm_enqueue');
    add_action('wp_head', 'u_head');
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#14-managing-asset-files)

<br>

The last step is to output the tags back in the HTML documents.
We copy the following `<link>` tags     
__index.html__
```
...
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
...
```

Then in the `head.php` file we output these tags.   
💡 instead of the `echo` statement we output the tags: the `<?php` tag at the beginning of the function switches from HTML to PHP mode and indicates the start of a PHP code block. The subsequent `?>` tag at the end of the function switches back to HTML mode and indicates the end of the PHP code block.




__head.php__
```
<?php 

function m_head() {
  ?>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <?php
}
```

The tags are now added to the <head> but they load after the google fonts load😱    
Therefore we have to add a 3rd argument in the `functions.php`'s `add_action('wp_head', 'm_head')`.    
[Priorities in WP](https://learn.wordpress.org/tutorial/wordpress-action-hooks/#:~:text=Because%20WordPress%20Core%20registers%20any,callback%20functions%20have%20been%20completed.) are numberd behind the sence, up to 10. the lower the number the higher its priority.

*We add 5 as a 3rd argument, to change the `wp_head` action hook's priority*
*Now it's closer to the beginning of <head>, so it loads before the google fonts lead.*        
__function.php__  
```
  <?php 


    // Variable declarations


    // Include statements
    include(get_theme_file_path('includes/front/enqueue.php'));
    include(get_theme_file_path('includes/front/head.php'));

    // Hoooks

    add_action('wp_enqueue_scripts', 'm_enqueue');
►   add_action('wp_head', 'u_head', 5);

```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev#14-managing-asset-files)

<br>

# [Templates](https://developer.wordpress.org/themes/block-themes/)

## [Template Part: header and footer](https://fullsiteediting.com/lessons/templates-and-template-parts/#h-creating-your-first-template-parts)

First, we have to split our index.html into multiple files.

At the `templates` folder we have an `index.html` file, which is very long (500 lines) → break it into smaller peces. It allows us to create reusable parts → these will be our template parts.   

We have to identify which sections should be placed in a separate file.

Start with __header__ and __footer__    

<br>

__Temaplte parts__ :      
a template part is an HTML file representing a section of a template by themselves.

To create template parts, first we need to create a __folder__ named __`parts`__ ❗️

In __parts__ folder we create 2 files:
  - header.html
  - footer.html

*(file name for template parts are flexible)*

We can create blocks with or without WP's editor.   
Here we use WP's FSE editor.

Open WP's editor:   
- click on the __edit site__ (we are on our index site)
we see a very long few 100 lines of HTML: empty out the html block.

- we add 2 more HTML blocks (so we'll have total 3 blocks empty)    
*click on the `+` button and add `html`*

- switch back to our `index.html` file where we get our lines:   
*(between the tags we have all the necessary lines - it's just shown shortly here for clarity)*  
__index.html__
```
<header class="shadow">...
</header>

<main class="container !mx-auto my-16 grid grid-cols-3 gap-16">...
</main>

<footer class="bg-gray-700 p-16">...
</footer>
```

Now we copy the `<header>` part to the `header.html`, the `<main>` to the `index.html` and the `<footer>` to the `footer.html`

- we jsut have to lead these template parts. *(By default Template parts are not loaded into a template → breaks the site)*

- if we go to the WP site editor, we can see the te index.html is missing the header and footer tags.

- we insert below and above HTML block (click on the `+` button on the right) : insert `template part`

- the template part block is capable of loading a template part

- click on the `choose` button → WP found our template parts. We can select and load them.

- on the `List View` we select the header block and copy it into the index.html file *(from WP we copy to our code editor)*      


*the block header and footer we got by copying the block from WP: `<!-- wp:template-part {"slug":"header","theme":"test"} /-->`*  

__index.html__
```
<!-- wp:template-part {"slug":"header","theme":"test"} /-->

<!-- wp:html -->
<!-- Main Content -->
<main class="container !mx-auto my-16 grid grid-cols-3 gap-16">...
</main>
<!-- /wp:html -->

<!-- wp:template-part {"slug":"footer","theme":"test"} /-->
```

By this code: `<!-- wp:template-part {"slug":"header","theme":"test"} /-->`
WP detects that we're loading a template block.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Anatomy of a block](https://fullsiteediting.com/blocks/)

A brief overview of blocks.

Let's check out our `index.html` file:
here we have 3 __blocks__:  

__index.html__
```
<!-- wp:template-part {"slug":"header","theme":"test"} /-->

<!-- Main Content -->
<main class="container !mx-auto my-16 grid grid-cols-3 gap-16">
...
</main>
<!-- /wp:html -->

<!-- wp:template-part {"slug":"header","theme":"test"} /-->
```

- __The HTML block__:   
  - The comments (see below) lets WP knows where a blocks starts and ends.     
  It has:   
  has opening  
  `<!-- wp:html -->`   
  and closing tags  
  `<!-- /wp:html -->` 

  - The comments (opening/closing) contain the name of the block: here the name is `wp:html`

  - inside the `<!-- wp:html -->` & `<!-- /wp:html -->` is the __contents__ of the block which is rendered on the page.

- __The template block__:
  - unlike the HTML block, the template part block does not have inner content, nor does it have a closing HTML comment.

  - __template blocks can be selfclosing__:   
  note the __` /--> `__ in the    
  `<!-- wp:template-part {"slug":"header","theme":"test"} /-->`

  - the template part block is an example of a block that __renders content through PHP__

  -  after the name of the block there is JSON   
    `{"slug":"header","theme":"test"}`   
    (WP parses this object before presenting the content)   
    (It can be difficult to alter these settings through an HTML comment.)

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Integrating Custom Templates (templates/index.html) with Gutenberg Editor](https://developer.wordpress.org/block-editor/) 
WordPress themes combine static templates (e.g., `index.html`) with the dynamic Gutenberg block editor. Here's how they work together.   
<br>
__Here's how it works__:
<br>
1. **Template Loading**:
When a page is rendered, WordPress looks at the theme files (like `index.html`) for structure. The blocks defined in Gutenberg are inserted into the corresponding areas dynamically.

3. **Using Gutenberg Blocks in Templates**:
   - Blocks created with the Gutenberg editor (like the header or footer blocks) are saved as part of the site's database.
   - These blocks can be referenced in your template files using comments like:
     ```html
     <!-- wp:template-part {"slug":"header","theme":"test"} /-->
     ```
     This tells WordPress to insert the appropriate block (in this case, the "header" block).

4. **Editing and Syncing**:  
Copying a block’s code from Gutenberg into index.html makes it part of the default template. However, any future edits made to that block in Gutenberg will not update the index.html file. The changes are saved in the database instead.

	To explain better, the Gutenberg edits are saved in the database:    
	  - When we make changes to a block through the Gutenberg editor, WordPress stores those changes in the database, specifically for the page or post we are editing. This ensures that the customized layout for that page is preserved.
	
	  - Templates like `index.html` serve as **fallbacks**: The `index.html` file in our theme is a static template. When WordPress renders a page, it first checks if a customized layout is saved in the database. If a layout exists (because we've edited it in Gutenberg), WordPress uses that layout and not the `index.html` (fallback file).

<br>
	
*This is an image of copying a block*
<br>

![copying](https://github.com/user-attachments/assets/74b6c05e-5a99-494c-83d3-8290e1bdb450)    

<br>    

*After this, we can paste it into our `templates/index.html`*

**Key Takeaways**      
- *Does `index.html` Always Load?*    
Not always. WordPress prioritizes layouts saved in the database if a page has been edited in Gutenberg. If no saved layout exists, it falls back to `index.html`.

- *Why Do Copied Blocks Work?*    
Blocks added to `index.html` become part of the theme’s default structure. They appear when the template loads but aren’t connected to the editor for future updates.    

**Best Practices**:  
   - Use `index.html` for default layouts and static content.
   - Use Gutenberg for content and layout customization on individual pages/posts.
   - Avoid mixing editing methods to prevent conflicts between the editor and templates. 

**WordPress Rendering Process**    
WordPress prioritizes layouts saved in the database for edited pages or posts.   
Example: If a page's template is edited, the saved version is loaded.
If no saved layout exists, the system falls back to theme templates like `index.html`.
Copying blocks into `index.html` updates the fallback layout, which takes effect unless superseded by saved content.

##### [link 01](https://developer.wordpress.org/block-editor/)   

##### [link 02](https://wordpress.org/plugins/templateberg/)   
 

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Header-footer optimization](https://www.wpzoom.com/docs/how-to-customize-the-header-in-wordpress-full-site-editor/)

  WP default blocks can generate additional markup.    
  eg.:    
  *Our header in the dev tool is between additional `<div>` tags.*   
  ```
  ► <div class="wp-site-blocks">
     <!-- Header -->
      <header class="shadow">...</header>
  ```
  We can optimize the generated HTML with the block settings.

 If a block can generate the same HTML as our static template, than we will let the block generate the HTML. If it can't, than we'll use an HTML block.

 *💡 WP's is HTML may not always match our static templates HTML.*

 (This part what we are going to do with the header is also relevant/same for the footer.)
 Let's switch to the full site editor:   
 - here we can see the header, the main (custom html), and the footer.   

 - select the header template. On the right-side bar select the __advance__ panel.   

 - here go to `HTML element`. We have the option of changing the default `<div>` tag setting to a different element. Let's change the tag to `<header>` (instead of `<div>`) by sleceting it from the list.

 -  next step: let's open the `header.html` file     
 *Here we have a class named "shadow"*     
    __header.html__
    ```
    <!-- wp:html -->
    <!-- Header -->
    <header class="shadow">
      <!-- Topbar -->
    ```
- back in the browser, in the *site-editor* mode, on the right side, Advanced/ADDITIONAL CSS CLASS(ES):   
here we can paste the header's `shadow` class    
→ WP merges its classes with our classes.
- now copy the header: *Copy block*   
- go to the `index.html` and update it by pasting our header block:     
We replace our header block with the new copy:    
  - old:    
	`<!-- wp:template-part {"slug":"header","theme":"test"} /-->`
  - new (updated block definition:):    
    	`<!-- wp:template-part {"slug":"header","theme":"test","tagName":"header","className":"shadow"} /-->`
    
	specifies additional attributes, such as tagName and className. These attributes allow WordPress to render the header block with the appropriate HTML tag and class directly in the output.    

	*Simplifies `header.html`:*   
	By defining the class and other properties in the block comment, we don't need to hard-code them in the `header.html` file. This ensures consistency. 
  *So we do this because it is easier to let the template part block create the class element for us (also less lines in our header.html file)*
- now switch to the `header.html` file and __remove__ the `<header class="shadow">` `</header>` tags.   
→ now we have only `<div>`s in the `header.html` file.   
- if we check the header in the browser's dev tool we can see that the `<div>` tag changed to a `<header>` tag:    
 *`<header class="shadow wp-block-template-part">`*
  
	Why we have removed the `class="shadow"`from our `header.html` file? Because this ensures the `<header>` element with the `class="shadow"` is rendered automatically, without needing the static definition in `header.html`. Since WP is capable of generating the necessary markup dynamically, including attributes like className and tagName → This streamlines the code and reduces redundancy in our templates.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>


## [Dummy content in WP](https://wordpress.org/plugins/fakerpress/)
Dummy text helps us to test our theme.
We use a plugin called [fakerpress](https://wordpress.org/plugins/fakerpress/).  

We start by creating some *terms*.   
(*terms* are the *categories* and *tags* associated with a *post*)

on the dashboard left sidebar click: FakerPress/Terms    
here we can set up our dummy texts paramters → click to *generate*   

We can also generate *posts* by going to the FakerPress/Posts   
here wen can set a bunch paramteres:
 - the quantity eg.: 20 and 30
 - the date option eg.: last 15 days
 - the post type field: it should include posts and pages
 - the author fields should be set to whatever account 
 - the Taxonomy Field Rules section:   
 here we can add categories and tags to a post under the rates field.
 - we can also configure the images generated for a post.

→ clcik to generate

After we can deactivate the plugin.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Making a top-bar](https://wordpress.com/support/site-editor/customize-your-header/)

The `<header>` should be grouped → we can move the header into different places. (💡template part)

Let's suppose our header contains 3 parts (3 rows: a top, a middle  and a bottom).   
We are going to create them as blocks.   

By using template parts, we can tell the editor to focus on a specific template part.

Open the site-editor (edit site): we can see our parts (header, index, footer).   
 - On the left sidebar select `template parts`
 - select the `header` template part   
 (On the header template part, we can focus on the header's __blocks__)
 - next step is to begin adding blocks
 - the top part of our header (top-bar) can be considered as a row of blocks
 → click on the `+` and add a `row` block to the top of our template (move it above the `custom html`)   
 This block is going to act as the overall container for the top bar.
 - the top bar element is the root div element
 - we can configure the properties either with CSS or with block settings. 
 
 Let's look how to configure properties with block settings (with the way users can modify easier the styles with the Gutenberg editor. With CSS they need a CSS knowledge.) 

 - changing the background color of the row block: bar on the right/Block/Layout/Styles(◉)/Color
 - setting the font size
 - setting padding
 - Save the changes

1. Add a block
2. Add styles:    
*apply styles through the blocks settings*
3. Add classes:    
*add classes for styles that can't be applied through a block settings*

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Modifiny the editor's style by code](https://developer.wordpress.org/block-editor/how-to-guides/enqueueing-assets-in-the-editor/)
#### [bonus link](https://codex.wordpress.org/Editor_Style)
We create an include folder and in it a `setup.php` file. In the `functions.php` we include the `setup.php`: <br>
`include(get_theme_file_path('/includes/setup.php'));` 

<br>

In the `setup.php` we write the following code to [modify the editor's style](https://developer.wordpress.org/reference/functions/add_theme_support/): 

<br>  

```
	function name_my_function_setup_theme(){
	  add_theme_support('editor-styles');
	
	// add_editor_style is a shortcut to add styles to the gutenberg edotir
 	// here adding the styles
	  add_editor_style([
	    'this can be for example a google fonts link',
	    'assets/bootstrap-icons/bootstrap-icons.css',
	    'assets/public/index.css'
	  ]);
	}
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Use HTML block to create a custom look](https://wordpress.org/documentation/article/custom-html/)

Creating a UI with multiple nested group blocks for icons, font sizes, and background colors can be challenging in WordPress. It often becomes difficult to manage and maintain. In such cases, using an **HTML block** in the Gutenberg editor or referencing **custom HTML from a file** (like parts/header.html) is often a better approach for a streamlined custom look.

Eg. we want an avatar, username and login button as 1 block. We open the HTML block in the Gutnberg editor and we write a code, like
```
    <div class="wp-block-something-plus-header-tools">
      <!-- Signin Modal Link -->
      <a class="signin-link open-modal" href="#signin-modal">
        <div class="signin-icon">
          <i class="bi bi-person-circle"></i>
        </div>
        <div class="signin-text">
          <small>Hello, Sign in</small>
          My Account
        </div>
      </a>
    </div>
```

You must create a separate file for handling the editor's markup to ensure a consistent and manageable structure.
<br>
In our `setup.php` we include an `editor.css` file from the `assets` folder.
```
<?php
function a_setup_theme(){
  add_theme_support('editor-styles');

  add_editor_style([
    'https://fonts.googleapis.com/css2?family=Pacifico&family=Rubik:wght@300;400;500;700&display=swap',
    'assets/bootstrap-icons/bootstrap-icons.css',
    'assets/public/index.css',
    'assets/editor.css'
  ]);
}
```
The `editor.css` file contains CSS that modifies or styles your content within the Gutenberg editor. This ensures that what you see when editing matches your design intentions and prevents discrepancies between the editor and the front end.
<br>
Example: If we want to hide the *search form in the header* (just for example), we can add the following CSS in `editor.css`:
```
.header-search-form .wp-block-search__label,
.header-search-form .wp-block-search__button {
  display: none;
}
```
This will hide the search label and button while editing in the Gutenberg editor.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Formatting Main Content - Columns](https://learn.wordpress.org/lesson/designing-with-the-columns-block/)

The key point is combining the Gutenberg editor with custom code to create pages. For example, in the main content area below the header, we use Gutenberg's Columns block alongside a custom templates/index.html file.

Example Template
(Note: Styling uses Bootstrap for brevity, though plain CSS is preferred for better performance.)
We can simplify by omitting unnecessary classes since the Columns block provides similar functionality. Only container and auto classes are used to center the content:

`templates/index.html`
```
<!-- Main Content -->
<main class="container !mx-auto my-16 grid grid-cols-3 gap-16">
  <div class="col-span-2">
    Column 1
  </div>
  <div>
    Column 2
  </div>
</main>
```
The `<main>` element contains 2 `<div>` tags for column content. The col-span-2 class sets the first column to 70% width, but this can be skipped since column widths are adjustable in the WordPress block settings. The design choice is up to us. <br>
In the Gutenberg editor, we add a column block under the header. There is an option to create a 2/3 - 1/3 column layout
<br>
We select the 'parent' column and, in the Advanced settings (bottom right), add the CSS classes from the `<main class="container !mx-auto"...>`. The remaining classes will be handled by WP Gutenberg. <br>
Paddings, margins and other styles can be added in the editor. Above the Advanced settings, there is the Dimensions section, where we can add paddings.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Rendering posts with the Query Loop Block](https://wordpress.org/documentation/article/query-loop-block/)

This query loop block fetches posts from the database, displays them, and adds pagination. It allows filtering by post type, taxonomies, etc. <br>
When adding the block, WordPress suggests various layouts. If your design requires a layout different from the defaults, choose the "Start Blank" option to begin with a basic template. (Here, we can choose options like sorting by date or title, allowing WordPress to display our posts accordingly.) 
<br> 
The Query Loop block is responsible for retrieving posts based on the specified criteria (e.g., post type, taxonomy, etc.). However, rendering the content of each post within the Query Loop is handled by the blocks inside the Query Loop, such as the Post Template block and its child blocks.   
The Query Loop block fetches the data and stores it in an array. The Post Template block then iterates through this array to render each post, so it loops through the array with PHP, but in FSE work can be handled by WordPress core blocks.

<br>

In WordPress, a query is a request for data from the database, which is why the block is called the Query Loop. The query is based on the current URL, prompting WordPress to retrieve and display posts that match the URL context. For example, on the home page, the query will select the latest posts. On a search page, it will retrieve posts matching the search term.
<br>
By choosing the "Custom" option, we can create a custom query. This means the Query Loop block won't generate a new query but will instead use WordPress's existing query for the page.   

<br>

![Custom  option](https://github.com/user-attachments/assets/6e3c777c-bdb5-4c18-885e-e515733c3a4f)


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [WordPress's Template Hiearchy](https://developer.wordpress.org/themes/basics/template-hierarchy/)

WordPress determines the type of content to render on a page by analyzing the URL. Based on this analysis, WordPress performs a query to the database to retrieve the appropriate posts or content that should be displayed. This process aligns with the WordPress template hierarchy, which decides which template file is used to render the page.    


**What URL Does WordPress Analyze?**   

WordPress analyzes the URL segment after the domain name `(e.g., https://example.com/about focuses on /about)`. This segment is often referred to as the path.   

The URL can include:    
*Permalink structure*    
WordPress interprets the URL based on the site's configured permalink settings `(e.g., /%postname%/, /category/post/, etc.)`.    
*Query string*   
If permalinks are not enabled, URLs might include query variables like `?p=123 or ?cat=5`.

<br>

**How Does WordPress Analyze the URL?**   

- *Parsing the URL:*      
WordPress uses the path to determine the query variables, such as `post_type`, `page_id`, or `category_name`.
If the URL includes query strings, these variables are directly passed to the database query.   

- *Routing via Query Vars:*    
WordPress maps parts of the URL to internal query vars. For example:
	- `/about → pagename=about`
	- `/category/news → category_name=news`
	- `/?p=123 → post_id=123`   
These query vars define what kind of content to fetch, like a `page`, `post`, or `archive`.

- *Running the Query:*     
WordPress uses the query vars to create a **WP_Query object**. This object retrieves the relevant posts, pages, or taxonomy terms from the database.

- *Template Hierarchy:*    
After identifying the type of content, WordPress determines which template file to use. WordPress template hierarchy works in a fallback order.
For example:
	- `/about → page-about.php`, then `page.php`, then `index.php`.    
	- `/category/news` → `category-news.php`, then `category.php`, then `archive.php`, and so on.   \
 

💡 In these examples, the PHP file extension is used. In block themes, **HTML files** are used instead, but **the template hierarchy is the same**.

![WordPress explaines it in a diagram](https://i0.wp.com/developer.wordpress.org/files/2014/10/Screenshot-2019-01-23-00.20.04.png?ssl=1)    

*If we examine the entire template hierarchy, all paths eventually fall back to the index template. This is why every theme must include an index template to meet WordPress's validity requirements.*

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Necessary templates: 404 (NotFound) template](https://developer.wordpress.org/themes/basics/template-hierarchy/#404-not-found)


According to the hierarchy, if no 404 template is available, WordPress falls back to the index template. However, the index template isn't ideal for displaying 404 errors, which are meant to indicate that no content was found for the requested URL.

To create a 404 page we can do the following: in the text editor we go to the `templates` folder, and create a file named `404.html`. In that file we can write a very simple code, basically a heading and some texts.   

```
	<!-- wp:template-part {"slug":"main-header","theme":"custom-theme","tagName":"header","className":"!custom-class!"} /-->
	
	<!-- wp:group {"style":{"spacing":{"margin":{"top":"6rem","bottom":"6rem"}}},"className":"content-container center-align"} -->
	<div class="wp-block-group content-container center-align" style="margin-top:6rem;margin-bottom:6rem">
	  <!-- wp:heading {"textAlign":"center","level":1,"style":{"typography":{"fontSize":"6rem"}},"textColor":"primary","className":"!error-title-class!"} -->
	  <h1 class="has-text-align-center !error-title-class! has-primary-color has-text-color" id="error-404" style="font-size:6rem">404</h1>
	  <!-- /wp:heading -->
	  
	  <!-- wp:heading {"textAlign":"center","style":{"typography":{"fontSize":"1.5rem","fontStyle":"italic","fontWeight":"400"},"spacing":{"margin":{"top":"0rem","bottom":"1rem"}}}} -->
	  <h2 class="has-text-align-center" id="not-found" style="font-size:1.5rem;font-style:italic;font-weight:400;margin-top:0rem;margin-bottom:1rem">
	    Sorry, we can't find the page you're looking for.
	  </h2>
	  <!-- /wp:heading -->
	  
	  <!-- wp:paragraph {"align":"center","className":"!home-link-class!"} -->
	  <p class="has-text-align-center !home-link-class!"><a href="/" target="_self" rel="noopener">Return to the homepage</a></p>
	  <!-- /wp:paragraph -->
	</div>
	<!-- /wp:group -->
	
	<!-- wp:template-part {"slug":"main-footer","theme":"custom-theme","tagName":"footer"} /-->
```

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Necessary templates: Category Template](https://developer.wordpress.org/themes/basics/template-hierarchy/#category)   


Based on the [documentation](https://developer.wordpress.org/themes/basics/template-hierarchy/#category), WordPress looks for 5 different templates in our theme, starting from the top.  

*Rendering category archive index pages uses the following path in WordPress:*
```
  1.	category-{slug}.php – If the category’s slug is news, WordPress will look for category-news.php.
  2.	category-{id}.php – If the category’s ID is 6, WordPress will look for category-6.php.
  3.	category.php
  4.	archive.php
  5.	index.php
```

- 1. `category-{slug}.php`   

It loads a template file named after the category slug. The file name might seem a bit unusual: there are curly brackets  surrounding the word slug (`category-{slug}.php`). Curly brackets indicate a placeholder.  
A slug is a keyword that gets attached to the URL.   

For example, if we have a site and want to set up a `category`, the URL structure will be consistent across all categories. It starts with the word *`category`, followed by the `slug` that identifies the specific category*.    

According to the WordPress documentation, we can create a template for a specific category by using its slug. This is particularly handy if we want to give that category a unique design.    

<br>

- 2. `category-{id}.php`
The next template is called Category ID. Categories are stored in a database, where most entries are assigned a unique `ID`. While `slugs` are useful, they’re not always reliable since administrators can change them. If we want to create a special template for a category without relying on its `slug`, we can use its `ID` instead. Unlike `slug`s, `ID`s are permanent and unchangeable.

<br>

- 3. `category.php`
There’s also a template called `category`. This template is used for all categories by default.

<br>

- 4. `archive.php`     
The archive template is a general template used for various types of pages that aren't the home page. Archives are general templates used for different types of pages that aren't the home page.

<br>

- 5. `index.php`
If the other templates aren’t available, the index template will be loaded as a fallback.

<br>

WordPress gives theme developers a lot of flexibility when it comes to templates.    
If we want to create a generic template for all categories, the `category.php` template is ideal for our theme.  
Let's create a `category.html` file in the `template folder`. The category template can be quite similar to the `index.html` template, so we can simply copy the content from the `index.html` file into the `category.html` file.   

We can start by adding the header at the top and creating classes to adjust the color, position, and size of the header.    
Most of this can be recreated using blocks. However, there is one issue: WordPress doesn't have a built-in block for displaying the name of the current category on the page. Without this, our block would just show the same text.    

To fix this, we have to create a custom block to display the category name. As a temporary solution, we can use the HTML block to manually add this information.    
For example: here is a code snippet which creates a custom header block with a placeholder for the category name:

```
    <div class="wp-block-mytheme-plus-page-header">
      <div class="inner-page-header">
        <h1>Category: Cars</h1>
      </div>
    </div>
```


After copying the HTML for the page header into the `category.html` file, open the WP full site editor in our browser. Since WordPress doesn’t automatically detect new template files, we need to refresh the page.
At this point, the category template should appear in the full site editor and look similar to the `index.html` template.
Lets add to our `category.html file`the following HTML code, and place it under the `<!-- wp:template-part {"slug":"header","theme":"mytheme","tagName":"header","className":"shadow"} /-->`

```
	<!-- wp:html -->
	<!-- Page Header -->
	<div class="wp-block-mytheme-plus-page-header">
	  <div class="inner-page-header">
	    <h1>Category: Cats</h1>
	  </div>
	</div>
	<!-- /wp:html -->
```

This adds the custom header to our category template.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Necessary templates: Single Post Template](https://developer.wordpress.org/themes/template-files-section/post-template-files/#single-php)

Adding this template to our theme is super important. It's what shows the content for a single post or custom post type.
We can’t fully rely on the index template for this since single posts usually need a unique design. However, we can reuse some elements from the index template in our single post template. <br>

For the correct file name, refer to the [documentation](https://developer.wordpress.org/themes/basics/template-hierarchy/#single-post).   
If we want a "generic" template that works for all posts, the `single.html` template is a great choice. Let’s create a file named `single.html` in the template folder.    

Once we’ve created the `single.html` file, we switch to the WordPress editor. We should see "Single Posts" listed under *Edit Site > Templates > All Templates*. Let’s open it and start adding and customizing blocks to create the design we want.

In single posts, we don’t need a Query Loop block (learn more [here](https://wordpress.org/documentation/article/query-loop-block/)) since the content is already specific to that single post. Blocks that pull post data can do so without a Query Loop block. The single post page is designed to display only one post, so any content blocks will automatically show the relevant post content.

If we built the template without using any loops, the blocks will still render the content correctly, as they inherently know they are displaying data for a single post.    

To display the entire post content, we can insert a block called "Post Content." This block will automatically pull and display the full content of the current post.     

If we want to add links to the previous and next posts (as a kind of pagination), we can create a "Row" block and place the "Previous Post" and "Next Post" blocks inside it. We can use custom styles to style these blocks, as they don’t offer many built-in styling options. These blocks will automatically generate links to the previous and next posts.

To create a comment section for our single post template, it’s a good idea to add a heading that says "Comments" to help visitors identify the section. Under the heading, we can add a "Post Comments" block. WordPress includes a block for building a UI for comments, though the form isn’t easily customizable. This block will perform two actions:   

 - It will display existing comments for the post.
 - It will include a form for submitting a new comment.

A common method to create our `single.html` file is to select all the blocks in the list view panel, copy them, and paste them into the `single.html` file. Then, in WordPress, go to *All Templates > Single Post*. Instead of opening it, click the *options/edit button and select Reset*. In the browser, we should see that the Single Post page is working.


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Necessary templates: Single Page Temaplate](https://developer.wordpress.org/themes/template-files-section/page-template-files/)

The page template is quite similar to the single post template. It’s the template file used to render a static page. Unlike posts, pages won’t include elements like the author’s name, post date, comment count, tags, or links to other posts. Essentially, it will be a simplified version of the single template.   

To create a generic template for all pages, we need to create a file called page.html in the templates directory (see the [documentation](The template file used to render a static page) for details).   

Since the structure is similar to the single.html template, we can copy the content from single.html to page.html. Next, let’s go back to WordPress and, from the All Templates section, select the Pages (or Page) template. Here, we can remove the elements we don’t need—such as the author, date, comment count, and tags. Afterward, we can select all the blocks (from the list view), copy them, and paste them into the page.html file.   
So that's it—our page template is done.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

## [Necessary templates: Custom Page Temaplate](https://developer.wordpress.org/themes/template-files-section/page-template-files/#creating-custom-page-templates-for-global-use)    

Custom templates are similar to the Page template, but they allow for more flexibility and unique options that might not be covered by the standard template hierarchy.   
For instance, we might want to create a template for a full-width page. Custom templates can provide this functionality, giving us more control over the layout and design of specific pages.

WordPress allows users to select custom templates for pages, which is explained in detail in the page template [documentation](https://developer.wordpress.org/themes/basics/template-hierarchy/#single-page). 
The 1st section of the documentation covers custom template files and how they have the highest priority when selecting templates for pages.   
*`custom template file` – The page template assigned to the page. See get_page_templates().*    

To make our custom templates available, we need to register a theme. This can be done through the `theme.json` file in our code editor. The `theme.json` file is useful for registering custom templates at the bottom of the object in an array called `customTemplates`.    
```
	{
	 "$schema": "https://schemas.wp.org/trunk/theme.json",
	  "version": 2,
	  "settings": {・・・
	  },
	"styles": {・・・
	  },
➤	"customTemplates": [
	    {
	      "name": "full-width-page",
	      "title": "Full Width Page",
      	      "postTypes" : [
        	"page"
              ]
	    }
	  ]
	}
```

This array accepts objects, with each object representing a single template.    
To register a custom template, lets add it as an object inside this array with a *name property* (`"name" " "my-name"`).

The name property should be *set to the file name of the custom template without the extension* (e.g., `full-width-page`). If a custom template is specified, WordPress will prioritize this template over the default templates.

With this registration, WordPress will use the custom template whenever it's selected, giving us full control over how specific pages are displayed.   

The next property we need is called "title". This property should be a human-readable name for the template, which will be displayed to users on the front end. For example, we can set the title property to "Full Width Page."

The last property is "postTypes". This property is an array that specifies which post types the template can be applied to. It allows us to restrict the template to specific post types, including custom post types.
Eg. we can pass in the *page post type* to apply this custom template to pages only.

For more details on custom templates in theme.json, [see the it here]((https://developer.wordpress.org/block-editor/how-to-guides/themes/global-settings-and-styles/#customtemplates).    

<br> 

Inside the template folder, let's create a new custom template file called full-width-page.html. The name of this file should match the value we set for the name property in the `theme.json` file.

After that, we can copy the content from `page.html` into `full-width-page.html`. The *full-width page template* will be similar to the *standard page template*, but we’ll remove any elements we don’t want to appear, such as the sidebar.

To do this, we can use the *Full Site Editor*. Go to *All Templates > Full Width Page* and select the Use *Pattern option* to open the template editor. Edit the template by removing unnecessary elements. Once we’ve made the changes, we can select everything in the list view panel, copy it, and paste it `into full-width-page.html`.

*Custom templates don’t get applied automatically; they need to be manually selected by the user.* For this reason, we'll go to the *WordPress Admin dashboard* and open one of the pages. After it open in our browser, on the *right sidebar*, find the **Templates panel**. WordPress will show an option to change the template. Select our custom template from the list and save the page.

![sidebar](https://github.com/user-attachments/assets/231363b6-f59a-4112-b53a-9c02c903203d)


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#15-templates)

<br>

# Plugin Development with JS and React

## [Intro to JS](https://learn.wordpress.org/lesson/javascript/)    

*PHP vs. JavaScript: Key Differences and Similarities*   

*What They Do?*    
- PHP: Runs on the server and creates the initial content of a webpage. Once the page loads, PHP’s job is done until a new request is made.   
- JavaScript: Runs in the browser and makes the page interactive. It can update content, validate forms, and handle media without reloading the page.

*Main Differences*  
- Execution: PHP is server-side, JavaScript is client-side.   
- Page Control: PHP generates static content; JavaScript can change elements on the page in real-time.   
- Updates: PHP needs a new request for changes; JavaScript can update content without a reload.   
- Capabilities: PHP deals with server-side tasks like databases, while JavaScript handles browser-side interactions and dynamic effects.
- Semicolons are optional in JavaScript, whereas in Php it gives an error if we miss it out
  
*What They Have in Common?*   
- Purpose: Both are essential for modern web development—PHP for the back end, JavaScript for the front end.   
- Programming Concepts: Variables, functions, loops, and conditionals are present in both.   
- Extensibility: Both have libraries and frameworks (e.g., PHP’s Laravel, JS’s React).   

*WordPress Example:*      
- WordPress uses PHP to create pages, manage databases, and handle server tasks.   
- JavaScript adds interactivity, like sliders and pop-ups, and helps with client-side form validation.

<br>

**Using the Browser Console for JavaScript**   

*The Console*
- Quick Test Runs: The browser console is great for running 1-2 lines of code quickly. We can open it up, type some JavaScript, and see it run right away.

*The Sources Panel*
- More Complex Coding: If we need to write and test more than a couple of lines of code, the Sources panel is where we go.
- What It Does:   
The Sources panel shows all the files loaded on our site. This is similar to the Network panel, which lists files but focuses on network activity—like tracking requests going in and out of our site.
- Debugging and Editing:    
The Sources panel lets us inspect, modify, and even create files directly in the browser. It’s a powerful tool for debugging our code. It's a great tool for quickly debugging a site without modifying the original code.

<br>

**Using Snippets in the Sources Panel**   
*What Are Snippets?*   
Snippets are perfect for writing and running JavaScript with multiple lines of code. They make it easy to test and debug larger pieces of code without creating a full script file.

*Accessing Snippets*    
To access snippets, click on the double chevron (>>) in the Sources panel. This will open the panel where we can find and manage your snippets.

![snippets](https://github.com/user-attachments/assets/4500409f-dded-4b24-91ff-615b6cc253ea)

  
*Creating and Running a Snippet*   
- Add a New Snippet: Click the New snippet button and name it (e.g., Index.js). The file name can be anything as long as it ends with the .js extension.   
- Write Our Code: Inside the snippet, we can write our JavaScript code. For example, test out an alert function:
  
```
	alert('This is a test!');
```

*To run the code click on the play button or press "⌘ + enter"*   

![test in snippets](https://github.com/user-attachments/assets/454db131-437f-48c3-9857-da0805fc41c6)


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#plugin-development-with-js-and-react)

<br>   

## [Intro to REACT](https://react.dev/learn)      

React is a JavaScript library for building user interfaces.   
To make matters better, WordPress has immense support for React.
to get started with React Node must be installed.   

JavaScript files can get big, so size does matters.     

**Optimizing Code for Production**   
To ensure optimal performance, our HTML, CSS, and JavaScript code should be production-ready. One common method to reduce file size is to compress the code into a single line and remove whitespace, which, while effective, can make the code hard to read. Fortunately, React provides tools to optimize JavaScript code for production.

<br> 

**Getting Started with React**   
To start using React without setting up a local environment, we can use an online tool like [StackBlitz](https://stackblitz.com/edit/react-3p3e9ngy?file=src%2FApp.js). This platform is ideal for testing new libraries and frameworks.

<br>

**React Project Structure**    
A basic React project includes the following files and folders:
 - `public/index.html`
 - `src/App.js`, `src/index.js`, `src/style.css`
 - `package.json`

<br>

**Understanding`package.json`**      
The `package.json` file is essential for managing a React project. It describes the project and its dependencies, ensuring consistency and proper version control.  
Packages can be found on [npm (Node Package Manager)](https://www.npmjs.com/), which is the official site for uploading and downloading third-party libraries.  

<br>

*  **Key properties in package.json include:**   

	The purpose of the **[`package.json`](https://docs.npmjs.com/cli/v7/configuring-npm/package-json)** file is to describe our project.   
	- `"name"`: The name of the project.
	- `"version"`: The current version of the project.
	- `"dependencies"` and `"devDependencies"`: Lists of packages used in the project.
	- `"scripts"`: Custom scripts for running, building, and testing the project.
  
```
	{
	  "name": "react",
	  "version": "0.0.0",
	  "private": true,
	  "dependencies": {
	    "react": "^18.1.0",
	    "react-dom": "^18.1.0"
	  },
	  "scripts": {
	    "start": "react-scripts start",
	    "build": "react-scripts build",
	    "test": "react-scripts test --env=jsdom",
	    "eject": "react-scripts eject"
	  },
	  "devDependencies": {
	    "react-scripts": "latest"
	  }
	}
```

* **dependencies** and **devDependencies**
	- `"dependencies"`:
	    Contains packages required for the app to run in production. Each package is listed as a property with its version number (e.g., `"react": "^18.1.0"`).
	- `"devDependencies"`:
	    Contains packages used for development purposes only, such as build tools and testing libraries. These are not included in the production build.
	eg.:
	```
		"dependencies": {
		  "react": "^18.1.0",
		  "react-dom": "^18.1.0"
		},
		"devDependencies": {
		  "react-scripts": "latest"
		}
	```
 <br> 

**Finding and Installing Packages**

Packages can be found on [npm (Node Package Manager)](https://www.npmjs.com/), the official site for uploading and downloading third-party libraries. To install packages, list them in the dependencies or devDependencies object, and use a package manager like npm or [yarn](https://yarnpkg.com/getting-started) to download them.

Note: React is itself a package and is installed via npm or yarn.

**The `public` directory**   
Here we have the `index.html` file.   
The content of the `index.html` file may not directly reflect what we see on the preview because it serves as the static template for the React app. React dynamically generates the content displayed in the browser.

<br>

**The `src` (source) directory**          
In most projects, it’s a best practice to have a `src` (source) directory to store your application code. This helps keep the app's logic separate from configuration files like `package.json`.      

Within the `src` directory, you'll typically find files such as:   
	  - `App.js`: The main component for your application.    
	  - `style.css`: The CSS file for styling your app.    
	  - `index.js`: The entry point that renders the React application.    

<br> 

* **`index.js`explanation**
	This file renders the React app into the root element of public/index.html and manages what appears in the browser.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#plugin-development-with-js-and-react)

<br>   

## [Creating a React app - discovering the `index.js` file](https://codeburst.io/reactjs-components-basics-e94b29b57de)

In the `src` folder, we can find the `index.js` file.  This is where we start by importing React using the following line of code:   
`import React from 'react'`   

This is similar to PHP's `include` function, which lets us share and reuse code across files, helping to keep projects organized.   

In JavaScript, splitting an application into multiple files is achieved through a system called **modules**.    
*Modules* allow us to share and reuse code between files. Unlike PHP’s simpler `include` function, *JavaScript modules* provide a more advanced and flexible approach, offering better control and scalability for larger projects.

Let’s break down the code `import React from 'react'`:

- `import` statement:    
	This is used to bring in functions or variables from one file into another. In this case, we're importing React from the react library so we can use it in our file.

- `React`:     
	When we import something, we need to specify a name for it (like a variable). In this example, React is the name of what we are importing. Unlike languages like PHP, JavaScript exposes functions from other files through variables. This means we can use the React variable to access functions and features from the React library.

- `from 'react'`:   
	Here, we tell JavaScript where to find the file we're importing. Instead of specifying a path, we just give the name of the package, react. This tells JavaScript to look for a package named react, which is defined in the package.json file. Node.js will automatically find the package for us.

<br> 

We can find functions in React's API ([find it here](https://legacy.reactjs.org/docs/react-api.html)). This page provides a complete list of functions, examples, and descriptions for the package. While React offers many functions, we'll only need one for now.

After the import statement, let's create a variable called `h1`:

```
import React from 'react';

const h1 = React.createElement()
```

The value of `const h1` is the `React.createElement` function. We're using this function to create an element that can be **displayed in the document**.    
The `createElement` function takes 3 arguments:   

```
import React from 'react';

const h1 = React.createElement(
  'h1', null, 'Hello Wordl!'
);
```
- 1st argument:
  	This is the type of the element we want to create. Since we want to create a heading, we use `'h1'`.

- 2nd argument:
	This is where we specify the properties or attributes for the element (like `className`, `id`, etc.). In this case, we don't want any attributes, so we pass `null`.

- 3rd argument:
  	This is the content inside the element. Here, we add the text `'Hello World!'`.

So, we've successfully created an `h1` element with the text `"Hello World!"` using.    
However, this element does not appear on the page. React doesn't automatically insert the element into the page. The element is only created in the memory. It is a good thing because we don't want react to start inserting content wherever it wants. The element must be manually inserted into the document.

<br>

Now that we've created our `h1` element, we need to insert it into the document.    
To do this, we first need to import `ReactDOM`: 

```
import React from 'react';
import ReactDOM from 'react-dom/client';

const h1 = React.createElement(
  'h1', null, 'Hello Wordl!'
);
```

In React, the `React package` helps us manage elements, but it doesn't actually display them on the web page. **To show React elements on the page, we need to use the `ReactDOM package`**.    
This package provides functions to interact with the browser and render elements on the screen. So, for this example, both `React` and `ReactDOM` are required.    

 <br> 
 
Next, **we need to define a root element, a variable called** `rootEl` ***(the main container where our React app will be rendered)***, **to specify where we want to render our element**.
Before rendering, we need to select a location in the DOM. The location is the element with `id="root"`, which we usually define in the HTML file like this: 

`<div id="root"></div>`    
  
We’ll use `document.querySelector` to select this location in the DOM. The `#root` selector refers to the `<div id="root">` element. (React needs to know where to render the app, because it doesn’t automatically know the specific location in the DOM.)

`const rootEl = document.querySelector('#root');`   

So now, our updated code looks like this:

```
import React from 'react';
import ReactDOM from 'react-dom/client';

const h1 = React.createElement(
  'h1', null, 'Hello Wordl!'
);
const rootEl = document.querySelector('#root')
```

Now, since we’ve selected the root element, we’re ready to render our `h1` element inside it.

<br>

Next, we need to tell React to treat the selected element as the **root element** of our application (the `<div id="root">`). To do this, we create a variable called `root`. This variable will store the result of calling `ReactDOM.createRoot`, which takes the `rootEl` (the DOM element we selected earlier) as an argument: 
`const root = ReactDOM.createRoot(rootEl);`

  <br> 
  
Time to start rendering the page.   
Our `root` variable runs a function called `root.render()`. The `render` function is responsible for displaying an element on the page. *It accepts 1 argument — the element created by React*.    
Let’s pass in the `h1` variable.      
Now, the text `"Hello World!"` will be rendered on the page.   
Here’s the full code:

```
import React from 'react';
import ReactDOM from 'react-dom/client';

// Create a React element (an h1 tag with text "Hello World!")
const h1 = React.createElement('h1', null, 'Hello World!');

// Select the root element in the HTML (the div with id="root")
const rootEl = document.querySelector('#root');

// Create the root React DOM container
const root = ReactDOM.createRoot(rootEl);

// Render the h1 element inside the root element
root.render(h1);
```
With this, we’ve successfully created and rendered the simplest React application!

<br>

To render multiple elements in React, we use the `createElement` function, just like we discussed before. For example, creating an `h1` element looks like this: `const h1 = React.createElement('h1', null, 'Hello World!');`    

**Elements with Children:**   

React elements can have child elements. These child elements can be inserted by passing them as an array in the third argument. Let’s see how to convert the third argument into an array.

Here’s how we can do it:
Let's convert the 3rd argument into an array `[]`:   
`const h1 = React.createElement('div', null, [ ]);`
After let's change the `h1` element to a  `div` tag:    
`const div = React.createElement('div', null, []);`     
The variable name will be updated se we need to update the variable name inside the render function:    
`root.render(div);`

**Adding More Elements:**    

Let’s run the React.createElement function a couple more times. We are going to create:
- 1 heading (h1) element.
- 2 paragraph (p) elements.  

Each element will use `null` as the 2nd argument to indicate no attributes.    
For the 3rd argument, we will add text content for each element.
Here’s the full code:  

```
import React from 'react';
import ReactDOM from 'react-dom/client';

// Creating a div that contains a heading and two paragraphs
const div = React.createElement('div', null, [
  React.createElement('h1', null, 'Hi'), // h1 element
  React.createElement('p', null, 'Bonjour'), // First p element
  React.createElement('p', null, 'Szia'), // Second p element
]);

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

// Rendering the div with all child elements
root.render(div);
```
<br>

**Explanation:**  
- `React.createElement('div', null, [...])`:   
	This creates a div element, with the array `[React.createElement('h1', null, 'Hi'), React.createElement('p', null, 'Bonjour'), React.createElement('p', null, 'Szia')]` as its children.
- `React.createElement('h1', null, 'Hi')`:
	This creates an `h1` element with the text `"Hi"`.   
- `React.createElement('p', null, 'Bonjour')` and `React.createElement('p', null, 'Szia')`:    
	These create 2 `p` elements with the texts `"Bonjour"` and `"Szia"`.

When we save and run this code, the page should reflect the changes by rendering the div containing the h1 and the two p elements.

<img width="1297" alt="indexjs" src="https://github.com/user-attachments/assets/bd0ca726-3757-48e0-9cff-dbfa3cee6663">

<br>

The main advantage of using React is its effectiveness in rendering dynamic content.

--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#plugin-development-with-js-and-react)

<br>   

## [Dynamic Content with React]()

Let’s enhance our solution by storing elements inside a function instead of a variable. This is generally a good practice in React, as it helps avoid memory leaks.

**Why Avoid Memory Leaks?**   
Memory leaks happen when an application uses up memory but doesn't release it when it's no longer needed. This can lead to performance issues, especially in larger applications. One common cause of memory leaks in React is storing elements in variables and not clearing them when they are no longer needed.   

Let’s look at a simple example. Imagine we have a login form in our app. We want to check if the user is logged in, and if not, render the `loginForm`. If the form is stored in a variable, it will occupy memory even if the user doesn't need it. This is where a memory leak can occur.
```
const loginForm = React.createElement('form')

if(someCondition) {
  ReactDOM.render(loginForm, document.querySelector("#root"))
}
```
If the user is not logged in, `loginForm` is rendered inside the `#root` element. However, the `loginForm` element is stored in memory as a variable, even if it’s not needed later. This can lead to unnecessary resource usage, especially if the form is no longer required. To avoid this, it's better to only create and render the form when necessary, and clear it from memory when it's no longer needed, preventing potential memory leaks.   

**Better Approach: Using Functions**   
To avoid memory leaks, it's a good practice to store elements inside functions rather than variables. By doing this, elements are only created when needed, and they don't persist in memory when they are no longer required.   
Here’s an updated version of the login form example using a function:

```
function loginForm() {
  return React.createElement('form')
}
if(someCondition) {
  ReactDOM.render(loginForm(), document.querySelector("#root"))
}
```

Now, the form is generated inside the `loginForm()` function, which is called only when needed. Once the form is rendered and no longer necessary, the memory used by the element is freed up automatically. This approach ensures we don’t store unnecessary elements in memory, keeping our app more efficient.

<br>

**Converting our variables to Functions** 

Improve our code by converting the elements into functions.    
This will help us avoid memory leaks and improve performance.     
Here’s the original example (with memory leaks):   

```
import React from 'react';
import ReactDOM from 'react-dom/client';

const div = React.createElement('div', null, [
  React.createElement('h1', null, 'Hi'),
  React.createElement('p', null, 'Bonjour'),
  React.createElement('p', null, 'Szia'),
]);

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

root.render(div);
```

In the original code, we store the content in a `div` variable, which works, but it’s not ideal for dynamic content and could lead to memory leaks. To improve this, we can avoid storing elements in variables and instead place them inside a function. Let’s define a function called `Page()` that will directly return the div elements.   

<br>

Here’s the refactored code:

```
import React from 'react';
import ReactDOM from 'react-dom/client';

function Page() {
  return React.createElement('div', null, [
    React.createElement('h1', null, 'Hi'),
    React.createElement('p', null, 'Bonjour'),
    React.createElement('p', null, 'Szia'),
  ]);
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

root.render(Page());
```
We’ll replace the variable assignment `const div = React.createElement('div', null, [...])` with a return statement return `React.createElement('div', null, [...])`.    
Instead of assigning the `div` element to a variable, we can update the render function to directly call `root.render(Page());` instead of passing the variable.   
This approach ensures the page remains clean, and we’re dynamically rendering the content only when needed.   

Now, we’re using a function instead of a variable, which ensures that the elements are created only when the `Page()` function is called. This is more efficient and reduces the chances of memory leaks.

<br>

**Adding Dynamic Content**

Let’s take this a step further and make the content dynamic. For example, we could display the current time like a clock. Since JavaScript has built-in date objects, we can use `Date()` and its `toLocaleString()` method to display the current time.

Here’s how we can do that inside our `h1` tag using a *[template literal](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-template-literals-template-strings)*.   
So, we should convert the 3rd argument to a template literal``` `React.createElement('h1', null, `Hi ${Date().toLocaleString()}` ```.   
The date function is defined by the JavaScript language, it's automatically available to us.
Here's how to refactor the code:
  
```
import React from 'react';
import ReactDOM from 'react-dom/client';

function Page() {
  return React.createElement('div', null, [
    React.createElement('h1', null, `Hi ${Date().toLocaleString()}`),
    React.createElement('p', null, 'Bonjour'),
    React.createElement('p', null, 'Szia'),
  ]);
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

root.render(Page());
```

In this updated version, the current date and time will be displayed in the `h1` tag. We're using a template literal to dynamically inject the time returned by `Date().toLocaleString()`.   

**Updating the Time Every Second**   

It would be even cooler if the time updated every second. To achieve this, we can use JavaScript’s `setInterval()` function, which allows us to run a block of code at regular intervals.
Let's run a function called `setInterval()`.

```
import React from 'react';
import ReactDOM from 'react-dom/client';

function Page() {
  return React.createElement('div', null, [
    React.createElement('h1', null, `Hi ${Date().toLocaleString()}`),
    React.createElement('p', null, 'Bonjour'),
    React.createElement('p', null, 'Szia'),
  ]);
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(Page());
}, 1000)
```

The `setInterval` function is built into JavaScript. It’s used to run a function at specified intervals.

It takes two arguments:   
- The 1st argument is the function we want to execute repeatedly. We can pass a regular function here, as **it’s completely valid to pass a function to a function**.
	```
	function() {
	  root.render(Page());
	}  
	```
- The 2nd argument is the interval, specified in milliseconds `}, 1000)`, which determines how often the function will run.

  To keep the time updated on the page, we should move the render function inside the `setInterval`. This way, the page is re-rendered every second. 


<img width="1291" alt="tolocaltime" src="https://github.com/user-attachments/assets/b7bf4eb1-02c9-4e68-a7b9-a114373363d4">


**What happens under the hood?**    

Under the hood, React is smart about updates. If an element doesn't need to change, it won’t be re-rendered. React detects that only the time is being updated, so it will only re-render the `h1` element with the new time. The rest of the content, like the paragraphs `p`, stays the same and remains untouched, which makes the update process more efficient.   


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#plugin-development-with-js-and-react)

<br>   

## [Intro to JSX](https://www.geeksforgeeks.org/reactjs-jsx-introduction/)

In our file, we currently use the `React.createElement` function to create elements, which can be unintuitive and hard to read. JSX simplifies this by allowing us to write HTML-like syntax directly in a JavaScript file.

### Webpack and JSX
Before our files are delivered to the browser, they go through a tool called **Webpack**, which bundles and optimizes the code for production. One of Webpack's tasks is to convert JSX into `React.createElement` calls. For example, `<h1>Example</h1>` becomes `React.createElement('h1', null, 'Example')`.

### What is JSX?
JSX is an extension of JavaScript that allows us to write HTML-like code in JavaScript files. It’s not actual HTML, though, so some differences exist. For example, not all HTML attributes are directly usable in JSX.

### Writing JSX
Here's the original code we are working with:

```javascript
import React from 'react';
import ReactDOM from 'react-dom/client';

function Page() {
  return React.createElement('div', null, [
    React.createElement('h1', null, `Hi ${Date().toLocaleString()}`),
    React.createElement('p', null, 'Bonjour'),
    React.createElement('p', null, 'Szia'),
  ]);
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(Page());
}, 1000);
```

First, we will completely replace the return value with a pair of parentheses.

```
import React from 'react';
import ReactDOM from 'react-dom/client';

function Page() {
  return (

  )
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(Page());
}, 1000)
```

We can replace the `React.createElement` calls with JSX syntax. First, wrap the return content in parentheses. Multi-line JSX must be enclosed in parentheses:

```
import React from 'react';
import ReactDOM from 'react-dom/client';

function Page() {
  return (
    <div>
      <h1>Hello World!</h1>
      <p>Hi</p>
      <p>Bonjour</p>
    </div>
  );

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(Page());
}, 1000)
```

JSX makes templates more readable and intuitive. However, JSX requires a single root element. If we remove the `<div>` tag, React throws an error: *"JSX expressions must have one root element."*  

So far, JSX makes writing templates feel intuitive, almost like working with HTML. However, there are some key differences. For instance, JSX requires that **a component returns only 1 root element**. If we remove the `<div>` wrapper from our code, the page will throw an error saying, *"JSX expressions must have one parent element."*    
This is because JSX doesn't allow multiple sibling elements at the top level of a component.  

<br>

**Fragments**  

Sometimes, adding a `<div>` tag just to wrap multiple elements can cause issues, such as breaking our CSS. Fortunately, React offers a solution: **fragments**.   

Fragments are elements that let us group multiple elements without adding an extra tag to the DOM. Written as empty tags,` <> </>`, they help keep our HTML cleaner and avoid unnecessary wrapper elements.

```
import React from 'react';
import ReactDOM from 'react-dom/client';

function Page() {
  return (
    <>
      <h1>Hello World!</h1>
      <p>Hi</p>
      <p>Bonjour</p>
    </>
  )
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(Page());
}, 1000)
```

By using fragments, we can keep our documents clean and avoid unnecessary tags.   
When we inspect the page in the browser, the DOM will look like this:  

```
<div id="root">
  <h1>Hello World!</h1>
  <p>Hi</p>
  <p>Bonjour</p>
</div>
```

<br>

**className**   

In JSX, we can apply CSS classes to elements, but instead of using the standard class attribute, we need to use className. This is because class is a reserved keyword in JavaScript, which can cause conflicts.      

For example, if we want to add a CSS class called green to an `<h1>` tag, we would write: `<h1 className="green">Hello World!</h1>` .    

Using className ensures there’s no confusion with JavaScript’s class keyword, and it works seamlessly with our CSS.    

```
import React from 'react';
import ReactDOM from 'react-dom/client';

function Page() {
  return (
    <>
      <h1 className="green">Hello World!</h1>
      <p>Hi</p>
      <p>Bonjour</p>
    </>
  )
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(Page());
}, 1000)
```

**Apply Styles**    

To style our React components, we can create a CSS file, for example, `src/style.css`.    
Let's add a CSS class to make the `<h1>` tag green:  

```
.green {
  color: green;
}
```

However, this CSS file is not automatically loaded into our application. We have 2 options to include it:  

1. **Link it in the HTML file**   
	Add a `<link>` tag in the `<head>` section of the HTML file to load the CSS.
2. **Import it directly in our JavaScript file**
	Importing the CSS file into our JavaScript file is usually the better choice because Webpack can process CSS alongside JavaScript. To do this, simply we can add the following line to our file: `import './style.css'`.    

With this approach, Webpack will handle the CSS, bundling and optimizing it for production.    
It’s a clean and efficient way to manage your styles in a React project.  

```
import React from 'react';
import ReactDOM from 'react-dom/client';
import './style.css'

function Page() {
  return (
    <>
      <h1 className="green">Hello World!</h1>
      <p>Hi</p>
      <p>Bonjour</p>
    </>
  )
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(Page());
}, 1000)
```

<img width="1074" alt="JSX" src="https://github.com/user-attachments/assets/7effa0bc-d1fd-482b-8be8-d2e87fa18757">


--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#plugin-development-with-js-and-react)

<br>   

## [Components with React](https://react.dev/learn/your-first-component)   

HTML wasn't built to be easily scalable, so you can't split a single page into separate files. React solves this problem with components.   
A **component** is like creating new, custom HTML tags. While browsers already know tags like `<p>` for paragraphs or `<video>` for videos, React lets us define our own tags.   

For example, we can create a `<LoginForm>` component that displays a login form. These components are fully customizable, allowing us to control both how they look and how they behave.   
This approach makes it easier to build and manage complex web pages, as we can reuse components wherever we need them.

**How components are created?**   

Components in React are created using functions.   
The only rule is that the function **must return JSX**. Other than that, React will treat the function as a component.  

To demonstrate, let’s update the render function. Instead of calling the `Page()` function, we'll use a self-closing tag: `<Page />`. If we check the app, we'll see it's still fully functional.   

React automatically recognizes that we're using a custom component. It will look for a function with the same name, execute it, and render the returned JSX.    

```
import React from 'react';
import ReactDOM from 'react-dom/client';
import './style.css'

function Page() {
  return (
    <>
      <h1 className="green">Hello World!</h1>
      <p>Hi</p>
      <p>Bonjour</p>
    </>
  )
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(<Page />);
}, 1000)
```

<br>

**Creating More Components**   

React allows us to create almost unlimited components. Let’s create another one!   

We’ll define a function called `Header()`. It's standard practice to capitalize the name of a component. This helps differentiate custom components from regular HTML elements, which are always lowercase.   

The `Header()` component will be responsible for rendering the `<h1>` tag. We'll move the `<h1>` from the Page component into `Header()` and return it there. If the component only returns one element, we can write it in a single line, which avoids the need for parentheses.    

Back in the `Page` component, we can include the `Header` component by adding a self-closing tag: `<Header />`.

```
	import React from 'react';
	import ReactDOM from 'react-dom/client';
	import './style.css'
	
➤	function Header() {
	  return <h1 className="green">Hello World!</h1>
	}
	
	function Page() {
	  return (
	    <>
➤	      <Header />
	      <p>Hi</p>
	      <p>Bonjour</p>
	    </>
	  )
	}
	
	const rootEl = document.querySelector('#root');
	const root = ReactDOM.createRoot(rootEl);
	
	setInterval(function() {
	  root.render(<Page />);
	}, 1000)
```

<br>

**Dynamic components**    

Let's add a clock to our `Header()` component to display the current time, just like we did in the [previous example](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#dynamic-content-with-react).   

To do this, we create a variable called `const clock`, which stores the result of `Date().toLocaleString()`. This will give us the current date and time.

Now, how do we add this dynamic value to the `<h1>` tag?    
We simply insert the `clock` variable inside the curly brackets `{}`. **In JSX, curly brackets are used to embed JavaScript expressions inside HTML-like code**.
Here’s how we do it: `return <h1 className="green">Hello {clock}</h1>`  

The `{clock}` part will display the current time inside the `<h1>` tag. The clock will automatically update whenever the component re-renders.

```
import React from 'react';
import ReactDOM from 'react-dom/client';
import './style.css'

function Header() {
  const clock = Date().toLocaleString();
  return <h1 className="green">Hello {clock}</h1>
}

function Page() {
  return (
    <>
      <Header />
      <p>Hi</p>
      <p>Bonjour</p>
    </>
  )
}

const rootEl = document.querySelector('#root');
const root = ReactDOM.createRoot(rootEl);

setInterval(function() {
  root.render(<Page />);
}, 1000)
```



--- 

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#plugin-development-with-js-and-react)

<br>   
