<!-- Janke Rall u24571238 -->

<script setup>
    const { data: weather } = await useFetch ('https://api.openweathermap.org/data/2.5/weather?q=Pretoria&appid=8ec0c06671e90a0743d3f7408f509947')
    const { data: dog } = await useFetch('https://dog.ceo/api/breeds/image/random')
</script>

<template>
  <div>
  
    <div class="nav">
      <NuxtLink to="/" class="link">Home</NuxtLink>
      <NuxtLink to="/project" class="link">My Projects</NuxtLink>
      <NuxtLink to="/contact" class="link">Send Me A Message</NuxtLink>
      
    </div>
  
    <div class="me">
      <h1>Janke Rall</h1>
      <div class="info">
        <img src="/public/images/my-photo.jpg" alt="My Photo" height="200px" class="images myPhoto" />
        <p>This is my portfolio</p>
        <p>Feel free to explore my projects and get in touch!</p>
      </div>
    </div>

    <h1 id="apiH">APIs</h1>
    <div class="apis">
      <div class="weather-info"> 
        <h2>Current Weather</h2>
        <p>{{ weather?.weather[0].description }}</p>
        <p>Temperature: {{ (weather?.main.temp - 273.15).toFixed(2) }} °C</p>
        <p>Humidity: {{ weather?.main.humidity }}%</p>
        <p>Wind Speed: {{ weather?.wind.speed }} m/s</p>
        <p>Location: {{ weather?.name }}</p>
      </div>
      
      <div class="dog-image">
          <h2>Meet a Random Dog!</h2>
          <img :src="dog?.message" alt="Cute Dog" height="200px" class="images" />
      </div>
    </div>

  </div>
</template>

<style>

  .nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: #222129;
    padding: 20px;
    color: white;
    font-size: 18px;
    font-weight: bold;
    position: sticky;
    top: 0;
  }

  .me {
    display: flex;
    justify-content: space-around;
    align-items: normal;
    flex-direction: row;
    margin-top: 20px;
    margin-bottom: 60px;
  }

  .link {
    color: white;
    text-decoration: none;
  }

  body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
  }
  
  h1 {
    color: #222129;
    font-size: 50px;
  }

  h1#apiH {
    margin-top: 20px;
    color: #222129;
    font-size: 50px;
    text-align: center;
  }

  p {
    font-size: 16px;
    line-height: 1.5;
  }

  img {
    border-radius: 10px;
    margin-bottom: 20px;
  }

  a {
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }

  h2 {
    margin-top: 20px;
    color: #555;
  }

  div {
    margin: 20px 0;
  }

  img {
    max-width: 100%;
    height: auto;
  }

  .apis {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  }

  .weather-info {
    padding: 20px;
  }

  .dog-image {
    border-radius: 10px;
    margin-top: 10px;
  }

  .images {
    height: 200px;
  }

  .myPhoto {
    border-radius: 50%;
    margin-bottom: 20px;
  }
</style>