<template>
  <v-container class="contact-section" fluid>
    <v-row justify="center">
      <v-col cols="12" md="8">
        <h2 class="section-title">Contact Me</h2>

        <!-- Contact Form -->
        <v-form v-model="valid" ref="form" @submit.prevent="submitForm">
          <v-row>
            <!-- Name Input -->
            <v-col cols="12" md="6">
              <v-text-field
                v-model="form.name"
                label="Full Name"
                required
                :rules="[rules.required]"
                outlined
                dense
              ></v-text-field>
            </v-col>

            <!-- Email Input -->
            <v-col cols="12" md="6">
              <v-text-field
                v-model="form.email"
                label="Email Address"
                required
                :rules="[rules.required, rules.email]"
                outlined
                dense
              ></v-text-field>
            </v-col>
          </v-row>

          <v-row>
            <!-- Message Input -->
            <v-col cols="12">
              <v-textarea
                v-model="form.message"
                label="Your Message"
                required
                :rules="[rules.required]"
                outlined
                dense
                rows="5"
              ></v-textarea>
            </v-col>
          </v-row>

          <v-row justify="center">
            <v-col cols="12" md="4">
              <v-btn
                :disabled="!valid"
                type="submit"
                color="purple"
                block
                class="submit-btn"
              >
                Send Message
              </v-btn>
            </v-col>
          </v-row>
        </v-form>

        <!-- Contact Info -->
        <v-row class="mt-5" align="center">
          <v-col cols="12" md="4" class="d-flex align-center">
            <v-icon large class="mr-3">mdi-phone</v-icon>
            <p class="contact-info">091234567891</p>
          </v-col>
          <v-col cols="12" md="4" class="d-flex align-center">
            <v-icon large class="mr-3">mdi-email</v-icon>
            <p class="contact-info">frezziecatamora@gmail.com</p>
          </v-col>
          <v-col cols="12" md="4" class="d-flex align-center">
            <v-icon large class="mr-3">mdi-map-marker</v-icon>
            <p class="contact-info">Butuan City, Philippines</p>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      valid: false,
      form: {
        name: '',
        email: '',
        message: '',
      },
      rules: {
        required: (value) => !!value || 'This field is required',
        email: (value) =>
          /.+@.+\..+/.test(value) || 'Please enter a valid email address',
      },
    };
  },
  methods: {
    submitForm() {
      this.$vuetify.toast.success('Message sent successfully!');
      // Logic for form submission goes here (e.g., send data to an API)
    },
  },
};
</script>

<style scoped>
.contact-section {
  background-color: #090211;
  color: #e0e0e0;
  padding: 60px 0;
}

.section-title {
  font-size: 2rem;
  text-align: center;
  color: #b19cd9;
  margin-bottom: 30px;
}

.v-text-field,
.v-textarea {
  background-color: #292929;
  color: #e0e0e0;
  border-radius: 8px; /* Rounded corners */
}

.v-text-field .v-input__control,
.v-textarea .v-input__control {
  height: 45px; /* Smaller input height */
}

.submit-btn {
  font-size: 1.1rem;
  padding: 15px 30px; /* Increased padding for a larger click area */
  background: linear-gradient(145deg, #6a4fa7, #9b77d6); /* Gradient background */
  border: none;
  color: white;
  border-radius: 8px; /* Rounded corners for smooth edges */
  box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3); /* Subtle shadow for depth */
  transition: all 0.3s ease; /* Smooth transition for hover effects */
}

.submit-btn:hover {
  background: linear-gradient(145deg, #9b77d6, #6a4fa7); /* Reversed gradient on hover */
  transform: scale(1.05); /* Slightly enlarge button on hover */
  box-shadow: 2px 2px 15px rgba(0, 0, 0, 0.4); /* Increase shadow on hover */
}

.submit-btn:disabled {
  background: #6a4fa7; /* Disabled button background */
  cursor: not-allowed; /* Change cursor to indicate disabled state */
  box-shadow: none; /* Remove shadow for disabled state */
}

.contact-info {
  color: #e0e0e0;
  font-size: 1.1rem;
  text-align: left; /* Align the text next to the icon */
}

.v-icon {
  color: #b19cd9;
}

.d-flex {
  display: flex;
}

.align-center {
  align-items: center;
}

.mr-3 {
  margin-right: 10px; /* Space between icon and text */
}
</style>
