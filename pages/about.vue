<template>
  <div class="about">
    <div class="about-content">
      <h2>About Our Music School</h2>
      <p class="description">
        At Music School, we offer a wide range of music lessons designed for all ages and skill levels. Whether you're a beginner looking to learn the basics or an advanced musician seeking to refine your skills, we have the perfect course for you.
      </p>
      <div class="values-section">
        <div class="value-item">
          <h3>🎶 Professional Instructors</h3>
          <p>
            Our team of professional instructors are passionate about music and dedicated to helping you reach your goals.
          </p>
        </div>
        <div class="value-item">
          <h3>🎸 Personalized Lessons</h3>
          <p>
            We offer personalized one-on-one lessons, ensuring that you receive the attention and guidance you need to excel.
          </p>
        </div>
        <div class="value-item">
          <h3>🎤 Variety of Instruments</h3>
          <p>
            From guitar to piano, violin to drums, we offer lessons for a wide variety of instruments to suit your passion.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about {
  padding: 100px 20px;
  background-color: #f5f5f5;
  text-align: center;
  color: #333;
}

.about-content {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

h2 {
  font-size: 36px;
  margin-bottom: 20px;
  font-weight: bold;
  color: #000;
}

.description {
  font-size: 18px;
  margin-bottom: 40px;
  line-height: 1.6;
}

.values-section {
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.value-item {
  background-color: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.value-item h3 {
  font-size: 24px;
  margin-bottom: 10px;
  color: #000;
}

.value-item p {
  font-size: 16px;
  color: #555;
  line-height: 1.6;
}

.value-item:hover {
  transform: scale(1.05);
}


@media (min-width: 768px) {
  .values-section {
    flex-direction: row;
    justify-content: space-between;
  }
  .value-item {
    flex: 1;
    margin: 0 15px;
  }
}
</style>
