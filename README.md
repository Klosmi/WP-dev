# PHP Basics to get started

1. [Environment](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#environment)  
2. [PHP basics for WP](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#php)     
3. [PHP variables](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#php-variables)     
4. [Strings and Booleans](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#strings-and-booleans)     
5. [Functions](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#functions)     
6. [Arrays](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#arrays)     
7. [Loops](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#loops)     
8. [Constants](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#constants)     
9. [Comments](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#comments)   
10. [Return values from within a function](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#return-values-from-within-a-function)

<br>

# WP Theme development with PHP

1. [Configuration file - `wp-config.php`](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#configuration-file)      
2. [Files and Folders](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#files-and-folders-of-wordpress)  
3. [File Headers](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#file-headers)      
4. [Additional File Headers](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#additional-file-headers)   
5. [Full-Site Editing](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#full-site-editing-fse)      
6. [Index Template](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#index-template)     
7. [Recreating the index template](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#recreating-the-index-template)     
8. [Language attribute](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#language-attribute)   
9. [Character Set](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#character-set)     
10. [Additional tags](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#additional-tags)    
11. [Body tag](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#body-tag)     
12. [Documentation and sources](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#documentation-and-sources)    
## 13. [Global Styles](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#global-styles)     
-  1. [JSON Schema](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#json-schema)    
-  2. [Changing WP Default Settings (eg.: the color palette)](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#changing-wp-default-settings-eg-the-color-palette)
-  3. [Typography](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#wp-typography---font-settings)     
-  4. [Content width](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#content-width)      
-  5. [Margin and Padding](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#margin-and-padding)
-  6. [Custom Units for margin and padding](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#custom-units-for-margin-and-padding)      
-  7. [Block Gaps](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#block-gaps)      
-  8. [Enabling everything: appearance tools](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#enabling-everything-appearance-tools)
## 14. [Managing Asset Files](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#managing-asset-files)
- 1. [Adding a static template as a theme](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#adding-a-static-template-as-a-theme)   
- 2. [Action Hooks](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#action-hooks)   
- 3. [Writing hooks - functions.php](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#writing-hooks---functionsphp)    
- 4. [Adding a hook](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#adding-a-hook)    
- 5. [Registering styles](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#registering-styles)   
- 6. [Enqueuing styles](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#enqueuing-styles)
- 7. [Loading Additional Head tags](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#loading-additional-head-tags)
## 15. [Templates](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#templates)    
- 1. [Template parts: `header` and `footer`](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#template-part-header-and-footer)
- 2. [Anatomy of a block](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#anatomy-of-a-block)
- 5. [Integrating Custom Templates (templates/index.html) with Gutenberg Editor](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#integrating-custom-templates-templatesindexhtml-with-gutenberg-editor)   
- 4. [Header & Footer optimization](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#header-footer-optimization)
- 5. [Dummy content in WP](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#dummy-content-in-wp)
- 6. [Making a top-bar](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#making-a-top-bar)
- 7. [Modifiny the editor's style by code](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#modifiny-the-editors-style-by-code)
- 8. [Use HTML block to create a custom look](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#use-html-block-to-create-a-custom-look)
- 9. [Formatting Main Content - Columns](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#formatting-main-content---columns)   
- 10. [Rendering posts with the Query Loop Block](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#rendering-posts-with-the-query-loop-block)     
- 11. [WordPress's Template Hiearchy](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#wordpresss-template-hiearchy)    
- 12. [Necessary templates: 404 (NotFound) template](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#necessary-templates-404-notfound-template)
- 13. [Necessary templates: Category Template](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#necessary-templates-category-template)
- 14. [Necessary templates: Single Post Template](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#necessary-templates-single-post-template)
- 15. [Necessary templates: Single Page Temaplate](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#necessary-templates-single-page-temaplate)
- 16. [Necessary templates: Custom Page Temaplate](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#necessary-templates-custom-page-temaplate)

<br>

# [Plugin Development with JS and React](https://developer.wordpress.org/news/2024/03/26/how-to-use-wordpress-react-components-for-plugin-pages/)    

1. [Intro to JS](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#intro-to-js)        
*For a solid understanding of JavaScript fundamentals, I recommend checking out my JS fundamentals use [this link](https://github.com/Klosmi/html-basics?tab=readme-ov-file#javascript--basics).*
2. [Start with React](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#intro-to-react)
3. [Create a React app - discovering the `index.js` file](https://github.com/Klosmi/WP-dev/blob/main/WPDevNotes.md#creating-a-react-app---discovering-the-indexjs-file)
