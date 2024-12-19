
# Zerodha Clone

## Overview

The Zerodha Clone project replicates the core functionalities of the Zerodha platform, providing users with a seamless interface to manage their portfolios, track real-time stock market data, and perform investment operations. This project demonstrates full-stack development skills, including backend and frontend integration, database management, and deployment processes.

---

## Features

- **User Authentication**:
  - Secure login using OAuth.
  - Session management for authenticated users.

- **Portfolio Management**:
  - Add, update, and delete investments.
  - View detailed portfolio statistics and performance.

- **Real-Time Market Data**:
  - Fetch real-time stock prices using third-party APIs.
  - Display market trends and user-specific stock information.

- **Interactive Dashboard**:
  - Visualize data through charts and graphs.
  - Comprehensive analytics for user investments.

---

## Technology Stack

### **Backend**
- **Node.js** with **Express.js** framework.
- RESTful API design.
- **Database**: MongoDB for data persistence.

### **Frontend**
- **React.js** for building user interfaces.
- **Redux** for state management.
- Responsive UI design using **Bootstrap**.

### **Hosting and Deployment**
- Backend hosted on **AWS EC2**.
- Frontend deployed via **Netlify**.
- CI/CD pipelines managed with **GitHub Actions**.

---

## Installation

### Prerequisites
- **Node.js** and **npm** installed.
- MongoDB database setup.
- API keys for third-party stock market data.

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/apna-college/Zerodha.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Zerodha
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Set up environment variables:
   - Create a `.env` file.
   - Add the following keys:
     ```env
     DATABASE_URL=<Your MongoDB Connection String>
     API_KEY=<Your Third-Party API Key>
     ```
5. Run the application:
   ```bash
   npm start
   ```
6. Open the application at `http://localhost:3000`.

---

## Project Structure

```plaintext
Zerodha/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── server.js
│
├── frontend/
│   ├── public/
│   ├── src/
│       ├── components/
│       ├── pages/
│       ├── redux/
│       ├── App.js
│
├── .env
├── package.json
└── README.md
```

---

## API Documentation

### User Authentication
- **POST** `/auth/login`
  - **Request Body**:
    ```json
    {
      "email": "user@example.com",
      "password": "password123"
    }
    ```
  - **Response**:
    ```json
    {
      "token": "JWT Token",
      "user": {
        "id": "12345",
        "name": "John Doe"
      }
    }
    ```

### Portfolio Management
- **GET** `/portfolio`
  - Fetches the user’s current portfolio.

- **POST** `/portfolio`
  - Adds a new investment.
  - **Request Body**:
    ```json
    {
      "symbol": "AAPL",
      "quantity": 10,
      "price": 150
    }
    ```

### Real-Time Market Data
- **GET** `/market-data`
  - Returns stock data for the requested symbols.

---
