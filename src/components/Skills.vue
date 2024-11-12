<!-- src/components/Resume.vue -->

<template>
    <v-container class="resume-section" fluid>
      <v-row justify="center">
        <v-col cols="12" md="10">
          <!-- Skills Section (Updated with icons and progress bars) -->
          <div class="resume-category">
            <h3 class="category-title">Skills</h3>
            <v-row>
              <!-- Skill 1: JavaScript -->
              <v-col cols="12" md="6">
                <v-row align="center" class="skill-item">
                  <v-col cols="auto">
                    <v-icon class="skill-icon">mdi-language-javascript</v-icon>
                  </v-col>
                  <v-col>
                    <v-progress-linear
                      :value="90"
                      height="15"
                      color="purple"
                      class="skill-bar"
                      striped
                    ></v-progress-linear>
                    <span class="skill-label">JavaScript (90%)</span>
                  </v-col>
                </v-row>
              </v-col>
  
              <!-- Skill 2: Vue.js -->
              <v-col cols="12" md="6">
                <v-row align="center" class="skill-item">
                  <v-col cols="auto">
                    <v-icon class="skill-icon">mdi-vuejs</v-icon>
                  </v-col>
                  <v-col>
                    <v-progress-linear
                      :value="85"
                      height="15"
                      color="purple"
                      class="skill-bar"
                      striped
                    ></v-progress-linear>
                    <span class="skill-label">Vue.js (85%)</span>
                  </v-col>
                </v-row>
              </v-col>
  
              <!-- Skill 3: Node.js -->
              <v-col cols="12" md="6">
                <v-row align="center" class="skill-item">
                  <v-col cols="auto">
                    <v-icon class="skill-icon">mdi-nodejs</v-icon>
                  </v-col>
                  <v-col>
                    <v-progress-linear
                      :value="80"
                      height="15"
                      color="purple"
                      class="skill-bar"
                      striped
                    ></v-progress-linear>
                    <span class="skill-label">Node.js (80%)</span>
                  </v-col>
                </v-row>
              </v-col>
  
              <!-- Skill 4: HTML5 -->
              <v-col cols="12" md="6">
                <v-row align="center" class="skill-item">
                  <v-col cols="auto">
                    <v-icon class="skill-icon">mdi-language-html5</v-icon>
                  </v-col>
                  <v-col>
                    <v-progress-linear
                      :value="95"
                      height="15"
                      color="purple"
                      class="skill-bar"
                      striped
                    ></v-progress-linear>
                    <span class="skill-label">HTML5 (95%)</span>
                  </v-col>
                </v-row>
              </v-col>
  
              <!-- Skill 5: CSS3 -->
              <v-col cols="12" md="6">
                <v-row align="center" class="skill-item">
                  <v-col cols="auto">
                    <v-icon class="skill-icon">mdi-language-css3</v-icon>
                  </v-col>
                  <v-col>
                    <v-progress-linear
                      :value="90"
                      height="15"
                      color="purple"
                      class="skill-bar"
                      striped
                    ></v-progress-linear>
                    <span class="skill-label">CSS3 (90%)</span>
                  </v-col>
                </v-row>
              </v-col>
  
              <!-- Skill 6: MongoDB -->
              <v-col cols="12" md="6">
                <v-row align="center" class="skill-item">
                  <v-col cols="auto">
                    <v-icon class="skill-icon">mdi-database</v-icon>
                  </v-col>
                  <v-col>
                    <v-progress-linear
                      :value="75"
                      height="15"
                      color="purple"
                      class="skill-bar"
                      striped
                    ></v-progress-linear>
                    <span class="skill-label">MongoDB (75%)</span>
                  </v-col>
                </v-row>
              </v-col>
  
              <!-- Skill 7: PostgreSQL -->
              <v-col cols="12" md="6">
                <v-row align="center" class="skill-item">
                  <v-col cols="auto">
                    <v-icon class="skill-icon">mdi-database</v-icon>
                  </v-col>
                  <v-col>
                    <v-progress-linear
                      :value="70"
                      height="15"
                      color="purple"
                      class="skill-bar"
                      striped
                    ></v-progress-linear>
                    <span class="skill-label">PostgreSQL (70%)</span>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </div>
  
          <!-- Certifications Section (As per previous implementation) -->
  
          <!-- Projects Section (As per previous implementation) -->
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: "Resume",
    data() {
      return {
        // Previous data (certifications, projects, etc.)
      };
    },
  };
  </script>
  
  <style scoped>
  /* Scoped CSS for Skills Section */
  .skill-item {
    margin-bottom: 20px;
  }
  
  .skill-icon {
    font-size: 2rem;
    color: #b19cd9;
  }
  
  .skill-bar {
    margin-top: 5px;
    background-color: #21072c;
  }
  
  .skill-label {
    color: #e0e0e0;
    font-size: 1.1rem;
    margin-left: 10px;
  }
  
  .category-title {
    font-size: 1.8rem;
    color: #b19cd9;
    margin: 40px 0 20px;
    text-align: center;
  }
  </style>
  