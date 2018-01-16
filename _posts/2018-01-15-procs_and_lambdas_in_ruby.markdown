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

The most special thing about Procs and Lambdas, and something that fans of JavaScript will appreciate, is that they create closures. For example, 
```def number_incrementer
   num = 0
   Proc.new {num + 5}
end

first_incrementer = number_counter
second_incrementer = number_counter

first_incrementer.call #returns 5
first_incrementer.call #returns 10

second_incrementer.call #returns 5```

