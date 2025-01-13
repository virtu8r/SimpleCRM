<template>
      <ul>
        <li v-for="(contact, index) in contacts" :key="index">
          {{ contact.name }} - {{ contact.email }} - {{ contact.phone }}
          <button @click="$emit('delete-contact', index)">Delete</button>
        </li>
      </ul>
    </template>

    <script>
    export default {
      props: ['contacts']
    };
    </script>

    <style scoped>
    ul {
      list-style: none;
      padding: 0;
    }
    li {
      margin-bottom: 10px;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    </style>
