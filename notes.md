# NOTES

## Frontend + integration + Backend + Database = FullStack

> Frontend (UI) (Client)
---
> Backend (Logics) (Server)
---
> Database (Storage)

>> Relational (Rows & Columns)
>> Non-Relational (Files)

# HTML

Tags are used in HTML

`<a>`
`<abbr>`
`<address>`
`<area>`
`<article>`
`<aside>`
`<audio>`
`<b>`
`<base>`
`<bdi>`
`<bdo>`
`<blockquote>`
`<body>`
`<br>`
`<button>`
`<canvas>`
`<caption>`
`<cite>`
`<code>`
`<col>`
`<colgroup>`
`<data>`
`<datalist>`
`<dd>`
`<del>`
`<details>`
`<dfn>`
`<dialog>`
`<div>`
`<dl>`
`<dt>`
`<em>`
`<embed>`
`<fieldset>`
`<figcaption>`
`<figure>`
`<footer>`
`<form>`
`<h1>`
`<h2>`
`<h3>`
`<h4>`
`<h5>`
`<h6>`
`<head>`
`<header>`
`<hr>`
`<html>`
`<i>`
`<iframe>`
`<img>`
`<input>`
`<ins>`
`<kbd>`
`<label>`
`<legend>`
`<li>`
`<link>`
`<main>`
`<map>`
`<mark>`
`<meta>`
`<meter>`
`<nav>`
`<noscript>`
`<object>`
`<ol>`
`<optgroup>`
`<option>`
`<output>`
`<p>`
`<param>`
`<picture>`
`<pre>`
`<progress>`
`<q>`
`<rp>`
`<rt>`
`<ruby>`
`<s>`
`<samp>`
`<script>`
`<section>`
`<select>`
`<slot>`
`<small>`
`<source>`
`<span>`
`<strong>`
`<style>`
`<sub>`
`<summary>`
`<sup>`
`<svg>`
`<table>`
`<tbody>`
`<td>`
`<template>`
`<textarea>`
`<tfoot>`
`<th>`
`<thead>`
`<time>`
`<title>`
`<tr>`
`<track>`
`<u>`
`<ul>`
`<var>`
`<video>`
`<wbr>`

# JavaScript 

> JavaScript Engines
---
>> Chrome - V8

>> Edge - Chakra 

>> Firefox - SpyderMonkey

---

Dynamically typed = No need of defining Datatype

# MongoDB

show dbs - show databases

db - show which db is selected

show collections - show groups inside the db

db.insertOne({Name:"Rithik"}) - Insert json into the collection

^ this returns a response which has true or false to show it is stored or not

```
{
        "acknowledged" : true,
        "insertedId" : ObjectId("6628927d5215f76af6758b09")
}
```

id is unique for each obj

```
> db.kiot.insertOne({Name:"Rithik", Age: 20, Sex: "Male", City: "Salem"})
{
        "acknowledged" : true,
        "insertedId" : ObjectId("6628948b5215f76af6758b0a")
}
```

Insert Multiple Datas

```
> db.kiot.insertMany([{Name: "Mani", Age:19},{Name:"Reshmi", Age:20}])
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("66289dff68db71630d4a5a5d"),
                ObjectId("66289dff68db71630d4a5a5e")
        ]
}
```

Update Data


```
> db.kiot.update({"_id":ObjectId("66289dff68db71630d4a5a5e")},{Name:"Reshma"})
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })
> db.kiot.find()
{ "_id" : ObjectId("6628927d5215f76af6758b09"), "Name" : "Rithik" }
{ "_id" : ObjectId("6628948b5215f76af6758b0a"), "Name" : "Rithik", "Age" : 20, "Sex" : "Male", "City" : "Salem" }
{ "_id" : ObjectId("66289dff68db71630d4a5a5d"), "Name" : "Mani", "Age" : 19 }
{ "_id" : ObjectId("66289dff68db71630d4a5a5e"), "Name" : "Reshma" }

```

