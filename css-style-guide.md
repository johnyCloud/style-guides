# CSS Style Guide

[SCSS Style Guide](https://github.com/johnyCloud/style-guides/blob/main/scss-style-guide.md)

## Table of Contents

1. [Declaration Order](#declaration)
1. [Single declarations](#Single_declarations)
1. [Media query placement](#Media_query_placement)
1. [Naming](#naming)
1. [Shorthand notation](#Shorthand_notation)
1. [Class names](#Class_names)
1. [Comments](#comments)
1. [Selectors](#Selectors)

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


## Single_declarations

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

## Media_query_placement
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

## Shorthand_notation

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
## Class_names
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
