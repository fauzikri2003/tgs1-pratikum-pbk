<!-- src/components/Biodata.vue -->
<template>
    <div class="biodata">
      <h2>{{ name }}</h2>
      <p>Age: {{ age }}</p>
      <p>Location: {{ location }}</p>
      <p>Profession: {{ profession }}</p>
      <p>Hobbies: {{ hobbies }}</p>
      <p>Teknik Informatika: {{ teknikInformatika }}</p>
      <p>Contact: {{ contact }}</p>
      <p>Email: {{ email }}</p>
      <p>Instagram: <a :href="instagramLink" target="_blank">{{ instagram }}</a></p>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue'
  
  const props = defineProps({
    name: String,
    age: Number,
    location: String,
    profession: String,
    hobbies: String,
    socialMedia: String,
    teknikInformatika: String,
    contact: String,
    email: String,
    instagram: String
  })
  
  const instagramLink = `https://www.instagram.com/${props.instagram}/`
  </script>
  
  <style scoped>
  .biodata {
    background: #ffffff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    text-align: center;
    max-width: 300px;
  }
  
  .biodata h2 {
    margin: 0;
    color: #191c1b;
    font-size: 24px;
  }
  
  .biodata p {
    margin: 10px 0;
    font-size: 16px;
    color: #333;
  }
  
  .biodata a {
    color: #3498db;
    text-decoration: none;
  }
  
  .biodata a:hover {
    text-decoration: underline;
  }
  </style>
  