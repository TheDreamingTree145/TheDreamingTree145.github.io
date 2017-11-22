---
layout: post
title:      "Differences Between State and Props in React"
date:       2017-11-22 23:04:10 +0000
permalink:  differences_between_state_and_props_in_react
---

Although the title calls for differences between state in React, there are some similarities as well. State and props are both plain javascript objects, when changed cause a re-render, and should have the same output given the same combination. Because of these similarities, it easy to mistunderstand when and why to use state or props.

### State

Local state for a component is initialized when a component mounts. It is mutable. It responds to changes, typically coming from user events, and re-renders based on those changes. State can only be modified within its own scope. That is a child component nor a parent component can change the state of a component. It can only be modified internally, though state can be set from a component to a child component. State captures the current attributes at a specific point of time.

### Props

Props on the other hand are immutable by a component. They are passed down from a parent component to child and the parent component can change the props, but again, the child component cannot mutate the passed down props. Props are really just the way components communicate with each other. They are really a vertical tree, where a parent at the top passes down props to the next branch and that branch can pass on props to a child branch and so forth.

### Conclusion

Though seemingly difficult to grasp at first, the similarities between state and props is fairly simple. State is mutable and internally controlled. Props, on the other hand, are passed down from a parent component to a child component and allow the components to communicate with each other. Props are immutable by the component the props are passed to. Through both are extremely powerful, stateless components are usually prefered, as state increases complexity.
