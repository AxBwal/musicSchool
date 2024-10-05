<template>
  <div>
    <header class="header">
      <h1>Music School</h1>
      <nav>
        <NuxtLink to="/" class="nav-link">Home</NuxtLink>
        <NuxtLink to="/about" class="nav-link">About Us</NuxtLink>
        <NuxtLink to="/courses" class="nav-link">Courses</NuxtLink>
        <NuxtLink to="/contact" class="nav-link">Contact</NuxtLink>
      </nav>
    </header>
    <main>
      <NuxtPage />
    </main>
    <footer class="footer">
      <p>&copy; 2024 Music School. All rights reserved.</p>
    </footer>
  </div>
</template>

<style scoped>
/* General layout styles */
.header {
  background-color: #000;
  color: #fff;
  padding: 30px 0;
  text-align: center;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 1000;
}
.header h1 {
  font-size: 32px;
  margin-bottom: 10px;
  font-weight: bold;
  color: #fff;
}

/* Navigation styles */
nav {
  margin-top: 10px;
}
.nav-link {
  margin: 0 20px;
  font-size: 18px;
  color: #fff;
  text-decoration: none;
  padding: 10px 15px;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}
.nav-link:hover {
  background-color: #fff;
  color: #000;
}

/* Main content styling */
main {
  padding: 50px;
  background-color: #f5f5f5;
  min-height: 80vh;
}

/* Footer styles */
.footer {
  background-color: #000;
  color: white;
  text-align: center;
  padding: 20px 0;
  font-size: 14px;
  position: relative;
  bottom: 0;
  width: 100%;
  margin-top: 50px;
  box-shadow: 0px -2px 10px rgba(0, 0, 0, 0.1);
}
</style>
