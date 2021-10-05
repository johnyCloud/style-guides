# HTML Style Guide

All rules and guidelines in this document apply to HTML files.

> The keywords "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt).

**Icon Legend**:

`·` Space, `⇥` Tab, `↵` Enter/Return

<!-- ---------------------------------------------------------------------- -->

## Table of Contents

1. [**Files**](#1-files)
	1. [File Format](#file-format)
	2. [Filename](#filename)
2. [**Document**](#2-document)
	1. Doctype
	2. Language
	3. Character Encoding
	4. Viewport
	5. Head and Body
3. [**Comments**](#3-comments)
	1. [Single-line Comments](#1-single-line-comments)
	2. [Multi-line Comments](#2-multi-line-comments)
	3. [Closing Tag Comments](#3-closing-tag-comments)
	4. [Sensitive Information](#4-sensitive-information)
4. [**Formatting**](#4-formatting)
	1. [Line Indentation](#1-line-indentation)
	2. [Direct Child Elements](#2-direct-child-elements)
	3. [Block, List and Table Elements](#3-block-list-and-table-elements)
	4. [Trailing Whitespace](#4-trailing-whitespace)
	5. [Elements and Attributes](#5-elements-and-attributes)
5. [**Elements and Attributes**](#5-elements-and-attributes)
	1. [Self-closing Elements](#1-self-closing-elements)
	2. [Optional Open/Close Tags](#2-optional-openclose-tags)
	3. [Attribute Values](#3-attribute-values)
	4. [Attribute Booleans](#4-attribute-booleans)
	5. [Type and Language Attribute](#5-type-and-language-attribute)
	6. [Type Attribute](#6-type-attribute)
	7. [Protocol](#7-protocol)
6. [**Best Practices**](#6-best-practices)
	1. [Structures, Styles and Scripts](#1-structures-styles-and-scripts)
	2. [Valid HTML](#2-valid-html)
	3. [Semantic HTML](#3-semantic-html)
	4. [Form Field Labels](#4-form-field-labels)
	5. [Form Field Names](#5-form-field-names)
	6. [Entity References](#6-entity-references)

<!-- ---------------------------------------------------------------------- -->

## 1. Files

This section describes the format and naming convention of HTML files.

#### File Format

1. **Character encoding** MUST be set to UTF-8 without BOM
	* Sublime.app &rarr; `File` &#8250; `Save with Encoding` &#8250; `UTF-8`
2. **Line endings** MUST be set to Unix (LF)
	* Sublime.app &rarr; `View` &#8250; `Line Endings` &#8250; `Unix`

#### Filename

1. **Letters** MUST be all lowercase
	* e.g. `sidebar.html`, `sidebar.php`
2. **Words** MUST be separated with a hyphen
	* e.g. `social-media-widget.html`, `social-media-widget.php`

&#9650; [Table of Contents](#table-of-contents)

<!-- ---------------------------------------------------------------------- -->

## 2. Document

This section showcases the main elements required in a complete HTML file.

1. **Doctype** MUST be specified and SHOULD be HTML5
	* e.g. `<!DOCTYPE html>`
2. **Language** MUST be defined in the `html` element
	* e.g. `<html lang="en">`
3. **Character encoding** MUST be defined as early as possible
	* e.g. `<meta charset="utf-8">`
4. **Viewport** MUST be included
	* e.g. `<meta name="viewport" content="width=device-width, user-scalable=no">`
5. **Head and body** elements MUST be included
	* e.g. `<head></head><body></body>`

&#9650; [Table of Contents](#table-of-contents)

<!-- ------------------------------ -->

#### Example

<pre lang=html>
&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;en&quot;&gt;
&lt;head&gt;
	&lt;title&gt;Welcome&lt;/title&gt;
	&lt;meta charset=&quot;utf-8&quot;&gt;
	&lt;meta name=&quot;viewport&quot; content=&quot;width=device-width, user-scalable=no&quot;&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;h1&gt;Welcome&lt;/h1&gt;
&lt;p&gt;This is a skeleton document.&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

&#9650; [Document](#2-document)

<!-- ---------------------------------------------------------------------- -->

## 3. Comments

This section describes how comments should be formatted and used.

1. [**Single-line comments**](#1-single-line-comments) MUST be on one line and text inside MUST be surrounded by spaces
	* e.g. `<!-- This is a comment -->`
2. [**Multi-line comments**](#2-multi-line-comments) MUST start and end on their own line and text MUST NOT be indented
	* i.e. `<!--` `↵` `Line number one` `↵` `Line number two` `↵` `-->`
3. [**Closing tag comments**](#3-closing-tag-comments) SHOULD include the class or ID symbol and name
	* e.g. `</div><!-- #main-wrapper -->`
4. [**Sensitive information**](#4-sensitive-information) MUST NOT be placed in a comment
	* e.g. `<!-- Sends email to user@domain.com -->`

&#9650; [Table of Contents](#table-of-contents)

<!-- ------------------------------ -->

### 1. Single-line Comments

Single-line comments MUST be on one line and text inside MUST be surrounded by spaces.

#### &#10006; Incorrect

<pre lang=html>
&lt;!--
This is a comment
--&gt;
</pre>

&#8627; Incorrect because `<!--`, `This is a comment` and `-->` should be one line.

<pre lang=html>
&lt;!--This is a comment--&gt;
</pre>

&#8627; Incorrect because there is no space before or after `This is a comment`.

#### &#10004; Correct

<pre lang=html>
&lt;!-- This is a comment --&gt;
</pre>

&#9650; [Comments](#3-comments)

<!-- ------------------------------ -->

### 2. Multi-line Comments

Multi-line comments MUST start and end on their own line and text MUST NOT be indented.

#### &#10006; Incorrect

<pre lang=html>
&lt;!-- This is a comment
that spans multiple lines
--&gt;
</pre>

&#8627; Incorrect because `<!--` and `This is a comment` are on one line.

<pre lang=html>
&lt;!--
	This is a comment
	that spans multiple lines
--&gt;
</pre>

&#8627; Incorrect because `This is a comment` and `that spans multiple lines` are indented.

#### &#10004; Correct

<pre lang=html>
&lt;!--
This is a comment
that spans multiple lines
--&gt;
</pre>

&#9650; [Comments](#3-comments)

<!-- ------------------------------ -->

### 3. Closing Tag Comments

Closing tag comments SHOULD include the class or ID symbol and name.

#### &#10006; Incorrect

<pre lang=html>
&lt;div id=&quot;main-wrapper&quot;&gt;
	...
&lt;/div&gt;&lt;!-- main-wrapper --&gt;
</pre>

&#8627; Incorrect because `#` prefix is missing.

<pre lang=html>
&lt;div id=&quot;main-wrapper&quot;&gt;
	...
&lt;/div&gt;&lt;!-- .main-wrapper --&gt;
</pre>

&#8627; Incorrect because `main-wrapper` is prefixed with `.` instead of `#`.

#### &#10004; Correct

<pre lang=html>
&lt;div id=&quot;main-wrapper&quot;&gt;
	...
&lt;/div&gt;&lt;!-- #main-wrapper --&gt;
</pre>

&#9650; [Comments](#3-comments)

<!-- ------------------------------ -->

### 4. Sensitive Information

Sensitive information MUST NOT be placed in a comment.

#### &#10006; Incorrect

<pre lang=html>
&lt;!-- Generated by some_php_function() --&gt;
</pre>

&#8627; Incorrect because comment reveals that markup comes from `some_php_function()`.

&#9650; [Comments](#3-comments)

<!-- ---------------------------------------------------------------------- -->

## 4. Formatting

This section outline various, general formatting rules related to whitespace and text.

1. [**Line indentation**](#1-line-indentation) MUST be accomplished using tabs
	* i.e. `<ul>` `↵` `⇥` `<li>`
2. [**Direct child elements**](#2-direct-child-elements) within `html`, `body`, `style` or `script` element MUST NOT be indented
	* i.e. `<body>` `↵` `<h1></h1>` `↵` `</body>`, `<head>` `↵` `⇥` `...` `</head>`
3. [**Block, list and table elements**](#3-block-list-and-table-elements) MUST start on a new line and their children MUST be indented
	* i.e. `<div>` `↵` `⇥` `<h1>`, `<table>` `↵` `⇥` `<th>`
4. [**Trailing whitespace**](#4-trailing-whitespace) MUST NOT be present
	* i.e. no `<p></p>` `·` `·` `↵`
5. [**Elements and attributes**](#5-elements-and-attributes) MUST be all lowercase
	* e.g. `<a href="" title="">`, `<link rel="stylesheet" href="">`

&#9650; [Table of Contents](#table-of-contents)

<!-- ------------------------------ -->

### 1. Line Indentation

Line indentation MUST be accomplished using tabs.

#### &#10006; Incorrect

<pre lang=html>
&lt;ul&gt;
  &lt;li&gt;Item number one&lt;/li&gt;
  &lt;li&gt;Item number two&lt;/li&gt;
&lt;/ul&gt;
</pre>

&#8627; Incorrect because `<li>` is indented with spaces instead of tabs.

#### &#10004; Correct

<pre lang=html>
&lt;ul&gt;
	&lt;li&gt;Item number one&lt;/li&gt;
	&lt;li&gt;Item number two&lt;/li&gt;
&lt;/ul&gt;
</pre>

&#9650; [Formatting](#4-formatting)

<!-- ------------------------------ -->

### 2. Direct Child Elements

Direct child elements within `html`, `body`, `style` or `script` element MUST NOT be indented.

#### &#10006; Incorrect

<pre lang=html>
&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;en&quot;&gt;
	&lt;head&gt;
		&lt;title&gt;Welcome&lt;/title&gt;
		&lt;meta charset=&quot;utf-8&quot;&gt;
		&lt;style&gt;
			#main-wrapper {
				width: 960px;
			}
		&lt;/style&gt;
		&lt;script&gt;
			function show_alert() {
				
			}
		&lt;/script&gt;
	&lt;/head&gt;
	&lt;body&gt;
		&lt;div id=&quot;main-wrapper&quot;&gt;
			&lt;h1&gt;Welcome&lt;/h1&gt;
			&lt;p&gt;This is a skeleton document.&lt;/p&gt;
		&lt;/div&gt;
	&lt;/body&gt;
&lt;/html&gt;
</pre>

&#8627; Incorrect because `<head>`, `<body>` and `<div>` are indented.<br />
&#8627; Incorrect because contents within `<style>` and `<script>` are indented.

#### &#10004; Correct

<pre lang=html>
&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;en&quot;&gt;
&lt;head&gt;
	&lt;title&gt;Welcome&lt;/title&gt;
	&lt;meta charset=&quot;utf-8&quot;&gt;
	&lt;style&gt;
	#main-wrapper {
		width: 960px;
	}
	&lt;/style&gt;
	&lt;script&gt;
	function show_alert() {
		
	}
	&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div id=&quot;main-wrapper&quot;&gt;
	&lt;h1&gt;Welcome&lt;/h1&gt;
	&lt;p&gt;This is a skeleton document.&lt;/p&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

&#9650; [Formatting](#4-formatting)

<!-- ------------------------------ -->

### 3. Block, List and Table Elements

Block, list and table elements MUST start on a new line and their children MUST be indented.

#### &#10006; Incorrect

<pre lang=html>
&lt;div&gt;&lt;p&gt;This is a paragraph.&lt;/p&gt;&lt;/div&gt;

&lt;ul&gt;&lt;li&gt;Item one&lt;/li&gt;&lt;li&gt;Item two&lt;/li&gt;&lt;/ul&gt;

&lt;table&gt;&lt;tr&gt;&lt;th&gt;Header&lt;/th&gt;&lt;/tr&gt;&lt;tr&gt;&lt;td&gt;Content&lt;/td&gt;&lt;/tr&gt;&lt;/table&gt;
</pre>

&#8627; Incorrect because `<div>`, `<ul>`, `<table>` and`<tr>` are not on their own line.<br />
&#8627; Incorrect because `<p>`, `<li>`, `<tr>` and `<td>`are not indented.

#### &#10004; Correct

<pre lang=html>
&lt;div&gt;
	&lt;p&gt;This is a paragraph.&lt;/p&gt;
&lt;/div&gt;

&lt;ul&gt;
	&lt;li&gt;Item one&lt;/li&gt;
	&lt;li&gt;Item two&lt;/li&gt;
&lt;/ul&gt;

&lt;table&gt;
	&lt;tr&gt;
		&lt;th&gt;Header&lt;/th&gt;
	&lt;/tr&gt;
	&lt;tr&gt;
		&lt;td&gt;Content&lt;/td&gt;
	&lt;/tr&gt;
&lt;/table&gt;
</pre>

&#9650; [Formatting](#4-formatting)

<!-- ------------------------------ -->

### 4. Trailing Whitespace

Trailing whitespace MUST NOT be present.

#### &#10006; Incorrect

<pre lang=html>
&lt;p&gt;This is a paragraph.&lt;/p&gt;   
</pre>

&#8627; Incorrect because there are spaces after `</p>`.

#### &#10004; Correct

<pre lang=html>
&lt;p&gt;This is a paragraph.&lt;/p&gt;
</pre>

&#9650; [Formatting](#4-formatting)

<!-- ------------------------------ -->

### 5. Elements and Attributes

Elements and attributes MUST be all lowercase.

#### &#10006; Incorrect

<pre lang=html>
&lt;div ID=&quot;mainWrapper&quot; class=&quot;DESKTOP&quot;&gt;
	&lt;P&gt;This is a paragraph&lt;/P&gt;
&lt;/div&gt;
</pre>

&#8627; Incorrect because `ID`, `mainWrapper`, `DESKTOP` and `<P>` are not lowercase.

#### &#10004; Correct

<pre lang=html>
&lt;div id=&quot;main-wrapper&quot; class=&quot;desktop&quot;&gt;
	&lt;p&gt;This is a paragraph&lt;/p&gt;
&lt;/div&gt;
</pre>

&#9650; [Formatting](#4-formatting)

<!-- ---------------------------------------------------------------------- -->

## 5. Elements and Attributes

This section addresses how to utilize elements and attributes.

1. [**Self-closing elements**](#1-self-encloding-elements) MUST NOT be closed
	* e.g. `<br>`, `<link rel="stylesheet" href="">`
2. [**Optional open/close tags**](#2-optional-openclose-tags) MUST be included
	* e.g. `<ul><li></li></ul>`
3. [**Attribute values**](#3-attribute-values) MUST be wrapped in double quotation marks
	* e.g. `<a href="" title="">Link</a>`
4. [**Attribute booleans**](#4-attribute-booleans) SHOULD NOT include a value
	* e.g. `<input type="text" name="" autofocus>`
5. [**Type and language attribute**](#5-type-and-language-attribute) MUST be omitted on `script` tags
	* e.g. `<script src=""></script>`
6. [**Type attribute**](#6-type-attribute) MUST be omitted on `link` and `style` tags
	* e.g. `<style src=""></script>`
7. [**Protocol**](#7-protocol) SHOULD be omitted
	* e.g. `<link href="//style.css" rel="stylesheet">`

&#9650; [Table of Contents](#table-of-contents)

<!-- ------------------------------ -->

### 1. Self-closing Elements

Self-closing elements MUST NOT be closed.

#### &#10006; Incorrect

<pre lang=html>
&lt;link href=&quot;theme.css&quot; rel=&quot;stylesheet&quot; /&gt;

&lt;br /&gt;
</pre>

&#8627; Incorrect because `<link>` and `<br>` have a `/` at the end.

#### &#10004; Correct

<pre lang=html>
&lt;link href=&quot;theme.css&quot; rel=&quot;stylesheet&quot;&gt;

&lt;br&gt;
</pre>

&#9650; [Elements and Attributes](#5-elements-and-attributes)

<!-- ------------------------------ -->

### 2. Optional Open/Close Tags

Optional open/close tags MUST be included.

#### &#10006; Incorrect

<pre lang=html>
&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;en&quot;&gt;
&lt;div id=&quot;main-wrapper&quot;&gt;
	&lt;h1&gt;Welcome&lt;/h1&gt;
	&lt;p&gt;This is a skeleton document.
&lt;/div&gt;
&lt;/html&gt;
</pre>

&#8627; Incorrect because `<head></head>`, `<body></body>` and `</p>` are missing.

#### &#10004; Correct

<pre lang=html>
&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;en&quot;&gt;
&lt;head&gt;
	&lt;title&gt;Welcome&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div id=&quot;main-wrapper&quot;&gt;
	&lt;h1&gt;Welcome&lt;/h1&gt;
	&lt;p&gt;This is a skeleton document.&lt;/p&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

&#9650; [Elements and Attributes](#5-elements-and-attributes)

<!-- ------------------------------ -->

### 3. Attribute Values

Attribute values MUST be wrapped in double quotation marks.

#### &#10006; Incorrect

<pre lang=html>
&lt;form action=processor.php class='application'&gt;
	...
&lt;/form&gt;
</pre>

&#8627; Incorrect because `processor.php` and `application` are not wrapped in double quotes.

#### &#10004; Correct

<pre lang=html>
&lt;form action=&quot;processor.php&quot; class=&quot;application&quot;&gt;
	...
&lt;/form&gt;
</pre>

&#9650; [Elements and Attributes](#5-elements-and-attributes)

<!-- ------------------------------ -->

### 4. Attribute Booleans

Attribute booleans SHOULD NOT include a value.

#### ~ Acceptable

<pre lang=html>
&lt;input type=&quot;text&quot; name=&quot;first_name&quot; autofocus=&quot;autofocus&quot;&gt;
</pre>

&#8627; Acceptable, but `autofocus` value is not required for `autofocus` attribute.

#### &#10004; Correct

<pre lang=html>
&lt;input type=&quot;text&quot; name=&quot;first_name&quot; autofocus&gt;
</pre>

&#9650; [Elements and Attributes](#5-elements-and-attributes)

<!-- ------------------------------ -->

### 5. Type and Language Attribute

Type and language attribute MUST be omitted on `script` tags.

#### &#10006; Incorrect

<pre lang=html>
&lt;script src=&quot;//script.js&quot; type=&quot;text/javascript&quot;&gt;&lt;/script&gt;
</pre>

&#8627; Incorrect because `type` attribute is included.

#### &#10004; Correct

<pre lang=html>
&lt;script src=&quot;//script.js&quot;&gt;&lt;/script&gt;
</pre>

&#9650; [Elements and Attributes](#5-elements-and-attributes)

<!-- ------------------------------ -->

### 6. Type Attribute

Type attribute MUST be omitted on `link` and `style` tags.

#### &#10006; Incorrect

<pre lang=html>
&lt;link rel=&quot;stylesheet&quot; href=&quot;//style.css&quot; type=&quot;text/css&quot;&gt;
</pre>

&#8627; Incorrect because `type` attribute is included.

#### &#10004; Correct

<pre lang=html>
&lt;link rel=&quot;stylesheet&quot; href=&quot;//style.css&quot;&gt;
</pre>

&#9650; [Elements and Attributes](#5-elements-and-attributes)

<!-- ------------------------------ -->

### 7. Protocol

Protocol SHOULD be omitted.

#### ~ Acceptable

<pre lang=html>
&lt;link rel=&quot;stylesheet&quot; href=&quot;http://domain.com/style.css&quot;&gt;
</pre>

&#8627; Acceptable, but `http://domain.com` could be replaced with `//`.

#### &#10004; Correct

<pre lang=html>
&lt;link rel=&quot;stylesheet&quot; href=&quot;//style.css&quot;&gt;
</pre>

&#9650; [Elements and Attributes](#5-elements-and-attributes)

<!-- ---------------------------------------------------------------------- -->

## 6. Best Practices

1. [**Structures, styles and scripts**](#1-structures-styles-and-scripts) MUST be separated from each other
	* e.g. `<a class="button" data-track="pageview">Read More</a>`
2. [**Valid HTML**](#2-valid-html) MUST be written
	* i.e. yes `<ul><li></li></ul>`, no `<ul><p></p></ul>`
3. [**Semantic HTML**](#3-semantic-html) MUST be written
	* i.e. yes `<a href="">View Options</a>`, no `<div class="click">View Options</div>`
4. [**Form field labels**](#4-form-field-labels) MUST be used
	* e.g. `<label for=""></label><input name="" type="text">`
5. [**Form field names**](#5-form-field-names) MUST use underscores to separate words
	* e.g. `<input type="text" name="first_name">`
6. [**Entity references**](#6-entity-references) MUST NOT be used
	* e.g. yes `—`, no `&mdash;`

&#9650; [Table of Contents](#table-of-contents)

<!-- ------------------------------ -->

### 1. Structures, Styles and Scripts

Structures, styles and scripts MUST be separated from each other.

#### &#10006; Incorrect

<pre lang=html>
&lt;div class=&quot;internships-module&quot;&gt;
	...
&lt;/div&gt;
</pre>

&#8627; Incorrect because structure, style and functionality are not decoupled.

#### &#10004; Correct

<pre lang=html>
&lt;div class=&quot;module internships&quot; data-track=&quot;pageview event&quot;&gt;
	...
&lt;/div&gt;
</pre>

&#9650; [Best Practices](#6-best-practices)

<!-- ------------------------------ -->

### 2. Valid HTML

Valid HTML MUST be written.

#### &#10006; Incorrect

<pre lang=html>
&lt;ul&gt;
	&lt;li&gt;Item one&lt;/li&gt;
	&lt;li&gt;Item two&lt;/li&gt;
	&lt;ul&gt;
		&lt;li&gt;Sub-item one&lt;/li&gt;
		&lt;li&gt;Sub-item two&lt;/li&gt;
	&lt;/ul&gt;
&lt;/ul&gt;
</pre>

&#8627; Incorrect because `<ul>` cannot be a child of a `<ul>`.

#### &#10004; Correct

<pre lang=html>
&lt;ul&gt;
	&lt;li&gt;Item one&lt;/li&gt;
	&lt;li&gt;Item two&lt;/li&gt;
	&lt;li&gt;
		&lt;ul&gt;
			&lt;li&gt;Sub-item one&lt;/li&gt;
			&lt;li&gt;Sub-item two&lt;/li&gt;
		&lt;/ul&gt;
	&lt;/li&gt;
&lt;/ul&gt;
</pre>

&#9650; [Best Practices](#6-best-practices)

<!-- ------------------------------ -->

### 3. Semantic HTML

Semantic HTML MUST be written.

#### &#10006; Incorrect

<pre lang=html>
&lt;div class=&quot;button&quot;&gt;Click Here&lt;/div&gt;
</pre>

&#8627; Incorrect because `<a>` is the elementing for clicking, not `<div>`.

<pre lang=html>
&lt;p&gt;&lt;strong&gt;Lorem ipsum:&lt;/strong&gt; Dolor sit amet, consectetur
adipiscing elit. Sed tincidunt urna id dui aliquet facilisis. Maecenas nulla diam,
scelerisque et nisl congue, ornare fermentum turpis. Pellentesque eu lorem nulla.
Sed interdum sagittis eros non vulputate. Donec sed interdum ante. Phasellus non
molestie nulla.&lt;/p&gt;
</pre>

&#8627; Incorrect because `Lorem ipsum` is to be bold, not strongly spoken by a screen reader.

<pre lang=html>
&lt;div class=&quot;textarea&quot;&gt;Write your text here.&lt;/div&gt;
</pre>

&#8627; Incorrect because `<div>` is not a natural element for user input.

#### &#10004; Correct

<pre lang=html>
&lt;a href=&quot;#&quot; class=&quot;button&quot;&gt;Click Here&lt;/a&gt;

&lt;p&gt;&lt;b&gt;Lorem ipsum:&lt;/b&gt; Dolor sit amet, consectetur adipiscing
elit. Sed tincidunt urna id dui aliquet facilisis. Maecenas nulla diam, scelerisque
et nisl congue, ornare fermentum turpis. Pellentesque eu lorem nulla. Sed interdum
sagittis eros non vulputate. Donec sed interdum ante. Phasellus non molestie
nulla.&lt;/p&gt;

&lt;textarea name=&quot;comment&quot;&gt;Write your text here.&lt;/textarea&gt; 
</pre>

&#9650; [Best Practices](#6-best-practices)

<!-- ------------------------------ -->

### 4. Form Field Labels

Form field labels MUST be used.

#### &#10006; Incorrect

<pre lang=html>
&lt;input type=&quot;radio&quot; name=&quot;gender&quot; id=&quot;male&quot; value=&quot;male&quot;&gt;
&lt;input type=&quot;radio&quot; name=&quot;gender&quot; id=&quot;female&quot; value=&quot;female&quot;&gt;
</pre>

&#8627; Incorrect because `<label>` is missing.

#### &#10004; Correct

<pre lang=html>
&lt;input type=&quot;radio&quot; name=&quot;gender&quot; id=&quot;male&quot; value=&quot;male&quot;&gt; &lt;label for=&quot;male&quot;&gt;Male&lt;/label&gt;
&lt;input type=&quot;radio&quot; name=&quot;gender&quot; id=&quot;female&quot; value=&quot;female&quot;&gt; &lt;label for=&quot;female&quot;&gt;Female&lt;/label&gt;
</pre>

&#9650; [Best Practices](#6-best-practices)

<!-- ------------------------------ -->

### 5. Form Field Names

Form field names MUST use underscores to separate words.

#### &#10006; Incorrect

<pre lang=html>
&lt;input type=&quot;text&quot; name=&quot;emailaddress&quot;&gt;
&lt;input type=&quot;text&quot; name=&quot;email-address&quot;&gt;
</pre>

&#8627; Incorrect because `emailaddress` and `email-address` are not using underscores between words.

#### &#10004; Correct

<pre lang=html>
&lt;input type=&quot;text&quot; name=&quot;email_address&quot;&gt;
</pre>

&#9650; [Best Practices](#6-best-practices)

<!-- ------------------------------ -->

### 6. Entity References

Entity references MUST NOT be used.

#### &#10006; Incorrect

<pre>
&euro;
</pre>

&#8627; Incorrect because `&euro;` entity reference is used.

#### &#10004; Correct

<pre>
€
</pre>

&#9650; [Best Practices](#6-best-practices)

---

&#9650; [Table of Contents](#table-of-contents)

Inspired in part by style guides from: [CKAN](http://docs.ckan.org/en/latest/html-coding-standards.html), [Google](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml), [jQuery](http://contribute.jquery.org/style-guide/html/), and [WordPress](http://make.wordpress.org/core/handbook/coding-standards/html/).
