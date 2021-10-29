---
title: js blog 1
date: "2021-10-29T23:46:37.121Z"
---

 what is useState ?

> useState():- It is Hook that allows you to read React to function component. We call it inside a function component to add some local state to it.
use State returns a pair: - the current state value and a function that lets you update it.
React will preserve this state between re-renders.
You can call this function from an Event handler or somewhere else.
>E.g.: - import React, {useState} from ‘react’.;
const nameStateVariable = useState(“Rahul”)
const[name, setname] = useState(“Rahul”)

what is useeffect ? 
> useEffect is a hook Encapsulating code that has ‘side Effects’, if you are familiar with React cycle 
Lifecycle methods, you can think of useEffect Hook as component DidMount, component Didupdate and component will Unmount combined.
Eg:-
>Import React, {useState, useEffect} from ‘react’,
useEffect(Function)
useEffect(Function,Array)
The function passed to useEffect unit run after the render is committed to the screen. 
Second argument to useEffect that is the array of values that the Effect depends on.


What does  useEffect do?    
>By using this Hook, you tell React that your component needs to do something after render. React will remember the function. You passed and call it. Later after performing the DOM updates. In this effect, we set the document title, we could also perform data fetching or call some other imperative API.


Why is useEffect called inside a component?
> Babel is a tool chain that is mainly used to convert ECMA 2015 + Code into a backward compatible version of JS in current and older browser or Environments.

Custom Hooks
> A Custom Hook is a J.S. function, when use want to share logic between this J.S. functions, we extract it a third function function.
Building your own Hook Lets you extract component logic into reusable functions.
You can write custom Hooks that cover a wide range of use cases like form handling, animation, declarative subscriptions, timers and many more.

Creating Custom Hook
> A custom Hook is a J.S. function whose name starts with “use” and that may call other Hooks.
Eg:- function useSomething(){
Return;
};

