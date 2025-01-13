<template>
      <div class="container">
        <h1>Simple CRM</h1>
        <ContactForm @add-contact="addContact" />
        <ContactList :contacts="contacts" @delete-contact="deleteContact" />
      </div>
    </template>

    <script>
    import ContactForm from './components/ContactForm.vue';
    import ContactList from './components/ContactList.vue';

    export default {
      name: 'App',
      components: {
        ContactForm,
        ContactList
      },
      data() {
        return {
          contacts: JSON.parse(localStorage.getItem('contacts')) || []
        };
      },
      methods: {
        addContact(contact) {
          this.contacts.push(contact);
          localStorage.setItem('contacts', JSON.stringify(this.contacts));
        },
        deleteContact(index) {
          this.contacts.splice(index, 1);
          localStorage.setItem('contacts', JSON.stringify(this.contacts));
        }
      }
    };
    </script>

    <style>
    .container {
      font-family: sans-serif;
      max-width: 600px;
      margin: 0 auto;
      padding: 20px;
    }
    </style>
