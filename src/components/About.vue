<template>
  <v-container class="about-section" fluid>
    <v-row align="center" justify="center">
      <!-- About Title Centered Above Both Columns -->
      <v-col cols="12" class="about-title-container">
        <h2 class="about-title">About Me</h2>
      </v-col>

      <!-- Left Column: Profile Image Centered in Column -->
      <v-col cols="12" md="4" class="text-center">
        <v-img
          src="../assets/profile.jpg"
          alt="Profile Picture"
          class="profile-image"
          contain
          max-width="250"
        ></v-img>
      </v-col>

      <!-- Right Column: Text Content -->
      <v-col cols="12" md="8" class="text-center text-md-left">
        <p class="about-description">
          I am a passionate Fullstack Developer with a solid foundation in web development technologies. I specialize in creating dynamic and responsive web applications using Vue.js, Node.js, and various modern frameworks. With a focus on user-centric design and performance optimization, I strive to build scalable solutions that cater to both user needs and business objectives.
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'About',
};
</script>

<style scoped>
.about-section {
  background-color: #090211;
  color: #f1f1f1;
  padding: 60px 20px;
  border-radius: 12px;
}

.about-title-container {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

.about-title {
  color: #b19cd9;
  font-size: 2.5rem;
  font-weight: bold;
  text-align: center;
  margin-bottom: 0;
  position: relative;
}

.about-title::after {
  content: '';
  position: absolute;
  bottom: -5px; 
  left: 0;
  width: 100%; 
  height: 4px; 
  background-color: #8e44ad; 
  border-radius: 1px; 
}

.profile-image {
  border-radius: 50%;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
  margin: 0 auto 20px auto; /* Center the profile image */
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  transform: scale(1.05); /* Slightly increase size on hover */
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.7); /* Darker shadow on hover */
}

.about-description {
  font-size: 1.2rem;
  max-width: 700px;
  margin: 0 auto;
  line-height: 1.6;
  color: #d3d3d3;
}

.download-button {
  background-color: #8e44ad;
  color: white;
  font-weight: bold;
  padding: 12px 30px;
}

.download-button:hover {
  background-color: #732d91;
}
</style>
