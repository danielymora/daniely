<template>
  <div id="app">
    <header>
      <h1>Daniely Rios</h1>
    </header>
    <main class="main-content">
      <div class="profile-container">
        <ProfileImage />
        <AboutMe />
      </div>
      <SocialIcons />
    </main>
  </div>
</template>

<script>
import AboutMe from './components/AboutMe.vue'
import SocialIcons from './components/SocialIcons.vue'
import ProfileImage from './components/ProfileImage.vue'

export default {
  name: 'App',
  components: {
    AboutMe,
    SocialIcons,
    ProfileImage
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600&family=Poppins:wght@400;600&display=swap');

/* Global Reset for margins, paddings, and overflow */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body, html {
  width: 100%;
  overflow-x: hidden; /* Prevent horizontal scroll */
}

#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
}

header {
  background-color: #053272;
  color: white;
  width: 100%; /* Ensure the header takes the full width */
  padding: 20px 0;
  box-sizing: border-box; /* Include padding in width calculation */
  margin: 0 auto; /* Center the header with no extra space */
}

h1 {
  font-size: 3em;
  font-weight: 600;
  font-family: 'Poppins', sans-serif;
  margin: 0;
  text-align: center;
}

.main-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 20px;
  width: 100%;
}

.profile-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-direction: row;
  gap: 20px;
  width: 100%;
  max-width: 1000px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  background-color: white;
}

/* Media Query for screens smaller than 768px (mobile) */
@media (max-width: 768px) {
  .profile-container {
    flex-direction: column;
    align-items: center;
    padding: 10px;
    width: 100%; /* Ensure it takes the full width */
  }

  .about-me {
    width: 100%;
    padding: 15px;
    border: 1px solid #ccc;
    border-radius: 8px;
    margin-bottom: 20px;
  }

  img {
    width: 150px;
    height: 150px;
  }

  h1 {
    font-size: 2em;
  }
}

footer {
  text-align: center;
  padding: 20px;
  background-color: #333;
  color: white;
}

/* Additional Media Query to handle extra small devices (i.e., 320px width) */
@media (max-width: 480px) {
  h1 {
    font-size: 1.8em;
  }

  .profile-container {
    padding: 10px;
  }

  .about-me {
    padding: 10px;
  }

  header {
    padding: 10px 0;
  }
}
</style>

