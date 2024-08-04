# Level Up: CSS Styling in React

## Introduction to CSS Styling in React

In React, CSS styling can be applied to your components in various ways. For this level up, we'll focus on three common approaches:

1. **Inline Styles**
2. **CSS Modules**
3. **Global CSS**

### 1. Inline Styles

Inline styles in React are defined using a JavaScript object. Each key in the object corresponds to a CSS property, and each value corresponds to the value of that property.

**Example:**

```jsx
const style = {
  color: 'blue',
  backgroundColor: 'lightgray',
  padding: '10px',
};

const App = () => {
  return (
    <div style={style}>
      <h1>Inline Styled Header</h1>
    </div>
  );
}
```


### 2. CSS Modules

CSS Modules allow you to scope CSS to the component, avoiding naming conflicts. This approach involves creating a separate CSS file for each component and importing it into your React component.

**Example:**

1. Create a `Button.css` file:

```css
/* Button.css */
.button {
  background-color: blue;
  color: white;
  padding: 10px;
  border: none;
  border-radius: 5px;
}
```

2. Import and use the CSS module in your component:

```jsx
import styles from './Button.css';

const App = () => {
  return <button className={styles.button}>Click Me</button>;
};
```

### 3. Global CSS

Global CSS is applied across the entire application and is useful for shared styles or base styles. You typically import global CSS files in the `index.js` or `App.js` file.

**Example:**

1. Create an `App.css` file:

```css
/* App.css */
body {
  font-family: Arial, sans-serif;
}

h1 {
  color: darkblue;
}

.completed {
  text-decoration: line-through;
  color: gray;
}

.not-completed {
  color: red;
}
```

2. Import the global CSS in your `App.js` file:

```jsx
import './App.css';

const App = () => {
  return (
    <div>
      <h1 className="completed">Completed Task</h1>
      <h1 className="not-completed">Incomplete Task</h1>
    </div>
  );
}
```

## Challenges

1. **Inline Styling Challenge:**
   - For your **Recipe Ingredients Checker** app, use inline styles to highlight missing ingredients in red and available ingredients in green.

2. **CSS Modules Challenge:**
   - For your **Workout Routine App**, create a CSS Module to style each exercise based on whether it’s completed or not. Ensure that completed exercises have a distinct style compared to incomplete ones.

3. **Global CSS Challenge:**
   - For your **Course Progress Tracker**, use global CSS to style the entire list of courses. Ensure that completed courses are displayed differently from the incomplete ones. Apply a base style to the app, such as font family and colors.

4. **Responsive Styling Challenge:**
   - Choose any app and make it responsive. Use media queries in your global CSS or CSS Modules to adjust styles for different screen sizes (e.g., mobile vs. desktop).

**Example of Responsive Styling:**

```css
/* App.css */
@media (max-width: 600px) {
  .completed, .not-completed {
    font-size: 14px;
    padding: 5px;
  }
}
```

## Conclusion

Experiment with different CSS styling approaches to see which works best for your React applications. Each method has its use cases and benefits, so understanding them will help you make better design choices for your projects. Have fun styling your apps!
