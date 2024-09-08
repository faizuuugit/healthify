# Healthify - Doctor Appointment Booking System

## Introduction

**Healthify** is a full-stack web application designed to simplify and streamline the process of booking appointments with healthcare providers. It provides a user-friendly interface for patients to register, search for doctors, and schedule appointments, while offering healthcare professionals an efficient platform to manage their availability and appointments.

## Features

- **User Registration & Login**: Secure user authentication using JSON Web Tokens (JWT) for both patients and doctors.
- **Doctor Profile Management**: Doctors can manage their profiles, set their availability, and view appointments.
- **Appointment Scheduling**: Patients can view doctors' availability and book appointments in real time.
- **Notifications**: Users receive notifications for new appointments, status updates, and cancellations.
- **Admin Dashboard**: Administrators can manage doctors and users, approve/reject doctor applications, and monitor system activities.
- **Responsive Design**: The application is fully responsive and can be accessed across various devices.

## Technology Stack

- **Frontend**: 
  - **React.js**: For building the dynamic user interface.
  - **Ant Design (AntD)**: UI component library for designing clean and professional interfaces.
  - **CSS**: For custom styling.
  
- **Backend**:
  - **Node.js**: For handling server-side logic.
  - **Express.js**: For building the RESTful API and middleware.
  - **MongoDB**: A NoSQL database for storing user, doctor, and appointment data.
  - **Mongoose**: For object data modeling (ODM) to interact with MongoDB.
  - **JWT (JSON Web Token)**: For secure authentication.

## Project Structure

```bash
Healthify/
├── client/                 # Frontend code (React.js)
│   ├── src/
│   │   ├── components/     # React components (Navbar, Footer, etc.)
│   │   ├── pages/          # Pages like Home, Login, Register, Appointments
│   │   ├── styles/         # CSS files for styling
│   │   └── App.js          # Main React app file
├── server/                 # Backend code (Node.js and Express.js)
│   ├── controllers/        # Logic for handling user, doctor, and appointment actions
│   ├── models/             # MongoDB models (User, Doctor, Appointment)
│   ├── routes/             # API routes for handling requests (userRoutes, doctorRoutes, etc.)
│   ├── config/             # Configuration files (database connection, environment variables)
│   └── server.js           # Entry point for starting the backend server
├── .env                    # Environment variables for database and API keys
├── README.md               # Project documentation
└── package.json            # Dependencies and scripts
```

## Installation and Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/healthify.git
   cd healthify
   ```

2. **Install Backend Dependencies**:
   Navigate to the `server` folder and install dependencies:
   ```bash
   cd server
   npm install
   ```

3. **Install Frontend Dependencies**:
   Navigate to the `client` folder and install dependencies:
   ```bash
   cd client
   npm install
   ```

4. **Set up Environment Variables**:
   Create a `.env` file in the `server` folder and add the following:
   ```bash
   PORT=8080
   MONGO_URI=<your-mongodb-connection-string>
   JWT_SECRET=<your-jwt-secret>
   ```

5. **Run the Application**:
   - Start the backend server:
     ```bash
     cd server
     npm run dev
     ```
   - Start the frontend application:
     ```bash
     cd client
     npm start
     ```

   The frontend will run on `http://localhost:3000` and the backend API will be available on `http://localhost:8080`.

## Key Functionalities

### Users (Patients)
- **Registration & Login**: Users can create accounts and log in securely using JWT-based authentication.
- **View Doctors**: Browse a list of available doctors, view their profiles, and book appointments.
- **Appointment Management**: View upcoming appointments and cancel or reschedule as necessary.
  
### Doctors
- **Profile Management**: Doctors can update their profiles, set their consultation fees, and manage availability.
- **View Appointments**: Doctors can view their scheduled appointments and update the status.
  
### Admin
- **User and Doctor Management**: Admins can view and manage registered users and doctors.
- **Approve/Reject Doctors**: Admins have the ability to approve or reject doctor applications.

## API Endpoints

- **User Routes**:
  - `POST /login`: Login a user.
  - `POST /register`: Register a new user.
  - `GET /getAllDoctors`: Retrieve a list of all doctors.
  - `POST /book-appointment`: Book an appointment.
  
- **Doctor Routes**:
  - `POST /apply-doctor`: Apply to become a doctor.
  - `POST /updateProfile`: Update doctor profile information.
  - `GET /doctor-appointments`: Retrieve all appointments for the doctor.

- **Admin Routes**:
  - `GET /getAllUsers`: Get all registered users.
  - `GET /getAllDoctors`: Get all registered doctors.
  - `POST /changeAccountStatus`: Approve or reject doctor applications.

## Future Enhancements

- **Payment Integration**: Add payment gateway for appointment fees.
- **Telemedicine**: Add support for virtual consultations via video conferencing.
- **Multi-language Support**: Allow users to select their preferred language for the interface.

---

This project provides a robust solution for managing doctor appointments and aims to improve the efficiency of healthcare services.
