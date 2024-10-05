<template>
  <div class="contact">
    <h2>Contact Us</h2>
    <form @submit.prevent="submitForm">
      <input type="text" v-model="name" placeholder="Your Name" />
      <span v-if="errors.name">{{ errors.name }}</span>
      
      <input type="email" v-model="email" placeholder="Your Email" />
      <span v-if="errors.email">{{ errors.email }}</span>
      
      <textarea v-model="message" placeholder="Your Message"></textarea>
      <span v-if="errors.message">{{ errors.message }}</span>
      
      <button type="submit">Send Message</button>
    </form>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  message: ''
})

const errors = reactive({
  name: '',
  email: '',
  message: ''
})

const validateForm = () => {
  errors.name = form.name ? '' : 'Name is required.'
  errors.email = /\S+@\S+\.\S+/.test(form.email) ? '' : 'Valid email is required.'
  errors.message = form.message ? '' : 'Message is required.'
  
  return !errors.name && !errors.email && !errors.message
}

const submitForm = () => {
  if (validateForm()) {
    // Process form data
    alert('Message sent successfully!')
  }
}
</script>

<style scoped>
.contact {
  padding: 80px;
  text-align: center;
  background-color: #fafafa;
}
form {
  display: flex;
  flex-direction: column;
  max-width: 400px;
  margin: 0 auto;
}
input, textarea {
  margin: 15px 0;
  padding: 15px;
  font-size: 16px;
  border-radius: 8px;
  border: 1px solid #ccc;
  width: 100%;
  background-color: #fff;
}
button {
  background-color: #000;
  color: white;
  padding: 15px;
  border: none;
  font-size: 16px;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}
button:hover {
  background-color: #333;
}
span {
  color: red;
  font-size: 14px;
}
</style>
