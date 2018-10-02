# Magnolia-Freemarker Snippets
These are snippets for Freemarker (`.ftl`) files. 

### Freemarker Snippets
Snippet     | Output                  
------------|-----------------
include     | `[#include ""]` 
macro:call  | `[@{macroName} {arguments} /]`
macro:define| `[#macro {macroName} {arguments}]\n\t\n[/#macro]`
if          | `[#if $statement]\n\t$0\n[/#if]`
if:has      | `[#if ${1:statement}?has_content]\n\t$0\n[/#if]`
if:else     | `[#if ${1:statement}]\n\t$2\n[#else]\n\t$3\n[/#if]`
if:elseif   | `[#if ${1:statement}]\n\t$2\n[#elseif ${3:statement}]\n\t$4\n[/#if]`
else        | `[#else]`
elseif      | `[#elseif $0]`
switch      | `[#switch ${1:variable}]\n\t[#case ${2:value1}]\n\t\t$0\n\t\t[#break]\n[/#switch]`
case        | `[#case $value]`
break       | `[#break]`
tag         | `[#$0]`
/           | `[/#$0]`
int         | `${$0}`
assign      | `[#assign $nameOfVariable = $value]`
local       | `[#local $nameOfVariable = $value]`


### HTML Snippets
Add a period "`.`" to the end of any html snippet to add a class property (e.g. "`section.`" outputs   `<section class=""></section>`).

Snippet     | Output                
------------|----------------
section     | `<section></section>`            
header      | `<header></header>`         
main        | `<main></main>`            
div         | `<div></div>`            
h1          | `<h1></h1>`
h2          | `<h2></h2>`
h3          | `<h3></h3>`
h4          | `<h4></h4>`
p           | `<p></p>`
a           | `<a href="" target="" rel=""></a>`
img         | `<img src="" alt="" title="" class="">`
strong      | `<strong></strong>`
class       | `class=""`
href        | `href=""`
style       | `style=""`
role        | `role=""`
alt         | `alt=""`
title       | `title=""`
src         | `src=""`


### Magnolia Snippets
Snippet     | Output          | Options        
------------|-----------------|------------------
cmsfn       | `cmsfn.{option}()`| children, contentByPath, contentById, contentListByTemplateId, page, link, externalLink, externalLinkTitle, linkPrefix, localizedLinks, asContentMap, asJCRNode, asNodeList, ancestors, parent, root, siteRoot, dump, isEditMode, isPreviewMode, isAuthorInstance, isPublicInstance, decode, abbreviateString, queryStringAndFragment, language, wrapForI18n, isCurrentLocale, metaData, fileExtension, readableFileSize            
dump        | `${cmsfn.dump()}`
components  | `[#list components as component]\n\t[@cms.component content=component /]\n[/#list]`
area        | `[@cms.area name=\"$areaName\" /]`


# Release Information

### v1.0.3
Adds the switch, case and break snippets.

### v1.0.2
Adds the elseif snippet to out put a single elseif tag (`[#elseif {condition}]`).
