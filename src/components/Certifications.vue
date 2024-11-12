<template>
  <div class="resume-category">
    <h3 class="category-title">Certifications</h3>
    <v-row>
      <v-col
        v-for="(cert, index) in visibleCertifications"
        :key="index"
        cols="12"
        md="6"
      >
        <v-card class="certification-card" outlined @click="openImage(cert.image)">
          <v-img
            :src="cert.image"
            :alt="cert.title"
            class="certification-image"
            contain
          ></v-img>
          <v-card-title>{{ cert.title }}</v-card-title>
          <v-card-subtitle>{{ cert.institution }}</v-card-subtitle>
          <v-card-text>{{ cert.date }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <!-- Show More/Show Less Button -->
    <v-row justify="center">
      <v-col cols="12" md="4">
        <v-btn @click="toggleCertifications" color="purple" block>
          {{ showMore ? 'Show More' : 'Show Less' }}
        </v-btn>
      </v-col>
    </v-row>

    <!-- Image Modal -->
    <v-dialog v-model="imageDialog" max-width="800px">
      <v-img :src="selectedImage" class="d-flex" contain></v-img>
    </v-dialog>
  </div>
</template>

<script>
export default {
  name: 'Certifications',
  data() {
    return {
      certifications: [
        {
          title: 'Introduction to HTML',
          institution: 'Sololearn',
          date: 'February 2024',
          image: 'src/assets/certifications/HTML - Intro.png',
        },
        {
          title: 'Introduction to CSS',
          institution: 'Sololearn',
          date: 'August 2024',
          image: 'src/assets/certifications/CSS - Intro.png',
        },
        {
          title: 'Introduction to Javascript',
          institution: 'Sololearn',
          date: 'September 2024',
          image: 'src/assets/certifications/JS - Intro.png',
        },
        {
          title: 'Introduction to SQL',
          institution: 'Sololearn',
          date: 'April 2024',
          image: 'src/assets/certifications/SQL - Intro.png',
        },
        {
          title: 'SQL intermediate',
          institution: 'Sololearn',
          date: 'April 2024',
          image: 'src/assets/certifications/SQL - Intermediate.png',
        },
        {
          title: 'Introduction to Java',
          institution: 'Sololearn',
          date: 'February 2024',
          image: 'src/assets/certifications/Java - Intro.png',
        },
        {
          title: 'Java Intermediate',
          institution: 'Sololearn',
          date: 'March 2024',
          image: 'src/assets/certifications/Java - Intermediate.png',
        },
      ],
      visibleCertifications: [],
      certificationsToShow: 4,
      showMore: true,
      imageDialog: false, // Controls the dialog visibility
      selectedImage: '', // Stores the selected image URL
    };
  },
  mounted() {
    this.visibleCertifications = this.certifications.slice(0, this.certificationsToShow);
  },
  methods: {
    toggleCertifications() {
      if (this.showMore) {
        this.visibleCertifications = this.certifications;
      } else {
        this.visibleCertifications = this.certifications.slice(0, this.certificationsToShow);
      }
      this.showMore = !this.showMore;
    },
    openImage(imageUrl) {
      this.selectedImage = imageUrl;
      this.imageDialog = true; // Open the modal with the selected image
    },
  },
};
</script>

<style scoped>
.category-title {
  font-size: 1.8rem;
  color: #b19cd9;
  margin: 40px 0 20px;
  text-align: center;
}

.certification-card {
  background-color: #292929;
  color: #e0e0e0;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* Hover Effect */
.certification-card:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
}

.certification-image {
  width: 100%;
  height: 150px;
  object-fit: contain;
  margin-top: 10px;
}

.v-btn {
  color: #b19cd9;
}
</style>
