# Frontend Integration with JWT APIs (Session-Based UI)
🧪 **Based on Experiment 6**

This project demonstrates a React-based frontend that consumes JWT APIs from a Node.js backend. It features session-based authentication where the JWT is stored in the browser's `sessionStorage` to restrict access to protected pages.

## 📘 Project Explanation
* **React frontend connects to backend APIs:** Handles authentication by calling the backend to verify credentials.
* **JWT stored in sessionStorage:** Upon successful login, the received JWT is securely stored in `sessionStorage`.
* **Protected routes accessed using token:** The Dashboard route is protected. It checks for a valid session token, and adds the token as a `Bearer` header for authorized API requests.
* **Logout clears session:** Clicking logout clears the session storage token and redirects the user safely back to the login page.

---

## 📸 Screenshots

### 1. Login from frontend (React UI)
User enters their username and password to log in.
![Login UI](screenshots/Screenshot%202026-04-15%20154322.png)

### 2. Token stored in sessionStorage (DevTools)
After logging in, the JWT token is successfully stored in the browser's Developer Tools under Session Storage.
![Token in Session Storage](screenshots/Screenshot%202026-04-15%20155804.png)

### 3. Access Protected API
The protected dashboard successfully fetches authorized data from the backend using the Bearer token.
![Access Protected API](screenshots/Screenshot%202026-04-15%20154401.png)

### 4. Unauthorized Access (Redirect to Login)
Attempting to directly navigate to the Dashboard (e.g., in Incognito without a token) strictly denies entry and forces the user out.
![Unauthorized Access](screenshots/Screenshot%202026-04-15%20154841.png)

### 5. Logout Functionality
Triggering the Logout function removes the local token entirely and returns the user to the login screen.
![Logout Functionality](screenshots/Screenshot%202026-04-15%20155625.png)

---

## ⚙️ Installation & Running the Project

### Frontend Setup
1. Open terminal in the `frontend` folder:
   ```bash
   cd frontend
   npm install
   npm start
   ```
2. The application will run on `http://localhost:3000`.

### Backend Setup (from Experiment 6)
Ensure that your backend server is running on `http://localhost:5000` so the React application can send authentication and data requests!