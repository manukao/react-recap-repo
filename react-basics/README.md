### React.js Basics

---

- "Diamonds" / Fragments -> use instead of divs if you dont want/need another div, when rendering more than one parent
  <>
  </>

---

### Props

- can pass any type of data as prop
- strings need "" all other need {}
- can use props to conditionally render parts of a component
- example:

```javascript
function UserCard({ name, isFavorite }) {
  return (
    <div>
      {name}
      {isFavorite ? <span>🌟</span> : null}
    </div>
  );
}
```

- if/else statements are also possible
- keep components as "dumb" as possible

---

### Nested Components in React:

- {children} : In React, {children} is a special prop that allows you to pass children elements or components to a parent component.
- Why?: to compose components and make them reusable.

```javascript
function Card(props) {
  return;
  <div className="card">{props.children}</div>;
}

function App() {
  return (
    <Card>
      <h1>Card Title</h1>
      <p>Card Content</p>
    </Card>
  );
}
```

Explanation: In this example, we have a Card component that takes in a {children} prop. The Card component then renders a div with a class of card and the {children} prop.

In the App component, we are using the Card component and passing in two child elements: an h1 with the title of the card and a p with the content of the card.

By using {children}, we can create a reusable Card component that can display different content without having to modify the component's implementation.

---
