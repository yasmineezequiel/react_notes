# react_notes
React is a JavaScript library for user interface. 
V in MVC which is the view. 
React is only the view, we don't store all of the date in it we use as a library not a framework.
https://codeburst.io/react-js-for-beginners-the-basics-87ef6e54dae7

Props;
Is a short for properties. Is how components 'talk' to each other, props flow downwards from the parent component. Props do not change their state. Props are used for passing data from parent to child or by the component itself

Components are independent, reusable code block, which divides the UI into smaller pieces.
React has two types of components: Functional (Stateless) and Class (Statefull)
Functional (Stateless);
Is basically a JavaScript(or ES6) function which returns a real element.
exp; 
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
Class (Statefull)
is bigger code 
starts with class 

A component is being called like an HTML tag, but starting with a capital letter:
<FirstChild />    // we can call a component like an HTML tag
https://codeburst.io/react-js-understanding-functional-class-components-e65d723e909

 
can I have many props in the same component?


State
can be changed, there is no state in function component, you have to use class in this case.

rce(from VS code)
react component export
state = {
  object: 'This is a state in a function'
}
debugger; for react
how to change the state;
this.setState({

})

Separation of concerns
life cycle and component Didmount componentwillmount 
 this. (can only be used in class components)
 we can only call render in a class component 
 not possible to use lifecycle components into function component only in class component.


 Cypress enables you to write all types of tests:

End-to-end tests
Integration tests
Unit tests
Cypress can test anything that runs in a browser

The render method returns a description of what you want to see on the screen. React takes the description and displays the result. In particular, render returns a React element, which is a lightweight description of what to render. Most React developers use a special syntax called “JSX” which makes these structures easier to write. The <div /> syntax is transformed at build time to React.createElement('div'). 
 React has a few different kinds of components, but we’ll start with React.Component subclasses:

class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}

// Example usage: <ShoppingList name="Mark" />

The example above is equivalent to:

return React.createElement('div', {className: 'shopping-list'},
  React.createElement('h1', /* ... h1 children ... */),
  React.createElement('ul', /* ... ul children ... */)
);

The ShoppingList component above only renders built-in DOM components like <div /> and <li />. But you can compose and render custom React components too. For example, we can now refer to the whole shopping list by writing <ShoppingList />. Each React component is encapsulated and can operate independently; this allows you to build complex UIs from simple components.

component test will be the base of our 7th week challenge 