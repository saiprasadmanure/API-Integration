# API-Integration
COMPANY: CODTECH IT SOLUTIONS
NAME : M SAIPRASAD
INTERN ID:CT06DL980
DOMAIN: FULL STACK WEB DEVELOPMENT
DURATION : 6 WEEKS
MENTOR : NEELA SANTOSH


This weather application is a simple, responsive, and interactive web-based project built using HTML, CSS, and JavaScript. Its primary function is to allow a user to enter the name of a city and fetch real-time weather information using the OpenWeatherMap API. Let’s explore how each part of the code contributes to its functionality and usability.

1. HTML Structure
The code begins with a standard <!DOCTYPE html> declaration, followed by the <html> tag with the lang="en" attribute indicating the language is English. Inside the <head> section, we define metadata such as the character encoding (UTF-8) and viewport settings for responsive design (width=device-width, initial-scale=1.0). The <title> tag gives the page a name – "Weather App" – which appears in the browser tab.

The body contains a <div> with a class of "container", which serves as the main content box centered on the page. Inside this container:

A heading (<h1>) displays the title "Weather App".

An <input> field allows the user to type in a city name.

A <button> labeled “Get Weather” triggers a JavaScript function when clicked.

A <div> with the ID "weather-result" is reserved for displaying the fetched weather data or any error messages.

2. Styling with CSS
The style block within the <head> tag provides the CSS needed to design the application visually. It ensures a clean and modern interface using styles such as:

Body styling: The entire body has a light grayish background (#f0f4f8) and uses Flexbox to center the container both horizontally and vertically. The font used is Arial, a widely supported sans-serif font for readability.

Container styling: This block is white, with padding and rounded corners to create a card-like appearance. A subtle shadow gives it a lifted effect, which enhances visual appeal.

Input styling: The input field is padded, has rounded borders, and stretches across 70% of the container width, making it user-friendly on both mobile and desktop.

Button styling: The button has a modern blue background (#007BFF), white text, and rounded edges. It changes the cursor to a pointer on hover, indicating it is clickable.

Weather result styling: The result section is slightly larger in font size to stand out once data is populated.

3. JavaScript Functionality
The functionality of the weather app is powered by a single JavaScript function: getWeather(). Here's how it works:

It first retrieves the value entered in the input field using document.getElementById("city").value.

It validates that a city name was entered. If the input is empty, it displays a message asking the user to enter a city.

If a city is entered, the function constructs an API URL to call the OpenWeatherMap API. This URL includes the city name, a predefined API key (fe614f473704ba32d3a0c5e64f73a042), and a units=metric parameter to get the temperature in Celsius.

javascript
Copy
Edit
const url = `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}&units=metric`;
Using the fetch() function with await, the script asynchronously requests weather data from the API. If the response is not OK (for example, if the city is invalid), it throws an error and displays a message.

When the response is successful, it parses the JSON data using response.json() and constructs a string with key weather details:

City name

Temperature in Celsius

Weather description (like "clear sky" or "rain")

Wind speed

This information is inserted into the weather-result div using innerHTML, dynamically updating the webpage without requiring a page reload.

4. Conclusion
This Weather App is an excellent example of a beginner-friendly web development project that demonstrates core frontend concepts:

HTML for structure

CSS for design and responsiveness

JavaScript for dynamic content and API interaction

It also showcases the use of asynchronous programming with async/await, and working with a real-world third-party RESTful API (OpenWeatherMap). Despite being simple in design, it effectively integrates all the essential building blocks of a dynamic web application, making it a strong base for adding more advanced features like forecast data, unit toggles, and geolocation.

This type of project is especially useful for internships or portfolio-building as it proves familiarity with external APIs, DOM manipulation, and clean UI design practices.


#OUTPUT     
![Image](https://github.com/user-attachments/assets/9f11ead5-485c-43b3-b6f3-a8e4c0cbefed)
