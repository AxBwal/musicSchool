<template>
  <div class="courses">
    <h2>Our Courses</h2>
    <ul class="course-list">
      <li v-for="course in courses" :key="course.id" @click="toggleCourseDetails(course.id)">
        <h3>{{ course.name }} →</h3>
        <div v-if="activeCourse === course.id" class="course-details">
          <p>{{ course.description }}</p>
          <p><strong>Duration:</strong> {{ course.duration }} months</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// Define the list of courses
const courses = [
  { id: 'guitar', name: 'Guitar Lessons', description: 'Learn the basics of guitar playing and advanced techniques.', duration: 3 },
  { id: 'piano', name: 'Piano Lessons', description: 'Master the piano with guidance from experienced instructors.', duration: 4 },
  { id: 'violin', name: 'Violin Lessons', description: 'Understand how to play the violin from scratch.', duration: 2 },
  { id: 'drums', name: 'Drum Lessons', description: 'Develop drumming skills with the best techniques.', duration: 5 }
]

// Store the ID of the currently active course
const activeCourse = ref(null)

// Toggle the visibility of the course details
const toggleCourseDetails = (courseId) => {
  activeCourse.value = activeCourse.value === courseId ? null : courseId
}
</script>

<style scoped>
.courses {
  padding: 80px;
  text-align: center;
  background-color: #f5f5f5;
  color: #000;
}

.course-list {
  list-style-type: none;
  padding: 0;
}

.course-list li {
  margin: 10px 0;
  padding: 20px;
  font-size: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
  cursor: pointer;
}

.course-list li h3 {
  margin: 0;
  color: #000;
}

.course-list li .course-details {
  margin-top: 10px;
  padding: 10px;
  background-color: #f9f9f9;
  border-radius: 5px;
  text-align: left;
}
</style>
