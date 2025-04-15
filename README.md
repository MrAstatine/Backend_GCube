# 🌐 G_Cube Club Backend

Welcome to the **official backend** of the [G_Cube Club](https://gcube-pes.vercel.app/), built using Node.js and Express. This system handles user registrations, query submissions, and multi-question answer submissions with a robust MongoDB integration and Cloudinary support for media storage.

---

## 📋 Table of Contents

- [Project Structure](#-project-structure)
- [Features](#-features)
- [Setup Instructions](#-setup-instructions)
- [API Endpoints](#-api-endpoints)
- [Technologies Used](#-technologies-used)
- [Code Style & Quality](#-code-style--quality)
- [Author](#-author)

---

## 📁 Project Structure

```
mrastatine-backend_gcube.git/
├── package.json
├── src/
│   ├── app.js           # App configuration and middleware setup
│   ├── index.js         # Entry point with MongoDB connection
│   ├── constants.js     # Constants like DB name
│   ├── controllers/     # Route logic
│   ├── db/              # MongoDB connection logic
│   ├── middlewares/     # Auth & file upload middleware
│   ├── models/          # Mongoose schemas
│   ├── routers/         # Express route handlers
│   └── utils/           # Utility classes & helpers
```

---

## 🚀 Features

- 🧑‍💻 **User Registration**: Handles user profile creation with validation.
- 💬 **Query Submission**: Collects questions or concerns via contact form.
- 📝 **Answer Registration**: Allows multi-question form submissions per user.
- ✅ **User Auth Middleware**: Retrieves user from request headers securely.
- ☁️ **Cloudinary Integration**: Image and file upload support.
- 📦 **REST API**: Modular, scalable endpoints for club interactions.

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/mrastatine-backend_gcube.git
cd mrastatine-backend_gcube.git
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Run the Development Server

```bash
npm run dev
```

---

## 🧪 API Endpoints

### User

| Method | Endpoint               | Description           |
|--------|------------------------|-----------------------|
| POST   | /api/v1/user/register  | Register a new user   |
| GET    | /api/v1/user/profile   | Get current user info |
| GET    | /api/v1/user/answers   | Get answers by user   |

### Answer

| Method | Endpoint                 | Description                |
|--------|--------------------------|----------------------------|
| POST   | /api/v1/answer/register  | Register answers for user  |

### Query

| Method | Endpoint                 | Description               |
|--------|--------------------------|---------------------------|
| POST   | /api/v1/query/register   | Submit a contact query    |

> 📝 All answer/user endpoints require `user-id` in request headers for authentication.

---

## 📄 Technologies Used

- Backend: [Node.js](https://nodejs.org/), [Express](https://expressjs.com/)
- Database: [MongoDB](https://www.mongodb.com/) + [Mongoose](https://mongoosejs.com/)
- File Upload: [Multer](https://github.com/expressjs/multer) + [Cloudinary](https://cloudinary.com/)
- Environment: [dotenv](https://github.com/motdotla/dotenv), [nodemon](https://nodemon.io/)
- Auth: Custom Middleware (header-based)

---

## 🧼 Code Style & Quality

- Prettified with [Prettier](https://prettier.io/)
- Uses asyncHandler for clean async error handling
- Custom ApiError and ApiResponse objects for consistency

---

## ✍️ Author

👤 Akshat Tripathi
