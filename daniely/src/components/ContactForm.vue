<template>
    <section>
      <h2>Contact Me</h2>
      <form @submit.prevent="sendEmail">
        <div>
          <label for="name">Name:</label>
          <input v-model="name" type="text" id="name" required />
        </div>
        <div>
          <label for="email">Email:</label>
          <input v-model="email" type="email" id="email" required />
        </div>
        <div>
          <label for="message">Message:</label>
          <textarea v-model="message" id="message" required></textarea>
        </div>
        <button type="submit">Send Message</button>
      </form>
      <p v-if="feedback">{{ feedback }}</p>
    </section>
  </template>
  
  <script>
  import emailjs from 'emailjs-com'
  
  export default {
    data() {
      return {
        name: '',
        email: '',
        message: '',
        feedback: ''
      }
    },
    methods: {
      sendEmail() {
        const templateParams = {
          name: this.name,
          email: this.email,
          message: this.message
        }
        emailjs
          .send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams, 'YOUR_USER_ID')
          .then(
            () => {
              this.feedback = 'Your message has been sent!'
              this.name = ''
              this.email = ''
              this.message = ''
            },
            (error) => {
              console.log('Failed...', error)
              this.feedback = 'There was an error sending your message. Please try again later.'
            }
          )
      }
    }
  }
  </script>
  
  <style scoped>
  form {
    display: flex;
    flex-direction: column;
    max-width: 400px;
    margin: 0 auto;
  }
  div {
    margin-bottom: 10px;
  }
  input, textarea {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  button {
    padding: 10px;
    background-color: #333;
    color: white;
    border: none;
    cursor: pointer;
  }
  button:hover {
    background-color: #555;
  }
  </style>
  