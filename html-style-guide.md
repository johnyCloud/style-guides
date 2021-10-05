# HTML Style Guide

[CSS Style Guide](https://github.com/johnyCloud/style-guides/blob/main/css-style-guide.md)
[SCSS Style Guide](https://github.com/johnyCloud/style-guides/blob/main/scss-style-guide.md)

## Table of Contents

1. [Naming](#Use-Lowercase-Element-Names)
1. [Closing Tags](#Close-All-HTML-Elements)
1. [Naming attributes](#Use-Lowercase-Attribute-Names)
1. [Avoid Long Code Lines](#Avoid-Long-Code-Lines)
1. [HTML Comments](#HTML-Comments)


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

## Avoid Long Code Lines
When using an HTML editor, it is NOT convenient to scroll right and left to read the HTML code.

Try to avoid too long code lines.

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
