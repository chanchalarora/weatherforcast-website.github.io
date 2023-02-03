const form = document.querySelector("form");
const weatherInfo = document.querySelector("#weather-info");

form.addEventListener("submit", (e) => {
  e.preventDefault();

  const city = form.elements.city.value;

  weatherInfo.innerHTML = "Loading...";

  // Replace YOUR_API_KEY with your API key from a weather API provider
  const API_KEY = "7f260139f8db0b86bea8152660bda690";
  const API_URL = `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${API_KEY}`;

  fetch(API_URL)
    .then((response) => response.json())
    .then((data) => {
      const { name, main } = data;
      const { temp, feels_like, temp_min, temp_max } = main;

      weatherInfo.innerHTML = `
        <h2>Weather in ${name}:</h2>
        <p>Temperature: ${temp}°C</p>
        <p>Feels like: ${feels_like}°C</p>
        <p>Temperature range: ${temp_min}°C - ${temp_max}°C</p>
      `;
    })
    .catch((error) => {
      weatherInfo.innerHTML = "Could not get weather info. Please try again later.";
      console.error(error);
    });
});
