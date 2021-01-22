![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) **SOFTWARE ENGINEERING IMMERSIVE**

# Sass {Syntactically Awesome Style Sheet}

<img src="https://media.giphy.com/media/xT9IgpernHLP5eWOY0/giphy.gif" alt='awesome rabbit' width="300px" style="border-radius:90%">

## Prerequisites
- Proficiency in CSS
- Proficiency in at a programming language (i.e. Javascript, Ruby or Python)

## Objectives

By the end of this lesson students will be able to:

-   [ ] Setup Sass for their web application
-   [ ] Understand the benefits of Sass
-   [ ] Develop an Application using Sass

<br/>

## What is Sass?

Sass is a feature-rich CSS extension language and pre-processor for creating styled variables, mixins, and modules. Sass also enables CSS selector nesting and inheritance.

It incorporates the basic benefits of programming languages into your style sheets.

<img src="https://media.giphy.com/media/CcwLAV11cALh3OuEJ5/giphy.gif" alt="keep coding" width="300px">

#### Variables
> If you've ever wanted one place to change the font-family or color theme of your app, this is the feature you want to use.

<details>
<summary>Variables Example</summary>

```sass
$helvetica-font: Helvetica, sans-serif
$primary-color: #333

body
  font-family: $helvetica-font
  color: $primary-color
```
</details>

<br/>

#### Mixins 
> If you have ever wanted to share blocks of styling with multiple CSS selectors without repeating CSS Selectors throughout your styles, this is the feature you want to use.

<details>
<summary>Mixins Example</summary>

```sass
=color-box-style($bg-color)
  width: 200px
  height: 200px
  background: $bg-color
  
  .red-box
    +color-box-style(red)
    color: cyan

  .green-box
    +color-box-style(green)
    color: purple
```
</details>

<br/>

#### Functions (from built-in sass modules)
> Incorporate pre-built functions into your styles easily. https://sass-lang.com/documentation/modules

<details>
<summary>Complement Function Example (Color Module)</summary>

```sass
<!-- Mixin -->
=color-box-style($bg-color)
  width: 200px
  height: 200px
  background: $bg-color

<!-- Variables -->
$color-1: red
$color-2: green

<!-- Styles -->
.color-box-1
  +color-box-style($color-1)
  color: complement($color-1) // <- function
.color-box-2
  +color-box-style($color-2)
  color: complement($color-2) // <- function

```
</details>

<br/>

#### THERES SO MUCH MORE
[Sass Docs](https://sass-lang.com/documentation)

<br/>


## Why Develop with Sass?
<img src="./images/why_dog.png" alt="question" width="100px">

- DRY / Organized styles
- Scalable / Modular
- Maintainable
- It's popular!

> Use Variables and Mixins to practice DRY code. When working on larger projects, build smaller - more practical stylesheets that take advantage of nested syntax (grouping like content). @import them into one .sass stylesheet for a modular application. These benefits mean that it becomes easier to manage your application content.

<br/>

### Sass vs CSS

#### HTTP REQUESTS

- Developing with multiple Sass files means the browser still only makes one HTTP request for a stylesheet. Scss outputs all css into one .css file
- Developing with multiple CSS files means the website visitor's browser is making multiple HTTP requests 
- Sass is great for larger projects and teams
- Less syntax
Scss will look more familiar because it uses **{ }** and **;**
- You can customize Bootstrap 4 with Sass. https://getbootstrap.com/docs/5.0/customize/sass/

- **Sass** files end in the _.sass_ extension
- **Scss** files end in the _.scss_ extension

Both need to be compiled to CSS

<br/>

## What is Scss {Sassy CSS}?
> Scss and Sass are essentially the same. Below are some of the differences in syntax.

#### Sass Syntax Example:

```sass
@import "section"

html, body
  margin: 0

.app
  background: blue
  color: white
  height: 100vh
  padding: 15px
  box-sizing: border-box
  display: flex
  flex-direction: column
  align-items: center

  h1 
    font-size: 24px
    font-weight: 700
```

#### Scss Syntax Example:

```scss
@import "section"

html, body{
  margin: 0;
}
.app{
  background: blue;
  color: white;
  height: 100vh;
  padding: 15px;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;

  h1 {
    font-size: 24px;
    font-weight: 700;
  }
}
```

#### CSS Syntax Example:

```css
.section {
  width: 100vw;
  height: 50vh;
  background: black;
  display: flex;
  justify-content: center;
  align-items: center;
}

html, body {
  margin: 0;
}

.app {
  background: blue;
  color: white;
  height: 100vh;
  padding: 15px;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.app h1 {
  font-size: 24px;
  font-weight: 700;
}
```



## Sass styling with bootstrap