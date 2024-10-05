<template>
  <div class="home">
    <h2>Welcome to Music School</h2>
    <p>Your gateway to learning music from the best instructors.</p>
    <NuxtLink to="/courses" class="cta-button">Explore Our Courses</NuxtLink>
  </div>
</template>

<style scoped>
.home {
  text-align: center;
  padding: 100px 0;
  background-color: #fff;
  color: #000;
  min-height: 70vh;
}
.home h2 {
  font-size: 48px;
  margin-bottom: 20px;
}
.home p {
  font-size: 20px;
  margin-bottom: 40px;
  font-weight: 300;
}
.cta-button {
  background-color: #000;
  color: white;
  padding: 15px 30px;
  font-size: 18px;
  border-radius: 50px;
  text-decoration: none;
  transition: background-color 0.3s ease, transform 0.3s ease;
}
.cta-button:hover {
  background-color: #fff;
  color: #000;
  transform: scale(1.05);
}
</style>
