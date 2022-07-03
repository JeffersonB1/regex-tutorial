# Matching an URL 

This is a tutorial on how to use regular expression to match an URL. The following is an expression to match a URL: 
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```
## Summary

By reading this tutorial you will be able to understand each part of the expression above and the use of it.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
We are going to have types of anchors that will be looking either for the beginning or the of a string. That way we can choose these as parameters of when the string we are looking will start or end.
 
Beginning anchor: 
^

Closing anchor:
$

### Quantifiers
The question mark is indication that a certain string is optional, which means it could have the string or not, example in our expression:

```
(https?:\/\/)?
```
In the expression above we can have ```https:``` or ``` http:```. At the same time we can ignore the whole expression about by adding the ```?``` at the end of the grouping.

We also have the *, this one is a combination of + and ?, which means it can match between 0 and 1 of the previous string or match one or more in a row of the previous string. You can see the use on the expression below.

```
([\/\w \.-]*)*
```

### Character Classes

The ````\d``` match a character that is type integer. We can see the use of it in the following expression:
```
([\da-z\.-]+)
```
In the expression above /d looks for a digit or a-z loos for any string betwing the range  of letter a and z.

The ```\w``` matches a word character and we can see it in the following expression: 

```
([\/\w \.-]*)
```
In the expression above we search for a word after the simbol ```/```.


### Flags

Regex usually are in between ```/``` so at the end of these we can specify flags for example: g(global), m(multi-line) and i (insensitive).  

### Grouping and Capturing
Our expression has 4 groups and each of those denotated by ().

First Group ```/^(https?:\/\/)?```, here we optionally use the http.

Second Group ```([\da-z\.-]+)```, here we look for any character.

Third Group ```([a-z\.]{2,6})```, match any character that comes before the period for example .com, .net etc...

Fourth Group ```([\/\w \.-]*) ``` this group represents the directory.

### Bracket Expressions

We use ```[]``` as bracket expression, and it is use like a ```|``` which means that whatever the value we have in between are the possible options that we are going to be looking for. For example:

```[\da-z\.-]``` Here we can match a digit or a letter from a-z or .


## Author

This tutorial was created by Jefferson Bencosme, if you want to find out more visit https://github.com/JeffersonB1