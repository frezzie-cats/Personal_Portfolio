<template>
  <div class="resume-category">
    <h3 class="category-title">Education</h3>
    <v-row justify="center" class="education-row">
      <v-col cols="12" md="8" class="education-col">
        <v-card class="education-card" outlined>
          <v-card-title class="education-degree">Bachelor of Science in Information Technology</v-card-title>
          <v-card-subtitle class="education-subtitle">Caraga State University</v-card-subtitle>
          <v-card-text class="education-details">
            Graduated: 2022 - 2026<br />
            Achievements: Dean’s Lister
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'Education'
};
</script>

<style scoped>
.resume-category {
  margin-bottom: 40px;
  text-align: center; /* Center-align the whole section */
}
.category-title {
  font-size: 1.8rem;
  color: #b19cd9;
  margin: 40px 0 20px;
}
.education-row {
  display: flex;
  justify-content: center; 
}
</style>
