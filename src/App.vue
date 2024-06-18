<!-- src/App.vue -->
<script setup>
import Biodata from './components/Biodata.vue'
</script>

<template>
  <div class="app-container">
    <div class="personal-photo-container">
      <img src="./assets/fauzikri.jpg" class="personal-photo" alt="Personal Photo" />
    </div>
    <Biodata 
      name="fauzikri ghifari" 
      :age="21" 
      location="PEKANBARU, RIAU" 
      profession="Software Developer" 
      hobbies="Play games"
      teknikInformatika="Teknik Informatika 2024"
      contact="+62 895-6309-53274"
      email="fauzikri2003@gmail.com"
      instagram="https://www.instagram.com/stmw_dragon_/"
    />
  </div>
</template>

<style scoped>
.app-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  background: linear-gradient(135deg, #525354, #434547, #444648);
  padding: 20px;
  box-sizing: border-box;
}

.personal-photo-container {
  margin-bottom: 20px;
}

.personal-photo {
  height: 150px;
  width: 150px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #1e201f;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.personal-photo:hover {
  transform: scale(1.1);
  box-shadow: 0 0 15px rgba(36, 38, 37, 0.7);
}
</style>
