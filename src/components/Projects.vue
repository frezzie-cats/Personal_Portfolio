<template>
  <div class="resume-category">
    <h3 class="category-title">Projects</h3>
    <v-row>
      <v-col
        v-for="(project, index) in visibleProjects"
        :key="index"
        cols="12"
        md="6"
      >
        <v-card class="project-card" outlined @click="openImage(project.image)">
          <v-img
            :src="project.image"
            :alt="project.title"
            class="project-image"
            contain
          ></v-img>
          <v-card-title>{{ project.title }}</v-card-title>
          <v-card-subtitle>{{ project.description }}</v-card-subtitle>
          <v-card-actions>
            <v-btn
              v-if="project.link"
              :href="project.link"
              target="_blank"
              color="purple"
              outlined
            >
              View Project
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>

    <!-- Show More/Show Less Button -->
    <v-row justify="center">
      <v-col cols="12" md="4">
        <v-btn @click="toggleProjects" color="purple" block>
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
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          title: 'To-Do List App',
          description: 'A to-do list app built with Vue.js and Vuetify.',
          image: 'src/assets/code.jpg',
          link: 'https://example.com/to-do-list',
        },
        {
          title: 'Interactive Learning Platform',
          description: 'A platform for interactive learning with quizzes and videos.',
          image: 'src/assets/code.jpg',
          link: 'https://example.com/learning-platform',
        },
      ],
      visibleProjects: [],
      projectsToShow: 4,
      showMore: true,
      imageDialog: false, // Controls the dialog visibility
      selectedImage: '', // Stores the selected image URL
    };
  },
  mounted() {
    this.visibleProjects = this.projects.slice(0, this.projectsToShow);
  },
  methods: {
    toggleProjects() {
      if (this.showMore) {
        this.visibleProjects = this.projects;
      } else {
        this.visibleProjects = this.projects.slice(0, this.projectsToShow);
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

.project-card {
  background-color: #292929;
  color: #e0e0e0;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* Hover Effect */
.project-card:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
}

.project-image {
  width: 100%;
  height: 150px;
  object-fit: contain;
  margin-top: 10px;
}

.v-btn {
  color: #b19cd9;
}
</style>
