# ReactJS-Tutorial

## Folder Structure
- node_modules
- public
  - index.html (the file which is rendered)
- src
  - index.js
  - App.js
  - index.css
  - App.css
- package.json
- package-lock.json
- .gitignore
- README.md

## React Components
- In React everything is a component.
- Component-Based Architecture.
- Component is nothing but a part of the web page like navbar, header, footer, side navbar etc.
- Component is a function.

      function HelloWorldComponent(){
        return (<h1>Hello World</h1>)
      }
  
  1. Should return JSX.
  2. Component name must start with uppercase letter.
 
## JSX
- JSX stands for JavaScript XML.
- Using JSX we can embed expressions.
- Dynamic attributes

## Props
- Props are like parameters to a function.
- It is used to make components generic so that it can be reused.

      function GreetComponent(props){
        return (<h1>Good Morning, {props.name}</h1>)
      }
      <GreetComponent name="Lolita"/>

## Life Cycle of a Component
1. Construction
2. Mount
3. Update
4. Un-mount

## Hooks
- All the hooks start with 'use'.

1. useState Hook:
- A state of a component is a variable that holds some information that may change over the lifetime of the component.
- Whenever the value of the state changes, the component re-renders itself with updated value.
- useState hook returns an array of size 2. 0th index contains the value of the variable (state) and 1st index contains the function used to update the value of the variable.
- A state is local to its component.

      import React, { useState } from "react";
  
      const CounterComponent = ()=>{
        const [count, setCount]=useState(0);
        return(
          <>
          <p>Count is {count}</p>
          <button onClick={()=>setCount(count+1)}>Increment</button>
          </>
        )
      }

2. useEffect Hook:
- Run code during the change in lifecycle of a component.
- The useEffect hook takes two arguments : callback function, dependency array.
  
1. The following snippet runs only when the component is mounted for the first time.
   
        useEffect(()=>{
          console.log("Counter component is mounted");
        },[])

2. The following snippet runs when the component is updated or the state changes.

        const [time, setTime]=useState(0);
  
        useEffect(()=>{
            const timer = setInterval(()=>setTime(time+1),1000);
            return function(){
                clearInterval(timer);
            }
        },[time]);
   The state is passed in the dependency array.

3. The function that is returned by the useEffect hook runs only when the component is unmounted.

       useEffect(()=>{
          console.log("Counter component is mounted");
          return (console.log("Counter component is unmounted")
        },[])
  

  

