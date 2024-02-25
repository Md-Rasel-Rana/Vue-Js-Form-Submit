<template>
    <div class="container border">
      <h2>Bootstrap Form</h2>
      <form @submit.prevent="submitForm" >
        <div class="mb-3">
          <label for="firstName" class="form-label">First Name</label>
          <input type="text" class="form-control" id="firstName" v-model="formData.firstName" placeholder="Enter your first name">
        </div>
        <div class="mb-3">
          <label for="lastName" class="form-label">Last Name</label>
          <input type="text" class="form-control" id="lastName" v-model="formData.lastName" placeholder="Enter your last name">
        </div>
        <div class="mb-3">
          <label for="email" class="form-label">Email address</label>
          <input type="email" class="form-control" id="email" v-model="formData.email" placeholder="name@example.com">
        </div>
        <div class="mb-3">
          <label for="password" class="form-label">Password</label>
          <input type="password" class="form-control" id="password" v-model="formData.password" placeholder="Enter your password">
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
      <div v-if="formSubmitted">
        <h3>Form submitted successfully!</h3>
        <p>First Name: {{ formData.firstName }}</p>
        <p>Last Name: {{ formData.lastName }}</p>
        <p>Email: {{ formData.email }}</p>
        <p>Password: {{ formData.password }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'DemoWorld',
    data() {
      return {
        formData: {
          firstName: '',
          lastName: '',
          email: '',
          password: ''
        },
        formSubmitted: false
      };
    },
    methods: {
      submitForm() {
        // Submit form logic here
        this.formSubmitted = true;
        console.log(this.formData);
      }
    }
  };
  </script>
  
  <style scoped>
  /* Add any scoped CSS styles for the form */
  </style>
  