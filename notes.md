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





# Example mongo Project -> college db

> DB Name : college
>> Collections

>> CSE

>> ADS

>> AML

>> ECE

>> EEE

---



#### CREATING DATABASE - `use college`
#### CREATING COLLECTIONS
```js
> use college
switched to db college
> db.createCollection("ADS")
{ "ok" : 1 }
> db.createCollection("CSE")
{ "ok" : 1 }
> db.createCollection("ECE")
{ "ok" : 1 }
> db.createCollection("EEE")
{ "ok" : 1 }
> db.createCollection("AML")
{ "ok" : 1 }
```
#### INSERTING DATA

```js

> db.ADS.insertMany([{name:"Rithik",age:20,marks:45},{name:"Mano",age:21,marks:40},{name:"Mohan",age:20,marks:42},{name:"Vishnu",age:21,marks:35},{name:"Ram",age:20,marks:34}])
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("6628c355e9dca134f5313381"),
                ObjectId("6628c355e9dca134f5313382"),
                ObjectId("6628c355e9dca134f5313383"),
                ObjectId("6628c355e9dca134f5313384"),
                ObjectId("6628c355e9dca134f5313385")
        ]
}
> db.CSE.insertMany([{name:"Rohini",age:20,marks:43},{name:"Manimala",age:20,marks:30},{name:"Mohanasundari",age:19,marks:48},{name:"Vishali",age:20,marks:34},{name:"Ramesh",age:20,marks:34}])
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("6628c3a2e9dca134f5313386"),
                ObjectId("6628c3a2e9dca134f5313387"),
                ObjectId("6628c3a2e9dca134f5313388"),
                ObjectId("6628c3a2e9dca134f5313389"),
                ObjectId("6628c3a2e9dca134f531338a")
        ]
}
> db.ECE.insertMany([{name:"Varun",age:20,marks:35},{name:"Manonmani",age:21,marks:40},{name:"Mala",age:21,marks:32},{name:"Nisha",age:20,marks:25},{name:"Lavanya",age:20,marks:43}])
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("6628c46ae9dca134f531338b"),
                ObjectId("6628c46ae9dca134f531338c"),
                ObjectId("6628c46ae9dca134f531338d"),
                ObjectId("6628c46ae9dca134f531338e"),
                ObjectId("6628c46ae9dca134f531338f")
        ]
}
> db.EEE.insertMany([{name:"Srikanth",age:20,marks:43},{name:"Gowtham",age:19,marks:44},{name:"Vikram",age:20,marks:40},{name:"Krishna",age:19,marks:45},{name:"Magesh",age:20,marks:48}])
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("6628c4e5e9dca134f5313390"),
                ObjectId("6628c4e5e9dca134f5313391"),
                ObjectId("6628c4e5e9dca134f5313392"),
                ObjectId("6628c4e5e9dca134f5313393"),
                ObjectId("6628c4e5e9dca134f5313394")
        ]
}
> db.AML.insertMany([{name:"Subha",age:20,marks:44},{name:"Lekha",age:20,marks:38},{name:"Sri",age:20,marks:39},{name:"Megha",age:20,marks:35},{name:"Malini",age:19,marks:37}])
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("6628c542e9dca134f5313395"),
                ObjectId("6628c542e9dca134f5313396"),
                ObjectId("6628c542e9dca134f5313397"),
                ObjectId("6628c542e9dca134f5313398"),
                ObjectId("6628c542e9dca134f5313399")
        ]
}
```

#### VIEWING DATA

```js

> db.ECE.find()
{ "_id" : ObjectId("6628c46ae9dca134f531338b"), "name" : "Varun", "age" : 20, "marks" : 35 }
{ "_id" : ObjectId("6628c46ae9dca134f531338c"), "name" : "Manonmani", "age" : 21, "marks" : 40 }
{ "_id" : ObjectId("6628c46ae9dca134f531338d"), "name" : "Mala", "age" : 21, "marks" : 32 }
{ "_id" : ObjectId("6628c46ae9dca134f531338e"), "name" : "Nisha", "age" : 20, "marks" : 25 }
{ "_id" : ObjectId("6628c46ae9dca134f531338f"), "name" : "Lavanya", "age" : 20, "marks" : 43 }
> db.EEE.find()
{ "_id" : ObjectId("6628c4e5e9dca134f5313390"), "name" : "Srikanth", "age" : 20, "marks" : 43 }
{ "_id" : ObjectId("6628c4e5e9dca134f5313391"), "name" : "Gowtham", "age" : 19, "marks" : 44 }
{ "_id" : ObjectId("6628c4e5e9dca134f5313392"), "name" : "Vikram", "age" : 20, "marks" : 40 }
{ "_id" : ObjectId("6628c4e5e9dca134f5313393"), "name" : "Krishna", "age" : 19, "marks" : 45 }
{ "_id" : ObjectId("6628c4e5e9dca134f5313394"), "name" : "Magesh", "age" : 20, "marks" : 48 }
> db.ADS.find()
{ "_id" : ObjectId("6628c355e9dca134f5313381"), "name" : "Rithik", "age" : 20, "marks" : 45 }
{ "_id" : ObjectId("6628c355e9dca134f5313382"), "name" : "Mano", "age" : 21, "marks" : 40 }
{ "_id" : ObjectId("6628c355e9dca134f5313383"), "name" : "Mohan", "age" : 20, "marks" : 42 }
{ "_id" : ObjectId("6628c355e9dca134f5313384"), "name" : "Vishnu", "age" : 21, "marks" : 35 }
{ "_id" : ObjectId("6628c355e9dca134f5313385"), "name" : "Ram", "age" : 20, "marks" : 34 }
> db.AML.find()
{ "_id" : ObjectId("6628c542e9dca134f5313395"), "name" : "Subha", "age" : 20, "marks" : 44 }
{ "_id" : ObjectId("6628c542e9dca134f5313396"), "name" : "Lekha", "age" : 20, "marks" : 38 }
{ "_id" : ObjectId("6628c542e9dca134f5313397"), "name" : "Sri", "age" : 20, "marks" : 39 }
{ "_id" : ObjectId("6628c542e9dca134f5313398"), "name" : "Megha", "age" : 20, "marks" : 35 }
{ "_id" : ObjectId("6628c542e9dca134f5313399"), "name" : "Malini", "age" : 19, "marks" : 37 }
> db.CSE.find()
{ "_id" : ObjectId("6628c3a2e9dca134f5313386"), "name" : "Rohini", "age" : 20, "marks" : 43 }
{ "_id" : ObjectId("6628c3a2e9dca134f5313387"), "name" : "Manimala", "age" : 20, "marks" : 30 }
{ "_id" : ObjectId("6628c3a2e9dca134f5313388"), "name" : "Mohanasundari", "age" : 19, "marks" : 48 }
{ "_id" : ObjectId("6628c3a2e9dca134f5313389"), "name" : "Vishali", "age" : 20, "marks" : 34 }
{ "_id" : ObjectId("6628c3a2e9dca134f531338a"), "name" : "Ramesh", "age" : 20, "marks" : 34 }

```

## Mongo Cheatsheet online

# MongoDB Cheat Sheet

## Show All Databases

```
show dbs
```

## Show Current Database

```
db
```

## Create Or Switch Database

```
use acme
```

## Drop

```
db.dropDatabase()
```

## Create Collection

```
db.createCollection('posts')
```

## Show Collections

```
show collections
```

## Insert Row

```
db.posts.insert({
  title: 'Post One',
  body: 'Body of post one',
  category: 'News',
  tags: ['news', 'events'],
  user: {
    name: 'John Doe',
    status: 'author'
  },
  date: Date()
})
```

## Insert Multiple Rows

```
db.posts.insertMany([
  {
    title: 'Post Two',
    body: 'Body of post two',
    category: 'Technology',
    date: Date()
  },
  {
    title: 'Post Three',
    body: 'Body of post three',
    category: 'News',
    date: Date()
  },
  {
    title: 'Post Four',
    body: 'Body of post three',
    category: 'Entertainment',
    date: Date()
  }
])
```

## Get All Rows

```
db.posts.find()
```

## Get All Rows Formatted

```
db.posts.find().pretty()
```

## Find Rows

```
db.posts.find({ category: 'News' })
```

## Sort Rows

```
# asc
db.posts.find().sort({ title: 1 }).pretty()
# desc
db.posts.find().sort({ title: -1 }).pretty()
```

## Count Rows

```
db.posts.find().count()
db.posts.find({ category: 'news' }).count()
```

## Limit Rows

```
db.posts.find().limit(2).pretty()
```

## Chaining

```
db.posts.find().limit(2).sort({ title: 1 }).pretty()
```

## Foreach

```
db.posts.find().forEach(function(doc) {
  print("Blog Post: " + doc.title)
})
```

## Find One Row

```
db.posts.findOne({ category: 'News' })
```

## Find Specific Fields

```
db.posts.find({ title: 'Post One' }, {
  title: 1,
  author: 1
})
```

## Update Row

```
db.posts.update({ title: 'Post Two' },
{
  title: 'Post Two',
  body: 'New body for post 2',
  date: Date()
},
{
  upsert: true
})
```

## Update Specific Field

```
db.posts.update({ title: 'Post Two' },
{
  $set: {
    body: 'Body for post 2',
    category: 'Technology'
  }
})
```

## Increment Field (\$inc)

```
db.posts.update({ title: 'Post Two' },
{
  $inc: {
    likes: 5
  }
})
```

## Rename Field

```
db.posts.update({ title: 'Post Two' },
{
  $rename: {
    likes: 'views'
  }
})
```

## Delete Row

```
db.posts.remove({ title: 'Post Four' })
```

## Sub-Documents

```
db.posts.update({ title: 'Post One' },
{
  $set: {
    comments: [
      {
        body: 'Comment One',
        user: 'Mary Williams',
        date: Date()
      },
      {
        body: 'Comment Two',
        user: 'Harry White',
        date: Date()
      }
    ]
  }
})
```

## Find By Element in Array (\$elemMatch)

```
db.posts.find({
  comments: {
     $elemMatch: {
       user: 'Mary Williams'
       }
    }
  }
)
```

## Add Index

```
db.posts.createIndex({ title: 'text' })
```

## Text Search

```
db.posts.find({
  $text: {
    $search: "\"Post O\""
    }
})
```

## Greater & Less Than

```
db.posts.find({ views: { $gt: 2 } })
db.posts.find({ views: { $gte: 7 } })
db.posts.find({ views: { $lt: 7 } })
db.posts.find({ views: { $lte: 7 } })
```


# Node JS

