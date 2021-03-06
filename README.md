# React_Js_Learning

**REACT JS**

_1.	Intro_

  •	React is a JavaScript library for building user interfaces.
  
  •	React is used to build single-page applications.
  
  •	React allows us to create reusable UI components.
  
  •	React is JS library created by Facebook.
  
  •	Latest Version is 16.8.6 on 27 March 2019. 
  
_2.	Working_

  •	Instead of manipulating the browser’s DOM directly, “React creates a virtual DOM in memory” ,where it does all the necessary manipulation, before making the changes in the browser DOM.

_3.	Setting up Development Environment_

  To run any React application, we must have NodeJS installed on our PC. So, the very first step will be to install NodeJS. 
 
  •	Step 1: Install NodeJS. You may visit the official download link of NodeJS to download and install the latest version of NodeJS. Once we have set up NodeJS on our PC, the next thing we need to do is set up React Boilerplate.
 
  •	After installing we will create a react application Using below command.
  
**CMD :-  npm i/install create-react-app FileName**  

  •	To run the react app we will use following command.

**CMD :- npm start**

_4.	File Structure_

  Main_folder
  
    1.	Node_Modules_folder :In which many modules Folder and File are there.
    
    2.	Public_Folder :
        	Favicon.ico_File
        	Index.html_File
        	Logo192.png_File
        	Logo512.png_File
        	Manifest.json_File
        	Robots.txt_File
        
    3.	Src_Folder
        	App.css_File
        	App.js_File
        	App.test.js_File
        	Index.css_File
        	Index.js_File
        	Logo.svg_File
        	reportWebVitals.js_File
        	setupTests.js_File
        
    4.	.gitignore_File
    
    5.	Package-lock.json_File
    
    6.	Package.json_File
    
    7.	README.md_File

_5.	ES6 or ECMAScript6_
  
  React use ES6 , So we are going to learn new feature…
  
  1.	Classes
  
    A class is a type of function, but instead of using the keyword function to initiate it, we use the keyword class, and the properties are assigned inside     a constructor() method.
        Ex:- 
            class Road {
              constructor(name) {
                this.brand = name;
              }
            }
            const myroad = new Road("Zig-Zag");
            document.write(myroad.brand);

  2.	Arrow function
  
    Arrow functions allow us to write shorter function syntax:
        Ex:-
          hello = () => {
            return "Hello World!";
          }

  3.	Variables
  
    There are three ways of defining the variables: var, let, and const.
    
        o	Var
        
          If you use var outside of a function, it belongs to the global scope.
          If you use var inside of a function, it belongs to that function.
          If you use var inside of a block, i.e. a for loop, the variable is still available outside of that block.
          
        o	Let
        
          If you use let inside of a block, i.e. a for loop, the variable is only available inside of that loop.
          
        o	Const
        
          const is a variable that once it has been created, its value can never change.

  4.	Array Method 
  
    The .map() method allows you to run a function on each item in the array, returning a new array as the result.
    
      Ex:-
      
        const myArray = ['apple', 'banana', 'orange'];
        const myList = myArray.map(
                (item) => <p>{item}</p>
                )
                
  5.	Import and export modules
  
    In file X to import module from this file :- 
       
       Syntax :- import message from "./message.js";
  
    In fileY to export module to other file :-
     
       Syntax :- export default message;


  6.	Ternary Operator
 
    The ternary operator is a simplified conditional operator like if / else.
        
        Syntax: condition ? <expression if true> : <expression if false>
        
        Ex :- 
        
        function renderApp() {
          document.getElementById("demo").innerHTML = "Welcome!";
        }
        function renderLogin() {
          document.getElementById("demo").innerHTML = "Please log in";
        }
        let authenticated = false;
        authenticated ? renderApp() : renderLogin();
        
_6.	Render HTML_

        React renders HTML to the web page by using a function called ReactDOM.render().
        
        The ReactDOM.render() function takes two arguments, HTML code and an HTML element.
        
        The purpose of the function is to display the specified HTML code inside the specified HTML element.

        Ex :-
            import React from 'react';
            import ReactDOM from 'react-dom/client';

            const myelement = (
              <table>
                <tr>
                  <th>Name</th>
                </tr>
                <tr>
                  <td>John</td>
                </tr>
                <tr>
                  <td>Elsa</td>
                </tr>
              </table>
            );
            ReactDOM.render(myelement, document.getElementById('root'));  //to display the HTML code
            
__7.	 JSX__

        JSX stands for JavaScript XML.
        
        JSX allows us to write HTML in React.
        
        JSX makes it easier to write and add HTML in React.
        
        Ex:-
        
          const myElement = (
              <>
                <p>I am a paragraph.</p>
                <p>I am a paragraph too.</p>
              </>
            );
          const root = ReactDOM.createRoot(document.getElementById('root'));
          root.render(myElement);
          
          
__8.	React Component__

          •	Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML.

          •	Components come in two types, Class components and Function components.

       **Class Component**

          o	When creating a React component, the component's name must start with an upper case letter.

          o	The component has to include the extends React.Component statement, this statement creates an inheritance to React.Component, and gives your                 component access to React.Component's functions.

          o	The component also requires a render() method, this method returns HTML.

          Ex :-
              class Car extends React.Component {
                render() {
                  return <h2>Hi, I am a Car!</h2>;
                }
              }

              const root = ReactDOM.createRoot(document.getElementById('root'));
              root.render(<Car />);

                a)	Constructor with state(Component Properties  as object)

                Ex :-
                    class Car extends React.Component {
                      constructor() {
                        super();
                        this.state = {color: "red"};
                      }
                      render() {
                        return <h2>I am a {this.state.color} Car!</h2>;
                      }
                    }  

                    const root = ReactDOM.createRoot(document.getElementById('root'));
                    root.render(<Car />);.

                b)	Props in the Constructor

                Ex :-

                    class Car extends React.Component {
                      constructor(props) {
                        super(props);
                      }
                      render() {
                        return <h2>I am a {this.props.model}!</h2>;
                      }
                    }

                    const root = ReactDOM.createRoot(document.getElementById('root'));
                    root.render(<Car model="Mustang"/>); 

                c)	React Class Component State

                  I.	React Class components have a built-in state object.

                  II.	The state object is where you store property values that belongs to the component.

                  III.	When the state object changes, the component re-renders.

                Ex:-

                    class Car extends React.Component {
                      constructor(props) {
                        super(props);
                        this.state = {
                          brand: "Ford",
                          model: "Mustang",
                          color: "red",
                          year: 1964
                        }
                      }
                      render() {
                        return (
                          <div>
                            <h1>My Car</h1>
                          </div>
                        );
                      }
                    }


                d)	Changing the state Object

                  o	To change a value in the state object, use the this.setState() method.

                  o	When a value in the state object changes, the component will re-render, meaning that the output will change according to the new                            value(s).

                Ex:-
                    class Car extends React.Component {
                      constructor(props) {
                        super(props);
                        this.state = {
                          brand: "Ford",
                          model: "Mustang",
                          color: "red",
                          year: 1964
                        };
                      }
                      changeColor = () => {
                        this.setState({color: "blue"});
                      }
                      render() {
                        return (
                          <div>
                            <h1>My {this.state.brand}</h1>
                            <p>
                              It is a {this.state.color}
                              {this.state.model}
                              from {this.state.year}.
                            </p>
                            <button
                              type="button"
                              onClick={this.changeColor}
                            >Change color</button>
                          </div>
                        );
                      }
                }


          **Function Component**

          Ex:-

              function Car() {
                return <h2>I am a red Car!</h2>;
              }

              const root = ReactDOM.createRoot(document.getElementById('root'));
              root.render(<Car />);
