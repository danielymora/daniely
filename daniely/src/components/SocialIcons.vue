<template>
    <section class="social-icons">
      <h2>Connect with Me</h2>
      <div class="icon-links">
        <a href="https://www.linkedin.com/in/daniely-rios-1876ba238" target="_blank">
        <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn" />
      </a>
      <a href="https://instagram.com/danielyrios" target="_blank">
        <img src="https://cdn-icons-png.flaticon.com/512/2111/2111463.png" alt="Instagram" />
      </a>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'SocialIcons'
  }
  </script>
  
  <style scoped>
  .social-icons {
    text-align: center;
    margin: 30px auto;
  }
  
  h2 {
    font-family: 'Poppins', sans-serif;
    font-size: 1.8em;
    color: #2c3e50;
    margin-bottom: 20px;
  }
  
  .icon-links {
    display: flex;
    justify-content: center;
    gap: 20px;
  }
  
  .icon-links a img {
    width: 40px;
    height: 40px;
  }
  </style>
  