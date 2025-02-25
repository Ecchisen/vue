<template>
  <div id="app">
    <header>
      <nav>
        <div class="logo">My Notes Hub</div>
        <ul class="nav-links">
          <li><a href="#">Home</a></li>
        </ul>
      </nav>
    </header>

    <div class="container">
      <Sidebar @semesterSelected="loadSemesterContent" />
      <SemesterContent :data="selectedSemesterData" v-if="selectedSemesterData" />
    </div>

    <footer>
      <p>&copy; 2025 My Notes Hub. All rights reserved.</p>
    </footer>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue';
import SemesterContent from './components/SemesterContent.vue';

export default {
  components: {
    Sidebar,
    SemesterContent
  },
  data() {
    return {
      selectedSemesterData: null
    };
  },
  methods: {
    loadSemesterContent(semesterData) {
      this.selectedSemesterData = semesterData;
    }
  }
};
</script>

<style>
/* Import your CSS styles here */
@import './assets/style.css';
</style>
