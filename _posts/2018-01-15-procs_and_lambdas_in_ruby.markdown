---
layout: post
title:      "Procs and Lambdas in Ruby"
date:       2018-01-15 19:47:32 -0500
permalink:  procs_and_lambdas_in_ruby
---

Everything in Ruby is an object, right? Well not quite! Blocks in Ruby are not objects! However, there is a way around this catastrophe. Procs and Lambdas! At some point if you've been studying Ruby, you've probably heard of these terms. Procs and Lambdas are objects and allow us to save blocks to them. Lambdas are a special type of Proc and they are very similar to one another with a few key differences we will cover. We can define a lambda a few different ways:

1.```saved_block = -> {puts "Hello World"}```
2.```saved_block = lambda {puts "Hello World"}```

Typically Procs are defined as ```saved_block = Proc.new {puts "Hello World"}```

Both are most often called simply by ```saved_block.call```

The most special thing about Procs and Lambdas, and something that fans of JavaScript will appreciate, is that they create closures. For example:

```
def number_incrementer`
   num = 0
   Proc.new {num + 5}
end

first_incrementer = number_counter
second_incrementer = number_counter

first_incrementer.call #returns 5
first_incrementer.call #returns 10

second_incrementer.call #returns 5

```

There are a few key differences between Procs and Lambdas in Ruby. The first is Procs does not care about arguments, but Lambdas do. Similar to regular Ruby methods, if you define a Lambda with 2 arguments but call it with 0, you will get an error. Procs, however, would not raise an error. 

The most important difference between Procs and Lambdas is how they return. Lambdas will return like normal Ruby blocks where it will return out of the block and continue on in the method it is called in. Procs, however, will return out of the entire method. This is an incredibly important distinction.

```
def returns_from_block
new_lambda = lambda {return 29}
new_lambda.call
puts "Hello World"

#Will have "Hello World" printed out

def returns_from_method
new_proc = Proc.new {return 29}
new_proc.call
puts "Hello World"

#Will not have "Hello World" printed
```

The big question is do you need Procs and Lambdas? The short answer is in all likelihood no. However, other developers may feel differently and it is good to recognized and understand what they do. They are definitely syntantic sugar, but they do have more elements to them than just syntax beaty. If you do come across a spot where a Proc or Lambda is necessary, I would recommend sticking with Lambdas as they are much closer to a typically Ruby block and can avoid odd errors moreso than a Proc.
