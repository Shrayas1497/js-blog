---
title: js blog 2
date: "2021-10-29T22:12:03.284Z"
description: "important js concepts"
---

NPM(Node Package Manager):->
> It is used to take advantage of a vast ecosystem of third-party packages and easily install or update them.


WEB PACK:->
> Web pack is a static module bundler for modern J.S. applications. When webpack processes your application, it internally builds a dependency graph which maps every module your project needs and generate it (one or more bundles). It does not read the files inside the public folder. It processes src only and copies from the public folder for building.


 BABEL:-> 
> Babel is a tool chain that is mainly used to convert ECMA 2015 + Code into a backward compatible version of JS in current and older browser or Environments.

COMPONENTS:->
> Components are the building block of any React app.
Components lets use spilt in the UI into independent, reusable piece and think about each in isolation.
Components are like J.S. They accept arbitrary inputs (caused “props”) and return React Elements describing what should appear on the screen.


Difference between functional vs Class Component
> Functional Component :->
Use functional Component if you are writing a presentational component which does’nt have its own state or needs to access Lifestyle hook. You cannot use UseState() in your component because Functional component are plain J.S. functions.

Class Components:->
Use Class Components if you need state or need access Lifecycle hooks are coming from React. Component which you extend from in Class Component.


PROPS:->
> When React sees an Element representing a user defined Component, it passes Jsx attributes to this Component as a single object. We call this object “props”.
Whether you declare as a fuction or a class, it must never modify its own props.
All react Components must act like pure function with respect to their props.

STATE:->
>State is similar to props but it is private and fully controlled by the Component. We can create state only in class Component. It is possible to update the state/Modify the state.
There are two ways to initialize state in React Component:-
Direct inside class
Inside the constructor




   Class Student extends Component{
State{
Name:”Rahul”
Prop 1: this props.prop1
}
render() }
}
    ========

    Note:- The state property is reffered as state.
              This is a class iinstance property.

    --------


HOOKS
>Hooks are function that let you”hook into” React state and lifecycle features from function Components.Hooks allow you to use React without classes. It means you can use state and other React feature without writing a class.
React provide a few built in Hooks like useState, useEffect etc.
Hooks are new addition in React 16.8.

WHEN USE HOOKS ?

> If you write a function component and realize you need to add some state to it.
>
Rules of Hooks
>
> Only call Hooks at the top level – we should not call Hooks inside loops, Conditions or nested functions. Instead , always use Hooks at the top level of your React function.
Only call Hooks from React function- We should not call Hooks from regular Javascript functions. Instead, call Hooks from React function component or call Hooks from custom Hooks.
React realizes on the order in which Hooks are called.
Hooks don’t work inside classes.
>

 