<template>
  <div class="resume-category">
    <h3 class="category-title">Work Experience</h3>
    <v-container fluid>
      <v-row justify="center">
        <v-col cols="12" md="8" lg="6">
          <v-timeline dense align="center" justify="center">
            <v-timeline-item
              v-for="(job, index) in workExperience"
              :key="index"
              :color="'purple'"
            >
              <template v-slot:opposite>
                <strong class="company">{{ job.company }}</strong>
                <br />
                <small>{{ job.dates }}</small>
              </template>
              <v-card flat>
                <v-card-title class="job-title">{{ job.position }}</v-card-title>
                <v-card-subtitle class="location">{{ job.location }}</v-card-subtitle>
                <v-card-text class="description">{{ job.description }}</v-card-text>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'WorkExperience',
  data() {
    return {
      workExperience: [
          {
            position: 'Fullstack Developer',
            company: 'AZ Tech Company',
            location: 'Cebu City, Philippines',
            dates: '2023 - Present',
            description: 'Developed and maintained web applications using Vue.js and Node.js.',
          },
          {
            position: 'Web Developer Intern',
            company: 'Babel Group',
            location: 'City of Manila, Philippines',
            dates: '2022 - 2023',
            description: 'Assisted in building front-end components and testing software solutions.',
          },
        ],
    };
  },
};
</script>

<style scoped>
.resume-category {
  margin-bottom: 40px;
  padding: 0 10px;
}

.category-title {
  font-size: 1.8rem;
  color: #b19cd9;
  margin-bottom: 20px;
  text-align: center;
}

.company {
  font-size: 1rem;
  color: #b19cd9;
}

.job-title {
  color: #b19cd9;
  font-weight: bold;
}

.location {
  color: #c4bcdc;
  font-size: 0.9rem;
}

.description {
  color: #d3d3d3;
  font-size: 0.85rem;
}

/* Responsive Design */
@media (max-width: 600px) {
  .category-title {
    font-size: 1.5rem;
  }
  .job-title {
    font-size: 1rem;
  }
  .company {
    font-size: 0.9rem;
  }
  .location, .description {
    font-size: 0.8rem;
  }
  .resume-category {
    margin-bottom: 20px;
    padding: 0;
  }
}
</style>
