<template>
  <v-app>
    <!-- Navigation Bar -->
    <v-app-bar app dark color="black">
      <v-toolbar-title class="logo-text">My Portfolio</v-toolbar-title>
      <v-spacer />
      <!-- Navbar Links -->
      <v-btn text href="#about" class="nav-link">About</v-btn>
      <v-btn text href="#resume" class="nav-link">Resume</v-btn>
      <v-btn text href="#contact" class="nav-link">Contact</v-btn>
    </v-app-bar>

    <!-- Content Sections -->
    <v-main>
      <v-container fluid>
        <!-- Hero Section -->
        <Hero />

        <!-- About Section -->
        <About id="about" />

        <!-- Resume Section -->
        <v-container class="resume-section" fluid id="resume">
          <v-row justify="center">
            <v-col cols="12" md="10">
              <h2 class="section-title">Resume</h2>

              <!-- Education Section -->
              <Education />

              <!-- Work Experience Section -->
              <WorkExperience />

              <!-- Skills Section (without lines) -->
              <Skills class="no-lines" />

              <!-- Certifications Section -->
              <Certifications />

              <!-- Projects Section -->
              <Projects />
            </v-col>
          </v-row>
        </v-container>

        <!-- Contact Section -->
        <Contact id="contact" />

        <!-- Footer Section -->
        <Footer />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import Education from './components/Education.vue';
import WorkExperience from './components/WorkExperience.vue';
import Skills from './components/Skills.vue';
import Certifications from './components/Certifications.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';

export default {
  name: 'App',
  components: {
    Hero,
    About,
    Education,
    WorkExperience,
    Skills,
    Certifications,
    Projects,
    Contact,
  },
};
</script>

<style scoped>
html, body {
  scroll-behavior: smooth;
}

.logo-text {
  font-weight: bold;
  color: #b19cd9;
  font-size: 1.3rem;
}

.nav-link {
  color: #f1f1f1;
  font-size: 1.0rem;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #b19cd9;
}

.v-app-bar {
  box-shadow: none;
}

.resume-section {
  background-color: #090211;
  color: #e0e0e0;
  padding: 40px 20px;  /* Adjusted padding for alignment */
  position: relative;
}

.resume-section::before,
.resume-section::after {
  content: '';
  position: absolute;
  width: 100%;
  height: 4px;
  background-color: #8e44ad;
  border-radius: 1px;
}

.resume-section::before {
  top: 0;
  left: 0;  
}

.resume-section::after {
  bottom: 0;
  left: 0; 
}

.section-title {
  font-size: 2.5rem;
  text-align: center;
  color: #b19cd9;
  margin-bottom: 50px;
}

.no-lines {
  position: relative;
}

.no-lines::before,
.no-lines::after {
  content: none;
}
</style>
