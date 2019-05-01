# Magnolia-Freemarker Snippets

Visual Studio snippets for the [FreeMarker](https://freemarker.apache.org/) templating language. The snippets work in `.ftl` files.

![Demo](videos/freemarker_snippets_demo.gif)

[**Install the Extension →**](https://marketplace.visualstudio.com/items?itemName=fentech.freemarker-magnolia-snippets)

## Jump to...

**[Freemarker Snippets](#freemarker-snippets)**
**[HTML Snippets](#html-snippets)**
**[Magnolia Snippets](#magnolia-snippets)**

&nbsp;
_Note: All output examples below have dummy data, in curly bracket (i.e. `{variableName}`), that represent tab stops, to show you how it should display._

&nbsp;

# Freemarker Snippets

All ftl commands have a arrow wrapper option `<>` with a similar prefix.

### **include**

```
[#include "{/path/to/include}"]
```

### **macro:call**

```
[@{macroName} {argument=argumentValue} /]
```

### **macro:define**

```
[#macro {macroName} {arguments=withDefaultValue}]
  {code}
[/#macro]
```

### **if**

```
[#if {statement}]
  {code}
[/#if]
```

### **if:has**

```
[#if {statement}?has_content]
  {code}
[/#if]
```

### **if:else**

```
[#if {statement}]
  {code}
[#else]
  {code}
[/#if]
```

### **if:elseif**

```
[#if {statement}]
  {code}
[#elseif {statement2}]
  {code}
[/#if]
```

### **else**

```
[#else]
```

### **elseif**

```
[#elseif {statement}]
```

### **switch**

```
[#switch {variable}]
  [#case {value1}]
    {code}
    [#break]
[/#switch]
```

### **case**

```
[#case {value}]
```

### **break**

```
[#break]
```

### **tag**

```
[#{tagName}]
```

### **/**

```
[/#{tagName}]
```

### **int**

```
${$0}
```

### **assign**

```
[#assign {nameOfVariable = value}]
```

### **local**

```
[#local {nameOfVariable = value}]
```

&nbsp;

# HTML Snippets

Add a period "`.`" to the end of any html snippet to add a class property (e.g. "`section.`" outputs `<section class=""></section>`).

| Snippet          | Has Class | Output                                                              |
| ---------------- | --------- | ------------------------------------------------------------------- |
| **section**      | &#x2714;  | `<section></section>`                                               |
| **header**       | &#x2714;  | `<header></header>`                                                 |
| **main**         | &#x2714;  | `<main></main>`                                                     |
| **div**          | &#x2714;  | `<div></div>`                                                       |
| **form**         | &#x2714;  | `<form id="{id}" action="{action}" method="{method}"></form>`       |
| **input**        | &#x2714;  | `<input id="{name}" name="{name}" type="{type}" value="{value}" />` |
| **span**         | &#x2714;  | `<span></span>`                                                     |
| **h1**           | &#x2714;  | `<h1></h1>`                                                         |
| **h2**           | &#x2714;  | `<h2></h2>`                                                         |
| **h3**           | &#x2714;  | `<h3></h3>`                                                         |
| **h4**           | &#x2714;  | `<h4></h4>`                                                         |
| **p**            | &#x2714;  | `<p></p>`                                                           |
| **strong**       | &#x2714;  | `<strong></strong>`                                                 |
| **a**            | &#x2714;  | `<a href="{href}"></a>`                                             |
| **button**       | &#x2714;  | `<button></button>`                                                 |
| **img**          | &#x2714;  | `<img src="{src}" alt="{alt}" title="{title}">`                     |
| **meta**         |           | `<meta property="{property}" content="{content}">`                  |
| **link**         |           | `<link rel="{rel}" href="{href}">`                                  |
| **script**       |           | `<script type="{type}" src="{src}"></script>`                       |
| **script#**      |           | `<script id="{id}" type="{type}" src="{src}"></script>`             |
| **script:block** |           | `<script></script>`                                                 |
| **class**        |           | `class=""`                                                          |
| **href**         |           | `href=""`                                                           |
| **style**        |           | `style=""`                                                          |
| **role**         |           | `role=""`                                                           |
| **alt**          |           | `alt=""`                                                            |
| **title**        |           | `title=""`                                                          |
| **src**          |           | `src=""`                                                            |

&nbsp;

# Magnolia Snippets

### **cmsfn**

```
cmsfn.{option}()
```

- **options:**
  1. children
  2. contentByPath
  3. contentById
  4. contentListByTemplateId
  5. page
  6. link
  7. externalLink
  8. externalLinkTitle
  9. linkPrefix
  10. localizedLinks
  11. asContentMap
  12. asJCRNode
  13. asNodeList
  14. ancestors
  15. parent
  16. root
  17. siteRoot
  18. dump
  19. isEditMode
  20. isPreviewMode
  21. isAuthorInstance
  22. isPublicInstance
  23. decode
  24. abbreviateString
  25. queryStringAndFragment
  26. language
  27. wrapForI18n
  28. isCurrentLocale
  29. metaData
  30. fileExtension
  31. readableFileSize

### **dump**

Outputs Magnolia [`cmsfn.dump()`](https://documentation.magnolia-cms.com/display/DOCS60/cmsfn#cmsfn-Dump) templating function.

```ftl
${cmsfn.dump({object_to_dump}, 3 , true)}
```

### **components**

```
[#list components as component]
  [@cms.component content=component /]
[/#list]
```

### **area**

```
[@cms.area name="{areaName}" /]
```

&nbsp;

# Release Notes

### v1.4.0
Adds arrow wrapper `<>` option snippets for all ftl commands

### v1.3.0

Adds `form` and `input` tag snippets

### v1.2.0

Adds `button` tag snippets

### v1.1.5

Sets default `depth` and `asHtml` arguments of `cmsfn.dump()` snippet.

### v1.1.4

Adds snippets for the following HTML tags: span, a tag with class, image tag with class, meta, link, script (script, script with id, and script block). Updates the README to indicate which html tags have a 'with class' variant.

### v1.1.3

Updates README

### v1.1.2

Updates README with better documentation and adds demo.

### v1.1.1

Fixes switch statement last tab stop.

### v1.1.0

Adds the switch, case, break, and elseif snippets.
