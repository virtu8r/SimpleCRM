# Simple-CRM

**A basic Customer Relationship Management (CRM) application built with Vue.js.**

Simple-CRM provides a straightforward interface for managing contacts. It features a form for adding new contacts and a list to display them.

## Features

*   **Contact management:** Add, view, and delete contact information.
*   **Vue.js components:** Modular design with reusable components (`ContactForm`, `ContactList`).
*   **Data binding:** Reactive updates between the form and contact list.

## Project setup
npm install


### Compiles and hot-reloads for development
npm run serve


### Compiles and minifies for production
npm run build


### Lints and fixes files
npm run lint 1    
 1. 
agrodk.cz
agrodk.cz


### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


## Component Structure

*   **ContactForm.vue:**
    *   Captures contact details (name, email, phone) through a form.
    *   Emits an `add-contact` event with the new contact data when the form is submitted.

*   **ContactList.vue:**
    *   Displays a list of contacts.
    *   Receives `contacts` (array) as a prop.
    *   Emits a `delete-contact` event with the index of the contact to be deleted.

## Future Enhancements

*   **Data persistence:** Store contact data using local storage or a backend API.
*   **Search and filtering:** Allow users to search and filter contacts.
*   **Contact details:** Display more comprehensive contact information (e.g., address, notes).
*   **Sorting:** Implement sorting of contacts by different criteria.
*   **UI improvements:** Enhance the visual design and user experience.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

[MIT](https://choosealicense.com/licenses/mit/)
