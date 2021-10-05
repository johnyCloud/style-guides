# HTML CSS SCSS Style Guide



## Table of Contents



[HTML](#html)
1. [Syntax](#syntax)
1. [Includes](#css-and-javascript-includes)
1. [Naming](#use-lowercase-element-names)
1. [Closing Tags](#close-all-html-elements)
1. [Naming attributes](#use-lowercase-attribute-names)
1. [Attribute order](#Attribute-order)
1. [Avoid Long Code Lines](#avoid-long-code-lines)
1. [HTML Comments](#html-Comments)
1. [Reducing markup](#reducing-markup)


[CSS](#css)
1. [Declaration Order](#declaration)
1. [Single declarations](#Single-declarations)
1. [Media query placement](#media-query-placement)
1. [Shorthand notation](#shorthand-notation)
1. [Class names](#class-names)
1. [Comments](#comments)
1. [Selectors](#selectors)

[SCSS](#scss)
1. [Code Formatting](#code-formatting)
1. [Specificity & Naming](#specificity--naming)
1. [Units](#units)
1. [Ordering](#ordering)

---
# HTML
## Syntax
- Don't capitalize tags, including the doctype.
- Use soft tabs with two spaces—they're the only way to guarantee code renders the same in any environment.
- Nested elements should be indented once (two spaces).
- Always use double quotes, never single quotes, on attributes.
- Don't include a trailing slash in self-closing elements—the HTML5 spec says they're optional.
- Don’t omit optional closing tags (e.g. </li> or </body>).
```html
    <!doctype html>
    <html>
    <head>
        <title>Page title</title>
    </head>
    <body>
        <img src="images/company-logo.png" alt="Company">
        <h1 class="hello-world">Hello, world!</h1>
    </body>
    </html>
```
- [Back To Top](#table-of-contents)
---
## CSS and JavaScript includes
Per HTML5 spec, typically there is no need to specify a type when including CSS and JavaScript files as text/css and text/javascript are their respective defaults.

HTML5 spec links
- [Using link](https://www.w3.org/TR/2011/WD-html5-20110525/semantics.html#the-link-element)
- [Using style](https://www.w3.org/TR/2011/WD-html5-20110525/semantics.html#the-style-element)
- [Using script](https://www.w3.org/TR/2011/WD-html5-20110525/scripting-1html#the-script-element)
```html
    <!-- External CSS -->
    <link rel="stylesheet" href="code-guide.css">

    <!-- In-document CSS -->
    <style>
    /* ... */
    </style>

    <!-- JavaScript -->
    <script src="code-guide.js"></script>
```
- [Back To Top](#table-of-contents)
---
## Use Lowercase Element Names

HTML allows mixing uppercase and lowercase letters in element names.

However, we recommend using lowercase element names, because:

- Mixing uppercase and lowercase names looks bad
- Developers normally use lowercase names
- Lowercase looks cleaner
- Lowercase is easier to write

```html
<!-- Good -->
<body>
    <p>This is a paragraph.</p>
</body>

<!-- Bad -->
<BODY>
    <P>This is a paragraph.</P>
</BODY>
```
- [Back To Top](#table-of-contents)
---
## Close All HTML Elements
In HTML, you do not have to close all elements (for example the <p> element).
However, we strongly recommend closing all HTML elements, like this:


```html
<!-- Good -->
<section>
  <p>This is a paragraph.</p>
  <p>This is a paragraph.</p>
</section>

<!-- Bad -->
<section>
  <p>This is a paragraph.
  <p>This is a paragraph.
</section>
```
- [Back To Top](#table-of-contents)
---
## Use Lowercase Attribute Names
HTML allows mixing uppercase and lowercase letters in attribute names.

However, we recommend using lowercase attribute names, because:

- Mixing uppercase and lowercase names looks bad
- Developers normally use lowercase names
- Lowercase look cleaner
- Lowercase are easier to write

```html
<!-- Good -->
<a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a>
<!-- Bad -->
<a HREF="https://www.w3schools.com/html/">Visit our HTML tutorial</a>
```
- [Back To Top](#table-of-contents)
---
## Attribute order
HTML attributes should come in this particular order for easier reading of code.

- class
- id, name
- data-*
- src, for, type, href, value
- title, alt
- role, aria-*

  Classes make for great reusable components, so they come first. Ids are more specific and should be used sparingly (e.g., for in-page bookmarks), so they come second.

```html
    <a class="..." id="..." data-toggle="modal" href="#">
    Example link
    </a>

    <input class="form-control" type="text">

    <img src="..." alt="...">
```
- [Back To Top](#table-of-contents)
---
## Avoid Long Code Lines
When using an HTML editor, it is NOT convenient to scroll right and left to read the HTML code.

Try to avoid too long code lines.
- [Back To Top](#table-of-contents)
---
## HTML Comments

Short comments should be written on one line, like this:
```html
<!-- This is a comment -->
```
Comments that spans more than one line, should be written like this:
```html
<!--
  This is a long comment example. This is a long comment example.
  This is a long comment example. This is a long comment example.
-->
```
- [Back To Top](#table-of-contents)
---
## Reducing markup

- Whenever possible, avoid superfluous parent elements when writing HTML. 
Many times this requires iteration and refactoring, but produces less HTML.
Take the following example:

```html
    <!-- Not so great -->
    <span class="avatar">
    <img src="...">
    </span>

    <!-- Better -->
    <img class="avatar" src="...">
```
- [Back To Top](#table-of-contents)
---
# CSS
## Syntax
* Use soft tabs with two spaces—they're the only way to guarantee code renders the same in any environment.
* When grouping selectors, keep individual selectors to a single line.
* Include one space before the opening brace of declaration blocks for legibility.
* Place closing braces of declaration blocks on a new line.
* Include one space after : for each declaration.
* Each declaration should appear on its own line for more accurate error reporting.
* End all declarations with a semi-colon. The last declaration's is optional, but your code is more error prone without it.
* Comma-separated property values should include a space after each comma (e.g., box-shadow).
* Don't include spaces after commas within rgb(), rgba(), hsl(), hsla(), or rect() values. This helps differentiate multiple color values (comma, no space) from multiple property values (comma with space).
* Don't prefix property values or color parameters with a leading zero (e.g., .5 instead of 0.5 and -.5px instead of -0.5px).
* Lowercase all hex values, e.g., #fff. Lowercase letters are much easier to discern when scanning a document as they tend to have more unique shapes.
* Use shorthand hex values where available, e.g., #fff instead of #ffffff.
* Quote attribute values in selectors, e.g., input[type="text"]. They’re only optional in some cases, and it’s a good practice for consistency.
* Avoid specifying units for zero values, e.g., margin: 0; instead of margin: 0px;.

```css
  /* Bad CSS */
  .selector, .selector-secondary, .selector[type=text] {
    padding:15px;
    margin:0px 0px 15px;
    background-color:rgba(0, 0, 0, 0.5);
    box-shadow:0px 1px 2px #CCC,inset 0 1px 0 #FFFFFF
  }

  /* Good CSS */
  .selector,
  .selector-secondary,
  .selector[type="text"] {
    padding: 15px;
    margin-bottom: 15px;
    background-color: rgba(0,0,0,.5);
    box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #fff;
  }
```
---
## Declaration 

Related property declarations should be grouped together following the order:
- 1.Positioning
- 2.Box model
- 3.Typographic
- 4.Visual
- 5.Misc


> Reason: If you know the order, you save time finding them.

```css
    .declaration-order {
        /* Positioning */
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        z-index: 100;

        /* Box-model */
        display: block;
        float: right;
        width: 100px;
        height: 100px;

        /* Typography */
        font: normal 13px "Helvetica Neue", sans-serif;
        line-height: 1.5;
        color: #333;
        text-align: center;

        /* Visual */
        background-color: #f5f5f5;
        border: 1px solid #e5e5e5;
        border-radius: 3px;

        /* Misc */
        opacity: 1;
    }
```
- [Back To Top](#table-of-contents)

## Single declarations

In instances where a rule set includes only one declaration, consider removing
line breaks for readability and faster editing. Any rule set with multiple
declarations should be split to separate lines.

>Reason: The key factor here is error detection—e.g., a CSS validator stating you have
    a syntax error on Line 183. With a single declaration, there's no missing it.
    With multiple declarations, separate lines is a must for your sanity.

```css
    /* Single declarations on one line */
    .span1 { width: 60px; }
    .span2 { width: 140px; }
    .span3 { width: 220px; }

    /* Multiple declarations, one per line */
    .sprite {
        display: inline-block;
        width: 16px;
        height: 15px;
        background-image: url("../img/sprite.png");
    }
    .icon           { background-position: 0 0; }
    .icon-home      { background-position: 0 -20px; }
    .icon-account   { background-position: 0 -40px; }
```
- [Back To Top](#table-of-contents)
---
## Media query placement
Place media queries as close to their relevant rule sets whenever possible. 
Don't bundle them    all in a separate stylesheet or at the end of the document. 
    
> Reason: Doing so only makes it easier for    folks to miss them in the future.
Here's a typical setup.

```css
    .element { ... }
    .element-avatar { ... }
    .element-selected { ... }

    @media (min-width: 480px) {
    .element { ...}
    .element-avatar { ... }
    .element-selected { ... }
    }
```
- [Back To Top](#table-of-contents)
---
## Shorthand notation

Limit shorthand declaration usage to instances where you must 
explicitly set all available values. Frequently overused shorthand properties include:

```css
    /* Bad example */
    .element {
        margin: 0 0 10px;
        background: red;
        background: url("image.jpg");
        border-radius: 3px 3px 0 0;
    }

    /* Good example */
    .element {
        margin-bottom: 10px;
        background-color: red;
        background-image: url("image.jpg");
        border-top-left-radius: 3px;
        border-top-right-radius: 3px;
    }
```
- [Back To Top](#table-of-contents)
---
## Class names
Keep classes lowercase and use dashes (not underscores or camelCase).
Dashes serve as natural breaks in related class (e.g., .btn and .btn-danger).

Avoid excessive and arbitrary shorthand notation.
.btn is useful for button, but .s doesn't mean anything.
Keep classes as short and succinct as possible.

Use meaningful names; use structural or purposeful names over presentational.

Prefix classes based on the closest parent or base class.
Use .js-* classes to denote behavior (as opposed to style), but keep these classes out of your CSS.
It's also useful to apply many of these same rules when creating Sass and Less variable names.
>Reason: To make clear to what elemnt  is attributed this class.

```css
    /* Bad example */
    .t { ... }
    .red { ... }
    .header { ... }

    /* Good example */
    .tweet { ... }
    .important { ... }
    .tweet-header { ... }
```
- [Back To Top](#table-of-contents)
---
## Comments

Code is written and maintained by people. Ensure your code is descriptive, 
well commented, and   approachable by others. 

Great code comments convey context or purpose. 
Do    not simply reiterate a component or class name.

Be sure to write in complete sentences for larger comments and succinct phrases for general notes.
    
  > Reason:  To make clear to your team what this code does.

```css
    /* Bad example */
    /* Modal header */
    .modal-header {
    ...
    }

    /* Good example */
    /* Wrapping element for .modal-title and .modal-close */
    .modal-header {
    ...
    }
```
- [Back To Top](#table-of-contents)
---
    
## Selectors
Use classes over generic element tag for optimum rendering performance.
  
Avoid using several attribute selectors (e.g., [class^="..."])
on commonly occuring components. Browser performance is known to be impacted by these.

Keep selectors short and strive to limit the number of elements in each selector to three.
Scope classes to the closest parent only when necessary (e.g., when not using prefixed classes).

```css
    /* Bad example */
    span { ... }
    .page-container #stream .stream-item .tweet .tweet-header .username { ... }
    .avatar { ... }

    /* Good example */
    .avatar { ... }
    .tweet-header .username { ... }
    .tweet .avatar { ... }
```
- [Back To Top](#table-of-contents)
---
# SCSS
## Code Formatting

### Declaractions

* Use soft tabs with a two space indent
* A selector should have a single space between the name and the `{`
* A property should have a single space between the `:` and the value
* There should be only one property per line
* Unrelated or non-sequenced selectors should have a single new line between them
* Colors should be specified in hex or rgba values
* Hex values should be in lowercase and use shorthand if possible (e.g., `#fff`)
* rgba values should utilize SASS conversion to maintain the hex value (e.g., `rgba(#fff, 0.5)`)
* Comma-separated values should have a single space after the `,` if they appear on a single line
* Multiple comma-separated property values should appear indented on multiple lines with one declaration per line
* Decimal values should start with a leading number before the `.` (e.g., `0.5`)
* Psuedo selectors and elements should be denoted using a single `:` (e.g., `:hover`, `:before`)
* Vendor prefixes should be taken care of by an [autoprefixer](https://github.com/postcss/autoprefixer)
* Use single quotes (e.g, `'foo'`)
* Do not specify units for zero-values (e.g, `margin: 0`)
* Single property declarations should appear on a single line
* Multi property declarations should appear on multiple lines with one rule per line
* Mixins without properties should omit the `()` (e.g., `@include my-mixin`)
* Avoid the use of SASS color functions (e.g., `lighten(#000)`)
* Avoid the use of `!important`

### Comments

* Use the SCSS comment syntax (`//`) for all comments
* Use comment headings appropriately

### Example

```scss
//
// This is a comment heading
//

//
// This is a comment block heading
//
// Iaculis velit a laoreet consectetur mollis dignissim diam fringilla,
// commodo vulputate turpis dis praesent lacus lorem, justo accumsan
// platea scelerisque pharetra viverra id.

// This is a good example
.foo,
.bar {
  position: absolute;
  display: block;
  font-family: 'Times New Roman', serif; // This is another good example
  font-size: 20px;
  color: #000;
  text-shadow:
    0 1px 2px #ddd,
    0 2px 2px #aaa;
  content: 'Hello world';
  background: rgba(#fff, 0.15);
  box-shadow: 0 0 10px 0 #000;
}

.foobar {
  color: #fff;

  &:hover { text-decoration: underline; }

  &:active { font-weight: bold; }
}

.biz { font-size: 16px; }
.baz { font-size: 24px; }
```
- [Back To Top](#table-of-contents)
---
## Units

* Use `px` for things that should scale in a fixed manner
* Use `rem` for things that should scale with the root `font-size`
* Use `em` for things that should scale with the element `font-size`
* Use `%` for things that should scale with the parent element
* Use `vw` and `vh` for things that should scale with the viewport
* `line-height` should be a unitless multiplier of `font-size`

- [Back To Top](#table-of-contents)
---
## Specificity & Naming

### Rule Specificity

Rules and properties should only be as specific as they need to be. Ideally, your selectors should maintain a flat structure.

```scss
// Bad 🙁
.grandparent .parent .my-selector {
  ...
}

// Good 😀
.my-selector {
  ...
}
```

### Selectors

* Always use class selectors
* Do not use ID selectors
* Do not use type selectors
* Do not mix class selectors with ID or type selectors
* Use attribute selectors wisely

Adhering to these guidelines _increases_ the amount of style resuability and _reduces_ the amount of overriding that needs to be done in the CSS codebase.

```scss
// Bad 🙁
div {
  ...
}

div.my-selector {
  ...
}

#my-selector {
  ...
}

// Good 😀
.my-selector {
  ...
}
```

### Naming Conventions

Rules should be named semantically so that someone looking at just the markup should be able to determine what that rule is going to do.

* Use BEM style for components
* Use kebab-case for multiple words (e.g., `.my-block`)
* Use two underscores (`__`) to separate blocks from elements (e.g., `.my-block__my-element`)
* Use two dashes (`--`) to separate modifiers from blocks or elements (e.g., `.my-block--my-modifier` or `.my-block__my-element--my-modifier`)

```scss
// Component Classes
.media {
  ...

  &-object {
    ...

    &-reversed { ... }
  }

  &-body {
    ...
  }
}

// Utility Classes
.text-sm { ... }
.text-md { ... }
.text-lg { ... }
```

Class names are broken down first into a block (`.media`). Then, into elements (`.media__object` and `.media__body`). And finally into modifiers (`.media__object--reversed`).

### Nesting

While nesting is a great feature of SASS, it can easily make things much more complex and hard to digest. Nesting should be limited to 3 levels or less.

### Extending

While extending selectors (`@extend`) is a great feature of SASS, it can easily make the output CSS much more complex and hard to digest so it is best to avoid using them. More often than not, it would make more sense to pull something out into a mixin rather than use an extend.

### Shorthand

Limit the use of shorthand declarations if you do not need to explicitly set additional declarations.

```scss
// Bad 🙁
.my-selector {
  margin: 10px 0 0 0;
  border-radius: 4px 0 0 0;
}

// Good 😀
.my-selector {
  margin-top: 10px;
  border-top-left-radius: 4px;
}
```

### Media Queries

SASS allows media queries to be nested inside of a selector. This can make our code very easy to digest when working in responsive styles.

```scss
.my-selector {
  ...

  @media (min-width: 1024px) {
    ...
  }
}
```

### Variables

SASS variables should be used wherever a property value may need to be repeated across the codebase (e.g., color values, breakpoints).

* Use kebab-case (e.g., `$color-white`)
* Use semantic naming conventions

```scss
// Bad 🙁
$alpha: #000;
$beta: #fff;

// Good 😀
$color-black: #000;
$color-white: #fff;
```

- [Back To Top](#table-of-contents)
---
## Ordering

* Order side values by `top`, `right`, `bottom`, `left`
* Declare mixins first, then regular properties
* Psuedo selectors should come before other selectors

```scss
.my-block {
  @include my-mixin;

  // Positioning
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 10;

  // Box Model
  box-sizing: border-box;
  display: block;
  width: 100px;
  height: 100px;
  padding-top: 10px;
  padding-bottom: 10px;
  margin: 10px;
  overflow: hidden;

  // Typography
  font-family: 'Times New Roman', serif;
  font-size: 1rem;
  font-style: italic;
  font-weight: bold;
  line-height: 1.5;
  color: #000;
  text-align: center;
  text-decoration: underline;
  text-shadow: 0 1px 0 #fff;
  text-transform: uppercase;

  // Accessibility & Interaction
  cursor: pointer;

  // Background & Borders
  background: #aaa;
  border: 10px solid #000;
  box-shadow: 0 0 10px #000;

  // Transitions & Animations
  transition: all 100ms ease;

  &:before { ... }

  &:hover { ... }

  &-my-modifier { ... }

  &-my-element { ... }
}
```
- [Back To Top](#table-of-contents)
---
