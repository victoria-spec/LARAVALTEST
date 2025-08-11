# Product Pulse Application Documentation

## Overview

The **Product Pulse** application is developed using **Laravel** and **React**. It leverages modern technologies to create a responsive user interface while ensuring robust security measures. The application is designed to allow users to select products and submit feedback efficiently.

## Technology Stack

- **Frontend**: 
  - React 19
  - Tailwind 4
  - shadcn/ui
  - Inertia 2

- **Backend**: 
  - Laravel
  - Sanctum for authentication

- **Database**: 
  - MariaDB

## Security Features

The application has been developed with security as a primary concern. Key security features include:

- **Input Validation**: All user inputs are validated to prevent malicious data entry.
- **Sensitive Information Handling**: Sensitive information, such as usernames, is not exposed to the client side; it is retrieved securely from the backend.
- **Authorization**: Only authorized users can view and submit feedback, protecting sensitive data and preventing system abuse.

## User Interface Design

The application assumes multiple products are available for users to select from when submitting feedback. To enhance usability, the following design patterns have been implemented:

- **Side Navigation**: A side navigation pattern allows users to select relevant products easily.
- **Main Screen for Feedback**: The main screen displays a list of feedback related to the selected product.
- **Focused Feedback Review**: When a user selects feedback, all other elements are hidden, allowing them to concentrate on reviewing feedback and comments without distractions.
- **Soring Feedbacks**:
- **Categories** Information about categories is stored in the database to ensure extensibility

## User Workflow

1. **Product Selection**: Users select a relevant product from the side navigation.
2. **Feedback Viewing/Submitting**: After selecting a product, users can view existing feedback or submit new feedback.

## Development Notes

Due to time constraints, the following aspects were not completed:
- Product support --> only demo for concept Product 1 is working 
- Comments support  --> model and routing developed
- Detial feedback view -->  
- Refactoring of several views ---> In process of refactoring product view into components

## Assumptions

1. The development machine can run a "Hello World" Laravel and React application.
2. MySQL or MariaDB is deployed and configured.

## Installation Procedure

To install the Product Pulse application, follow these steps:

1. Unzip the application.
2. Navigate to the application directory:
   ```bash
   cd product-pulse''' 
   
3. Modify the .env file to include information about the database connection.
4. Create an empty database.
5. Grant only the required permissions for schema manipulation (create, delete, modify tables) and read/write access from all tables in the Product Pulse database. No additional permissions are needed for the user.
6. Run the following command to deploy dependencies:
   ```bash
   composer install''' 

7. Run the following command to migrate the database:
bash

php artisan migrate:fresh

Seed the database with initial data:

bash

php artisan db:seed

8. Install frontend dependencies and build the application:

bash

npm install && npm run build

9. Run the development server:

bash

    composer run dev

## Conclusion

The Product Pulse application is designed to provide a secure and user-friendly platform for feedback submission. With a focus on responsive design and security, it aims to enhance user experience while protecting sensitive data.




