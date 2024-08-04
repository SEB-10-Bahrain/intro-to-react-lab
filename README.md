### Homework Assignment: Create a Weather App Using React and Vite

#### Objective
In this homework assignment, you will create a simple weather app using React and Vite. The app will display weather information using predefined arrays and fake state objects. You will practice conditional rendering using ternary expressions, transforming arrays into JSX elements with the `map()` method, and applying conditions to list items.

#### Instructions

1. **Setup the Project:**
   - Create a new React app using Vite.
     ```bash
     npm create vite@latest my-weather-app --template react
     cd my-weather-app
     npm install
     npm run dev
     ```

2. **Clean Up the App:**
   - Open `src/App.jsx` and delete all the Vite-provided content.
   - Replace it with the basic structure of a React component:
     ```jsx
      import './App.css'
      
      function App() {
      
      
        return (
          <>
            <h1>Weather App</h1>
          </>
        )
      }
      
      export default App
     ```

3. **Update CSS:**
   - Delete the contents of index.css (leave blank once deleted)
   - Open `src/App.css` and replace with some basic styles:
     ```css
        body {
          font-family: Arial, sans-serif;
          text-align: center;
          margin-top: 50px;
        }
        
        .weather-item {
          margin: 10px;
          padding: 10px;
          border: 1px solid #ddd;
          border-radius: 5px;
          display: inline-block;
        }
        
        .sunny {
          background-color: #f1c40f;
        }
        
        .cloudy {
          background-color: #ecf0f1;
        }
        
        .rainy {
          background-color: #3498db;
        }
     ```

5. **Define Arrays/Fake State Objects:**
   - Inside `App.jsx`, define some arrays and objects to represent the weather data:
     ```jsx
     const weatherData = [
       { day: 'Monday', condition: 'Sunny', temperature: 30 },
       { day: 'Tuesday', condition: 'Cloudy', temperature: 22 },
       { day: 'Wednesday', condition: 'Rainy', temperature: 18 },
       { day: 'Thursday', condition: 'Sunny', temperature: 28 },
       { day: 'Friday', condition: 'Cloudy', temperature: 24 },
     ];

     const isSunny = (condition) => condition === 'Sunny';
     const isCloudy = (condition) => condition === 'Cloudy';
     const isRainy = (condition) => condition === 'Rainy';
     ```

6. **Conditional Rendering Using Ternary Expressions:**
   - Use ternary expressions to conditionally render content based on the weather conditions:
     ```jsx
     function App() {
       return (
         <div className="App">
           <h1>Weather App</h1>
           <div>
             {weatherData.map((item, index) => (
               <div
                 key={index}
                 className={`weather-item ${
                   isSunny(item.condition) ? 'sunny' : isCloudy(item.condition) ? 'cloudy' : 'rainy'
                 }`}
               >
                 <h2>{item.day}</h2>
                 <p>{item.condition}</p>
                 <p>{item.temperature}°C</p>
               </div>
             ))}
           </div>
         </div>
       );
     }
     ```

7. **Using `map()` to Transform Arrays into JSX Elements:**
   - The `weatherData` array is already being transformed into JSX elements using the `map()` method in the code snippet above.

8. **Applying Conditions in Loops to Change List Item Display:**
   - The conditions applied in the `map()` method ensure that each list item is displayed differently based on the weather condition.

#### Deliverables
- A React app created using Vite.
- `src/App.jsx` file with the modified content.
- Basic styles added to `src/App.css`.
- Arrays and fake state objects representing weather data.
- Implementation of conditional rendering using ternary expressions.
- Use of the `map()` method to loop through arrays and transform them into JSX elements.

#### Submission
- Upload the project folder to a GitHub repository.
- Provide a link to your GitHub repository for review.
