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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

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

### addig [scripts](https://developer.wordpress.org/reference/functions/wp_footer/)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>  

## [Changing WP default settings](https://fullsiteediting.com/lessons/theme-json-color-options/#h-what-color-values-can-you-use-in-theme-json) eg. the color palette
[adding color to the defalult palette](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#adding-color-to-the-defalult-palette)   
[color palette or css properties](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#color-palette-or-css-properties)        
[custom colors](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#custom-colors)      
[duotone colors](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#dutone-colors)      
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


### [Dutone colors](https://fullsiteediting.com/lessons/theme-json-color-options/#h-how-to-add-duotone-colors)   

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

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

[⬅️ back to the table of contents](https://github.com/Klosmi/WP-dev/blob/main/README.md#wp-theme-development-with-php)

<br>

# [Managing Asset Files](https://developer.wordpress.org/plugins/wordpress-org/plugin-assets/)
