<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <aside id="sidebar">
      <h3>Semesters</h3>
      <ul class="semester-links">
        <li v-for="(data, semester) in semesters" :key="semester">
          <a href="#" @click.prevent="selectSemester(semester)">
            <i :class="icons[semester]"></i> Semester {{ semester }}
          </a>
        </li>
      </ul>
    </aside>
  </template>
  
  <script>
  export default {
    data() {
      return {
        semesters: {
          1: { notes: "Notes for Semester 1", assignments: "Assignments for Semester 1", exams: "Exam Questions for Semester 1", labReports: "Lab Reports for Semester 1" },
          2: { notes: "Notes for Semester 2", assignments: "Assignments for Semester 2", exams: "Exam Questions for Semester 2", labReports: "Lab Reports for Semester 2" },
          3: { notes: "Notes for Semester 3", assignments: "Assignments for Semester 3", exams: "Exam Questions for Semester 3", labReports: "Lab Reports for Semester 3" },
          4: { notes: "Notes for Semester 4", assignments: "Assignments for Semester 4", exams: "Exam Questions for Semester 4", labReports: "Lab Reports for Semester 4" },
          5: { notes: "Notes for Semester 5", assignments: "Assignments for Semester 5", exams: "Exam Questions for Semester 5", labReports: "Lab Reports for Semester 5" },
          6: { notes: "Notes for Semester 6", assignments: "Assignments for Semester 6", exams: "Exam Questions for Semester 6", labReports: "Lab Reports for Semester 6" },
          7: { notes: "Notes for Semester 7", assignments: "Assignments for Semester 7", exams: "Exam Questions for Semester 7", labReports: "Lab Reports for Semester 7" },
          8: { notes: "Notes for Semester 8", assignments: "Assignments for Semester 8", exams: "Exam Questions for Semester 8", labReports: "Lab Reports for Semester 8" },
        },
        icons: {
          1: "fas fa-laptop-code",
          2: "fas fa-code",
          3: "fas fa-database",
          4: "fas fa-globe",
          5: "fas fa-network-wired",
          6: "fas fa-mobile-alt",
          7: "fas fa-cloud",
          8: "fas fa-graduation-cap",
        }
      };
    },
    methods: {
      selectSemester(semester) {
        this.$emit('semesterSelected', this.semesters[semester]);
      }
    }
  };
  </script>
  