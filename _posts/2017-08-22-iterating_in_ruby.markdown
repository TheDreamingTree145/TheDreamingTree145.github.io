---
layout: post
title:  "Iterating in Ruby"
date:   2017-08-22 16:07:45 +0000
---


Iterating over collections of objects is a major aspect of learning a programming language and Ruby is no different. There are many different iterators in Ruby and choosing the right tool for the job is essential. Knowing what the iterator will return to  you at the end of the iteration is the key to getting it right. Continue on to get a base of some options for your code.

## Each
Each is one of the most basic low-level iterators in ruby. It will run through a collection of items and yields to a block. The important thing to remember about the Each method is that it will always return the original collection at the end.

```
arr = [1,2,3,4]

arr.each do |int|
  puts int
end

1
2
3
4
[1,2,3,4]
```
As shown, each yielded to the block, but the end return value was still the original array.

## Collect/Map

Collect and map methods can be used interchangably. These methods are similar to the each method, however, their return values are different. Collect will iterate through a collection, yield to a block, and return a NEW array. Collect nor map will alter the orignal array.

```
arr = [10, 8, 6, 4]

arr.collect do |int|
  int - 2
end

return value is [8, 6, 4, 2]

arr is still equal to [10, 8, 6, 4]
```

## Select 
Select is very helpful at pulling specific items from the collection it is passed. Select will find all elements in a collection for which the block passed to select is true. Select will the return a new array with the elements that evaluated to true. Again, select will not modify the existing array.

```
arr = [10, 8, 10, 4]

arr.select do |int|
  int < 9
end 

return value is [8, 4]

arr is still equal to [10, 8, 10, 4]
```

## Find/Detect
Find and select are very similar in that it looks for elements in a collection that evaluate to true based on a block. The difference between find and select is that find will only find the first value that will return true, unlike select, which returns all values that evaluate to true. Find and detect can be used interchangably.

```
arr = [10, 8, 10, 4]

arr.find do |int|
  int < 9
end 

return value is 8

arr = [10, 8, 10, 4]
```

These are some of the basic building blocks when learning ruby while they seem simple, and for the most part are, it is important to have a good understand what each iterator will do for you so you can have the right tool for the job. In a future blog post, I will go more in depth on some more advanced iterators. Happy Coding!
