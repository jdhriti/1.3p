<script setup>
import { ref } from "vue";

// Define a reactive object for form data
const fdata = ref({
  name: '',
  email: '',
  password: '',
  confirmPassword: '',
});

// Function to handle form submission
const submitForm = () => {
  // Access the form data from the fdata ref
  const { name, email, password, confirmPassword } = fdata.value;

  // Add your form validation and submission logic here
  if (!name || !email || !password || !confirmPassword) {
    // Example: Handle validation errors
    alert('Please fill in all fields.');
  } else if (password !== confirmPassword) {
    // Example: Handle password mismatch
    alert('Password and Confirm Password do not match.');
  } else {
    // Example: Submit the form data to the server or perform other actions
    alert('Registration successful!');
    fdata.name = '';
    fdata.email = '';
    fdata.password = '';
    fdata.confirmPassword = '';
    fdata.gender = '';
  }
};
</script>

<template>
    <div class="container">
      
      <form @submit.prevent="submitForm">
        <div>
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="fdata.name" />
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="fdata.email" />
        </div>
        <div>
          <label for="password">Password:</label>
          <input type="password" id="password" v-model="fdata.password" />
        </div>
        <div>
          <label for="confirmPassword">Confirm Password:</label>
          <input type="password" id="confirmPassword" v-model="fdata.confirmPassword" />
        </div>
        <div>
        <label for="gender">Gender:</label>
            <select id="gender" v-model="fdata.gender">
            <option value="">Select Gender</option>
            <option value="male">Male</option>
            <option value="female">Female</option>
            <option value="other">Other</option>
            </select>
        </div>
        <button type="submit">Register</button>
      </form>
    </div>
    
</template>

<style scoped>


.container {
    max-width: 80vw;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #f9f9f9;
    
  }

 
  input[type="text"],
  input[type="email"],
  input[type="password"],
  select {   
    margin-bottom: 15px;
  }


  select {
    background-color: #f8f4f4;
    
  }

  /* Form submit button */
  button[type="submit"] {
    display: block;
    width: 100%;
    padding: 10px;
    background-color:#a41e3b; 
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }

  button[type="submit"]:hover {
    background-color: #109447;
  }

</style>
