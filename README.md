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

#### Functions (built-in modules)
> https://sass-lang.com/documentation/modules

<details>
<summary>Color Module Example (complement function)</summary>

```sass
$color-1: red
$color-2: greem

.color-box-1
  +color-box-style($color-1)
  color: complement($color-1)
.color-box-2
  +color-box-style($color-2)
  color: complement($color-2)

```
</details>

<br/>

#### Inheritance 
> benefit
<details>
<summary>Inheritance Example</summary>

```sass
%message-shared
  border: 1px solid #ccc
  padding: 10px
  color: #333

.message
  @extend %message-shared


.success
  @extend %message-shared
  border-color: green


.error
  @extend %message-shared
  border-color: red

```
</details>

<br/>

## Why would we use Sass?
- DRY styles / Organized
- Scalable / Modular
- Maintainable
- It's famous!

### DRY styling
Extending/ Inheriting Styles 

### Scalable
Import smaller/more practical stylesheets into one stylesheet vs having a large plain CSS imports

- Importing styles via Sass means the browser only makes one HTTP request as it renders your web page
- Importing via basic CSS makes multiple requests if you have multiple style sheets.

### Maintainable
Nested syntax allows for organized styling where you can group styles for sections or components in relation to the box model.

<br/>

## Sass vs Scss vs CSS
CSS
Scss will look more familiar because it uses **{ }** and **;**

- **Sass** files end in the _.sass_ extension
- **Scss** files end in the _.scss_ extension

Both need to be compiled to CSS

<br/>

Sass Syntax Example:

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

Scss Syntax Example:

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

CSS Syntax Example:

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

## Setup
1. Install Sass via the CLI (w/ Homebrew)
    * brew install sass/sass/sass

1. Compile Sass to CSS. 
    * Install a Sass Extension (**Live Sass Compiler**)   
    OR
    * run sass --watch input-file.sass output-file.css

1. 

## Sass styling with bootstrap