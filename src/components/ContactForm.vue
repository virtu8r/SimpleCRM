<template>
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="name" required>
        </div>
        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div class="form-group">
          <label for="phone">Phone:</label>
          <input type="tel" id="phone" v-model="phone">
        </div>
        <button type="submit">Add Contact</button>
      </form>
    </template>

    <script>
    export default {
      data() {
        return {
          name: '',
          email: '',
          phone: ''
        };
      },
      methods: {
        submitForm() {
          const newContact = {
            name: this.name,
            email: this.email,
            phone: this.phone
          };
          this.$emit('add-contact', newContact);
          this.name = '';
          this.email = '';
          this.phone = '';
        }
      }
    };
    </script>

    <style scoped>
    .form-group {
      margin-bottom: 10px;
    }
    label {
      display: block;
      margin-bottom: 5px;
    }
    input, button {
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
      width: 100%;
    }
    button {
      background-color: #4CAF50;
      color: white;
      border: none;
      cursor: pointer;
    }
    </style>
