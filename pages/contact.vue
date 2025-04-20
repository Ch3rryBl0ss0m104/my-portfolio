<!-- Janke Rall u24571238 -->

<template>

  <div class="nav">
    <NuxtLink to="/" class="link">Home</NuxtLink>
    <NuxtLink to="/project" class="link">My Projects</NuxtLink>
    <NuxtLink to="/contact" class="link">Send Me A Message</NuxtLink>
    
  </div>

  <div class="contact-form">
    <h1 class="contactH">Contact Me</h1>
    <form name="contact" netlify netlify-honeypot="bot-field" data-netlify="true" method="POST">
      <input type="hidden" name="form-name" value="contact" />
      <p>
        <label for="name">Name:</label>
        <br/>
        <input type="text" id="name" name="name" required />
      </p>
      <p>
        <label for="email">Email:</label>
        <br/>
        <input type="email" id="email" name="email" required />
      </p>
      <p>
        <label for="message">Message:</label>
        <br/>
        <textarea id="message" name="message" required></textarea>
      </p>
      <button type="submit" class="submitBtn">Send</button>
    </form>
  </div>
</template>

<style>
  form {
    display: flex;
    flex-direction: column;
    max-width: 400px;
    margin: auto;
  }
  label {
    margin-bottom: 5px;
  }
  input, textarea {
    margin-bottom: 15px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  button:hover {
    background-color: #222129;
  }
  .contactH {
    margin-top: 20px;
    color: #222129;
    font-size: 50px;
    text-align: center;
  }
  .contact-form {
    margin: 20px auto;
    padding: 20px;
    background-color: #f4f4f4;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
  }
  .submitBtn {
    margin-top: 10px;
    background-color: #555;
    color: rgb(255, 255, 255);
    border: none;
    border-radius: 4px;
    padding: 10px 15px;
    cursor: pointer;
  }
</style>
