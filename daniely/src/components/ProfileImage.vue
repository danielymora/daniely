<template>
    <section class="profile-image">
      <img src="@/assets/daniely.jpg" alt="Daniely Rios" />
    </section>
  </template>
  
  <script>
  export default {
    name: 'ProfileImage'
  }
  </script>
  
  <style scoped>
  .profile-image img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.2);
    object-fit: cover;
  }
  </style>
  