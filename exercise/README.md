# Intro to React Lab - Exercise

## Overview

In this lab, you'll build as many simple applications as you can within the `App.jsx` file. These applications will utilize the concepts of JavaScript in JSX, conditional rendering, and looping in JSX. Here are the app ideas you can choose from:

1. **Shopping List App**:
   - Display a list of items to buy.
   - Indicate whether each item has been purchased.
   - Use conditional rendering to style purchased items differently.

2. **Movie Watchlist App**:
   - List movies to watch.
   - Indicate whether each movie has been watched.
   - Use conditional rendering to show a different message or style for watched movies.

3. **Book Reading Tracker**:
   - Display a list of books.
   - Indicate whether each book has been read.
   - Use conditional rendering to differentiate read books from unread ones.

4. **Daily Planner**:
   - Show a list of daily tasks.
   - Indicate whether each task is completed.
   - Use conditional rendering to show a "Completed" message or style for completed tasks.

5. **Recipe Ingredients Checker**:
   - List ingredients needed for a recipe.
   - Indicate whether each ingredient is available.
   - Use conditional rendering to highlight missing ingredients.

6. **Workout Routine App**:
   - List exercises in a workout routine.
   - Indicate whether each exercise has been completed.
   - Use conditional rendering to show completed exercises differently.

7. **Course Progress Tracker**:
   - Display a list of courses or modules.
   - Indicate whether each course or module has been completed.
   - Use conditional rendering to show progress and completed modules.

8. **Budget Tracker**:
   - List expenses.
   - Indicate whether each expense is within budget or over budget.
   - Use conditional rendering to show a warning message for over-budget expenses.

9. **Travel Itinerary Planner**:
   - Display a list of places to visit.
   - Indicate whether each place has been visited.
   - Use conditional rendering to mark visited places.

10. **Event RSVP List**:
    - Show a list of event attendees.
    - Indicate whether each attendee has confirmed their RSVP.
    - Use conditional rendering to highlight confirmed attendees.

## Instructions

1. **Choose an App Idea**: Select one of the app ideas listed above to start with.

2. **Create the App Structure**:
    - Use an array to store the data for your app (e.g., a list of items, movies, books, tasks, etc.).
    - Map through the array to dynamically generate the list items in JSX.

3. **Implement Conditional Rendering**:
    - Use conditional rendering to display different styles or messages based on the data (e.g., whether an item is purchased, a movie is watched, a task is completed, etc.).

4. **Use CSS for Styling**:
    - Clear the contents of the `index.css`.
    - Edit the `App.css` file for custom styles specific to your app.
    - Import and use the styles at the top of your `App.jsx` file.

    ```jsx
    // src/App.jsx
    import './App.css';

    // src/App.css
    .completed {
      text-decoration: line-through;
    }

    .not-completed {
      color: red;
    }
    ```

5. **Build and Test**:
    - Build your app and test it in the browser.
    - Make sure the conditional rendering and looping work as expected.

6. **Repeat**:
    - Once you finish one app, select another app idea from the list and repeat the process.
    - Try to build as many apps as you can within the given time.

## Example: Shopping List App

Here is an example of how you might build the Shopping List App:

```jsx
// src/App.jsx
import './App.css';

const App = () => {
  const items = [
    { name: 'Milk', purchased: true },
    { name: 'Bread', purchased: false },
    { name: 'Eggs', purchased: true },
  ];

  return (
    <>
      <h1>Shopping List</h1>
      <ul>
        {items.map((item, index) => (
          <li key={index} className={item.purchased ? 'completed' : 'not-completed'}>
            {item.name}
          </li>
        ))}
      </ul>
    </>
  );
}

export default App;
```

```css
/* src/App.css */
.completed {
  text-decoration: line-through;
}

.not-completed {
  color: red;
}
```


Build as many simple applications as you can, practicing the core concepts of JavaScript in JSX, conditional rendering, and looping in JSX. Focus on creating a functional and visually appealing app for each idea you choose.

Good luck and have fun!
