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
  

  

