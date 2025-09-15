# Code-Review

A full-stack web application for automated code review and feedback using AI (Google Gemini).  
This project consists of a Node.js/Express backend and a React/Vite frontend.

---

## Features

- Submit code or prompts for AI-powered review.
- Uses Google Gemini API for generative feedback.
- RESTful API backend.
- Modern React frontend with Vite.
- CORS enabled for frontend-backend communication.

---

## Tech Stack

- **Backend:** Node.js, Express
- **Frontend:** React, Vite
- **AI Service:** Google Gemini API

---

## Project Structure

```
code-review/
│
├── Backend/
│   ├── src/
│   │   ├── controllers/
│   │   │   └── ai.controller.js
│   │   ├── routes/
│   │   │   └── ai.route.js
│   │   ├── services/
│   │   │   └── ai.service.js
│   │   └── app.js
│   ├── server.js
│   ├── package.json
│   └── .env
│
├── Frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── ...other components
│   ├── package.json
│   ├── vite.config.js
│   └── .env
│
└── README.md
```

---

## Setup Instructions

### 1. Clone the repository

```sh
git clone https://github.com/<your-username>/code-review.git
cd code-review
```

### 2. Backend Setup

```sh
cd Backend
npm install
```

- Create a `.env` file in `Backend` with your Google Gemini API key:
  ```
  GOOGLE_GEMINI_KEY=your_google_gemini_api_key
  PORT=3000
  ```

- Start the backend server:
  ```
  npx nodemon server.js
  ```
  or
  ```
  node server.js
  ```

### 3. Frontend Setup

```sh
cd ../Frontend
npm install
```

- Start the frontend development server:
  ```
  npm run dev
  ```

---

## Environment Variables

**Backend/.env**
```
GOOGLE_GEMINI_KEY=your_google_gemini_api_key
PORT=3000
```

**Frontend/.env**
```
# Add any frontend environment variables here if needed
```

---

## Usage

1. Start both backend and frontend servers.
2. Open your browser and go to `http://localhost:5173` (default Vite port).
3. Use the UI to submit code or prompts for review.

---

## API Endpoints

### POST `/ai/get-review`

- **Description:** Get AI-generated review for submitted code or prompt.
- **Request Body:**
  ```json
  {
    "prompt": "your code or question here"
  }
  ```
- **Response:**
  ```json
  {
    "response": "AI-generated feedback"
  }
  ```

---

## Contributing

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

---

## Credits

- [Google Gemini API](https://ai.google.dev/)
- [Vite](https://vitejs.dev/)
- [React](https://react.dev/)
- [Express](https://expressjs.com/)

