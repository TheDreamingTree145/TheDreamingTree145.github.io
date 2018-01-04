---
layout: post
title:      "Basics of Stacks and Queues "
date:       2018-01-04 00:19:56 +0000
permalink:  basics_of_stacks_and_queues
---

Linkined lists, stacks and queues can seem like intimidating concepts at first, and they can be complex. However, the basics are easy to understand. Like arrays linked lists, stacks and queues are data structures. They differ from arrays  in that arrays are random access data structures, meaning we can access any element at any time. Linked lists are sequential data structures where each element has to be accessed in order. Stacks and queues are a type of sequential data structure but they both have limited access.

## Linked Lists
Linked lists are really a collection of data structures laid out in a specific order. Linked lists are most often a series of data structures where each data structure is called a node. The node will have the data as well as having a pointer to the next node. There are many operations that are able to be done with linked lists including creating a node, deleting a node, and traversing through the nodes. There a few types of linked lists including single linked lists where each nodes pointer points to the next node, double linked lists where each nodes pointer points to the previous node and next node, and circular linked lists where the last node points back to the first node.

## Stacks
The easiest way to think of stacks is think of LIFO, or the last in first out principle, where the last item added will be the first item sent out. We can also think of a stack like a deck of cards, we can't really take or add a card off the bottom of the stack, but we can add or remove a card from the top. This is why stacks follow LIFO. Stacks typically have two basic operations, push and pop. Similar to many programming languages, push is when we add an element to the top of the stack, while pop is used for removing an element from the top of the array. The important things to remember with stacks is that any time we can only access the top element of the stack and stacks follow LIFO, last in first out, principles.

## Queues 
Unlike stacks, queues follow a FIFO method, which is first in first out which means that the oldest element in the structure will be removed first and if element is inserted into the structure, it will go to the back of the line. A good way to think of queues would be amusement park lines. The person in front of the line has been in the line the longest and will be the first to exit the line, while the person in the back of line was the most recent person added to the line. Not coincidentally, amusement park lines are also called queues. Like stacks, there are two basic operations for queues, enqueue which is to add item to back/end of the structure, and dequeue which is take the oldest/first item out of the structure. Important to remember with queues is that thy follow a FIFO method.

