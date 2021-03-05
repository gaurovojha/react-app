What Is React?
React is a declarative, efficient, and flexible JavaScript library
It lets you compose complex UIs from small and isolated pieces of code called “components”.


A component takes in parameters, called props, and returns a hierarchy of views to display via the render method.
render returns a React element
eg:
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

Above JSX code is transformed to the below code :

return React.createElement('div', {className: 'shopping-list'},
  React.createElement('h1', /* ... h1 children ... */),
  React.createElement('ul', /* ... ul children ... */)
);


Since the Square components no longer maintain state, the Square components receive values from the Board component and inform the Board component when they’re clicked. In React terms, the Square components are now controlled components. The Board has full control over them.



Why Immutability Is Important
Data Change with Mutation:
var player = {score: 1, name: 'Gaurov'};
//update score
player.score = 2;

Data Change without Mutation:
var player = {score: 1, name: 'Gaurov'};
var newPlayer = Object.assign({}, player, {score: 2});
//using spread operator
var newPlayer = {...player, score: 2};

BENEFITS :
Complex Features Become Simple
Detecting Changes
Determining When to Re-Render in React : helps you build pure components in React.

List items in REACT

<li key={user.id}>{user.name}: {user.taskCount} tasks left</li>

It’s strongly recommended that you assign proper keys whenever you build dynamic lists.
React uses this key to identify changes in the list during rerender.
