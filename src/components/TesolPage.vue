<template>
  <div class="tesol-container">
    <header class="tesol-header">
      <h1>TESOL</h1>
      <p class="subtitle">Teaching English to Speakers of Other Languages</p>
    </header>

    <section class="lessons-section">
      <h2>Lessons I Learned in TESOL</h2>
      <ul class="lesson-list">
        <li v-for="(lesson, index) in lessons" :key="index">
          <span class="lesson-number">#{{ index + 1 }}</span>
          <p class="lesson-text">{{ lesson }}</p>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  name: "TesolPage",
  data() {
    return {
      lessons: [
        "Educators must be aware of their own biases and strive to create a safe and welcoming space for all students.",
        "It is important for teachers to strike a balance between utilizing technology and ensuring that it does not detract from the learning experience.",
        "One effective strategy for engaging TESOL learners is to use real-life examples. By connecting classroom content to students' personal experiences and interests, teachers can create a more meaningful and relevant learning experience.",
        "Another strategy for engaging TESOL learners is to incorporate multimedia into lessons. Videos, audio clips, and interactive online activities can help break up the monotony of traditional lectures and keep students engaged.",
        "Teachers can also use cultural sensitivity to understand and respect students' cultural differences and avoid misunderstandings."
      ]
    };
  }
};
</script>

<style scoped>
.tesol-container {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  max-width: 800px;
  margin: auto;
  padding: 2rem;
  color: #333;
  background-color: #f9f9f9;
  border-radius: 8px;
}

.tesol-header {
  text-align: center;
  margin-bottom: 2rem;
}

.tesol-header h1 {
  font-size: 2.5rem;
  color: #2c3e50;
}

.subtitle {
  font-size: 1rem;
  color: #7f8c8d;
}

.lessons-section h2 {
  color: #34495e;
  margin-bottom: 1rem;
}

.lesson-list {
  list-style: none;
  padding: 0;
}

.lesson-list li {
  background-color: #ffffff;
  border: 1px solid #e0e0e0;
  padding: 1rem;
  margin-bottom: 1rem;
  border-radius: 6px;
  display: flex;
  align-items: flex-start;
}

.lesson-number {
  font-weight: bold;
  margin-right: 0.75rem;
  color: #2980b9;
}

.lesson-text {
  flex: 1;
}
</style>
