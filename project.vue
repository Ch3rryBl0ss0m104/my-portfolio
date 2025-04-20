<!-- Janke Rall u24571238 -->

<template>

  <div class="nav">
    <NuxtLink to="/" class="link">Home</NuxtLink>
    <NuxtLink to="/project" class="link">My Projects</NuxtLink>
    <NuxtLink to="/contact" class="link">Send Me A Message</NuxtLink>
  </div>

  <div class="projects">
    <h1 class="projectH">My Projects</h1>
    <div class="project-list">
      <div class="project-item">
        <h2>Song Playlist Viewers</h2>
        <p>View your Spotify playlist in a beautiful way!</p>
        <img src="/public/images/project1.png" alt="Project 1 screenshot" class="project-image" />
      </div>
      <div class="project-item">
        <h2>Lecture Venue Counter</h2>
        <p>Count the number of students in a lecture venue!</p>
        <img src="/public/images/project2.png" alt="Project 2 screenshot" class="project-image" />
      </div>
      <div class="project-item">
        <h2>Express Server</h2>
        <p>My Express server for handling HttP requests!</p>
        <img src="/public/images/project3.png" alt="Project 3 screenshot" class="project-image" />
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

  .projects {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
  }

  .projectH {
    color: #222129;
    font-size: 50px;
    text-align: center;
  }

  .project-list {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap; /* Allow wrapping to next line */
    justify-content: center; /* Center items */
    align-items: center; /* Center items vertically */
    min-width: 25%;;
  }

  .project-item {
    margin: 10px; /* Space between items */
    text-align: center; /* Center text */
    background-color: #f4f4f4;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  }

  .project-image {
    width: 100%;
    height: 300px; /* Maintain aspect ratio */
  }


</style>