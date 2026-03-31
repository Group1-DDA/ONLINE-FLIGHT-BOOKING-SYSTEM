# ONLINE-FLIGHT-BOOKING-SYSTEM

Project Description

Is a comprehensive Online Travel Agent (OTA) platform designed to handle real-time flight searches, seat reservations, and ticket management. Built on a decoupled Client-Server architecture, the system ensures high performance, security, and strict data integrity.

A core focus of this project is its robust Inventory Management System. It features a 15-minute temporary seat lock during the checkout process and utilizes automated background jobs (Cron) to instantly release unpaid seats back to the inventory, strictly preventing overselling anomalies.

The platform provides dedicated interfaces and permissions for three distinct user roles:
Guests: Search for dynamic flight schedules and check booking status via PNR without needing an account.
Registered Users: Securely book flights, manage frequent passenger profiles for faster checkouts, and view personal transaction history.
Administrators: Access a visual analytics dashboard, perform full CRUD operations on flight inventory, enforce emergency ticket cancellations, and manage user role authorizations.

---

Technologies Used

This project is built on the MERN Stack (MongoDB, Express, React, Node.js).

#Frontend (Client Tier)
React.js: Single Page Application (SPA) framework for dynamic and responsive user interfaces.
Axios: Promise-based HTTP client utilizing Interceptors for automatic JWT injection.
Recharts: Composable charting library used to render interactive revenue and booking ratio charts in the Admin Dashboard.
React Router: Declarative routing for seamless navigation between pages.

#Backend (Application Tier)
Node.js & Express.js: Highly scalable RESTful API server handling complex business logic, dynamic search queries (Regex), and routing.
JSON Web Tokens (JWT) & bcryptjs: Implementing stateless authentication, secure password hashing, and role-based access control (Middleware).
node-cron: Background task scheduler responsible for the automated 15-minute ticket cancellation and inventory release mechanisms.
Nodemailer: Integrated email service for automated booking confirmations and payment reminders.

#Database (Data Tier)
MongoDB & Mongoose: NoSQL document database optimized for flexible handling, nested data structures (e.g., flight seats, passenger arrays). Utilizes atomic operations to ensure concurrency control during ticket booking.

---

Installation Guide

Follow these steps to set up and run the project locally. Please ensure you have Node.js and MongoDB (Local or Atlas) installed on your machine.
Environmental requirements :
Operating system: Windows.
Node.js: Version v24.12.0. 
MongoDB: Install MongoDB Compass (https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.6-signed.msi).
Step 1: Clone the source code 
Open Terminal and run the following command to download the project to your machine:

git clone https://github.com/Group1-DDA/ONLINE-FLIGHT-BOOKING-SYSTEM.git

cd ONLINE-FLIGHT-BOOKING-SYSTEM

Step 2: Configure and launch the Backend (Node.js/Express)
Move into the backend directory:

cd backend

Install the necessary libraries (Dependencies):

npm install

Set up environment variables: Create a file named . env in the root directory of the backend and declare 
PORT=3000
MONGO_URI=mongodb://localhost:27017/mydb  # Or your MongoDB Atlas link
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=gmail_app_password
Add sample data to the Server:

node seed.js

Launch Server:

node server.js 

Expected result: Terminal notification "Server đang chạy tại http://localhost:3000" và "Kết nối MongoDB thành công!".
Step 3: Configure and launch Frontend (React.js)
Open a new Terminal and navigate to the frontend directory:

cd frontend

Install the libraries (Dependencies):

npm install

Launch the React interface:

npm run dev

Expected result: The browser automatically opens or provides access to the Frontend at http://localhost:5173/.
