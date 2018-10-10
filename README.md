# Magnolia-Freemarker Snippets
These are snippets specific to Freemarker (`.ftl`) files. 

![Demo](videos/freemarker_snippets_demo.gif)

## Jump to... 
__[Freemarker Snippets](#freemarker-snippets)__  
__[HTML Snippets](#html-snippets)__  
__[Magnolia Snippets](#magnolia-snippets)__

&nbsp;
_Note: All output examples below have dummy data, in curly bracket (i.e. `{variableName}`), that represent tab stops, to show you how it should display._

&nbsp;
# Freemarker Snippets
### __include__
```
[#include "{/path/to/include}"] 
```
### __macro:call__
```
[@{macroName} {argument=argumentValue} /]
```
### __macro:define__
```
[#macro {macroName} {arguments=withDefaultValue}] 
  {code}
[/#macro]
```
### __if__
```
[#if {statement}] 
  {code}
[/#if]
```
### __if:has__
```
[#if {statement}?has_content]
  {code}
[/#if]
```
### __if:else__
```
[#if {statement}]
  {code}
[#else]
  {code}
[/#if]
```
### __if:elseif__
```
[#if {statement}]
  {code}
[#elseif {statement2}]
  {code}
[/#if]
```
### __else__
```
[#else]
```
### __elseif__
```
[#elseif {statement}]
```
### __switch__
```
[#switch {variable}]
  [#case {value1}]
    {code}
    [#break]
[/#switch]
```
### __case__
```
[#case {value}]
```
### __break__
```
[#break]
```
### __tag__
```
[#{tagName}]
```
### __/__
```
[/#{tagName}]
```
### __int__
```       
${$0}
```
### __assign__
```
[#assign {nameOfVariable = value}]
```
### __local__
```
[#local {nameOfVariable = value}]
```

&nbsp;
# HTML Snippets
Add a period "`.`" to the end of any html snippet to add a class property (e.g. "`section.`" outputs   `<section class=""></section>`).

Snippet           | Has Class  | Output                
------------------|------------|----------------
__section__       | 	&#x2714; | `<section></section>`            
__header__        | 	&#x2714; | `<header></header>`         
__main__          | 	&#x2714; | `<main></main>`            
__div__           | 	&#x2714; | `<div></div>`            
__span__          | 	&#x2714; | `<span></span>`            
__h1__            | 	&#x2714; | `<h1></h1>`
__h2__            | 	&#x2714; | `<h2></h2>`
__h3__            | 	&#x2714; | `<h3></h3>`
__h4__            | 	&#x2714; | `<h4></h4>`
__p__             | 	&#x2714; | `<p></p>`
__strong__        | 	&#x2714; | `<strong></strong>`
__a__             | 	&#x2714; | `<a href="{href}"></a>`
__img__           | 	&#x2714; | `<img src="{src}" alt="{alt}" title="{title}">`
__meta__          || `<meta property="{property}" content="{content}">`
__link__          || `<link rel="{rel}" href="{href}">`
__script__        || `<script type="{type}" src="{src}"></script>`
__script#__       || `<script id="{id}" type="{type}" src="{src}"></script>`
__script:block__  || `<script></script>`
__class__         || `class=""`
__href__          || `href=""`
__style__         || `style=""`
__role__          || `role=""`
__alt__           || `alt=""`
__title__         || `title=""`
__src__           || `src=""`

&nbsp;
# Magnolia Snippets
### __cmsfn__ 
```
cmsfn.{option}()
```
* __options:__
  1. children
  2. contentByPath
  2. contentById
  2. contentListByTemplateId
  2. page
  2. link
  2. externalLink
  2. externalLinkTitle
  2. linkPrefix
  2. localizedLinks
  2. asContentMap
  2. asJCRNode
  2. asNodeList
  2. ancestors
  2. parent
  2. root
  2. siteRoot
  2. dump
  2. isEditMode
  2. isPreviewMode
  2. isAuthorInstance
  2. isPublicInstance
  2. decode
  2. abbreviateString
  2. queryStringAndFragment
  2. language
  2. wrapForI18n
  2. isCurrentLocale
  2. metaData
  2. fileExtension
  2. readableFileSize 


### __dump__
```
${cmsfn.dump()}
```
### __components__ 
```
[#list components as component]
  [@cms.component content=component /]
[/#list]
```
### __area__ 
```
[@cms.area name="{areaName}" /]
```
&nbsp;

# Release Notes  

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
