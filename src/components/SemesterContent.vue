<template>
    <main id="content">
      <h2>Semester Content</h2>
      <div v-if="data">
        <div class="section">
          <h3>Notes</h3>
          <p>{{ data.notes }}</p>
        </div>
        <div class="section">
          <h3>Assignments</h3>
          <p>{{ data.assignments }}</p>
        </div>
        <div class="section">
          <h3>Exams</h3>
          <p>{{ data.exams }}</p>
        </div>
        <div class="section">
          <h3>Lab Reports</h3>
          <p>{{ data.labReports }}</p>
        </div>
      </div>
      <p v-else>Please select a semester.</p>
    </main>
  </template>
  
  <script>
  export default {
    props: {
      data: Object
    }
  };
  </script>
  