<template>
  <v-container
    class="hero-section"
    fill-height
    fluid
  >
    <v-row
      align="center"
      justify="center"
      class="text-center"
    >
      <v-col cols="12" md="8">
        <h1 class="display-2 font-weight-bold title">
          Hi, I'm <span class="highlight">Frezzie Marie C. Catamora</span>
        </h1>
        <h2 class="subtitle-1 font-weight-light subtitle">
          Fullstack Developer
        </h2>
        <p class="mt-4 description">
          Building seamless and dynamic web applications from front to back
        </p>
        
        <!-- Download CV Button -->
        <v-btn class="cta-button mt-4 mr-4">
          Download CV
          <v-icon right>mdi-download</v-icon>
        </v-btn>

        <!-- Hire Me Button -->
        <v-btn class="cta-button mt-4" href="#contact">
          Hire Me
          <v-icon right>mdi-briefcase</v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<style scoped>
.hero-section {
  background-image: url('src/assets/hero-background.jpg'); /* Background image URL */
  background-size: cover;
  background-position: center;
  color: white;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  padding: 0;
}

.hero-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5); /* Semi-transparent overlay */
}

.title {
  font-size: 3.5rem; /* Larger font size */
  line-height: 1.2;
  margin-bottom: 10px;
  color: white;
  z-index: 1;
  animation: fadeIn 1s ease-out forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.highlight {
  color: #a17fdf; /* Light purple accent */
  font-weight: 600;
  text-shadow: 1px 1px 10px rgba(177, 156, 217, 0.6);
}

.subtitle {
  color: #c4bcdc;
  font-size: 1.8rem;
  margin-bottom: 20px;
  z-index: 1;
  animation: fadeIn 1s ease-out 0.5s forwards;
}

.description {
  color: #d3d3d3;
  font-size: 1.2rem;
  max-width: 600px;
  margin: 0 auto;
  padding: 0 20px;
  z-index: 1;
  animation: fadeIn 1s ease-out 1s forwards;
}

.cta-button {
  background-color: #8e44ad;
  color: white;
  font-weight: bold;
  transition: transform 0.3s ease, background-color 0.3s ease;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.4);
  z-index: 1;
  padding: 12px 24px;
  font-size: 1.0rem;
}

.cta-button:hover {
  background-color: #732d91;
  transform: translateY(-3px) scale(1.05); /* Hover effect */
}

.cta-button .v-icon {
  transition: transform 0.3s ease;
}

.cta-button:hover .v-icon {
  transform: translateX(5px); /* Icon movement */
}
</style>
