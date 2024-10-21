
# YouTube Clone (Capstone Project)

This is a YouTube clone project built using the **MERN stack** (MongoDB, Express.js, React, Node.js). It allows users to view, upload, and interact with videos, including features like comments, likes, and user authentication.

## Table of Contents

- [Objective](#objective)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Backend Setup](#backend-setup)
- [Frontend Setup](#frontend-setup)
- [API Endpoints](#api-endpoints)
- [Sample Data](#sample-data)
- [Contributing](#contributing)
- [License](#license)

## Objective

The project aims to help you understand how to build a full-stack real-world application using the **MERN stack**. It includes front-end and back-end components, responsive design, user authentication, and interactive video features.

## Features

### Frontend
- **Home Page**:
  - Display a YouTube-like header.
  - Static sidebar with toggle from the hamburger menu.
  - Grid of video thumbnails with title, thumbnail, channel name, and view count.
- **User Authentication**:
  - Register and login using JWT.
  - After signing in, display the user's name in the header.
  - Sign-in takes the user to a Google-like form for login and registration.
- **Search and Filter**:
  - Search bar on the homepage filters videos based on title.
  - Filter videos by category using filter buttons.
- **Video Player Page**:
  - Displays the selected video with player controls.
  - Includes like, dislike buttons, and a comment section.
  - Users can add, edit, and delete comments.
- **Channel Page**:
  - Option to create a channel after user login.
  - Display videos specific to that channel.
  - Users can edit or delete their videos.
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices.

### Backend
- **User Authentication**:
  - Sign up, login, and JWT-based authentication.
- **Video Management**:
  - API to fetch, update, and delete videos.
- **Comment Management**:
  - API to add and fetch comments.
- **Channel Management**:
  - API to create new channels and manage video uploads.

## Tech Stack

### Frontend
- **React**: JavaScript library for building UI.
- **Redux**: State management for global data handling.
- **Axios**: HTTP client for API calls.
- **React Router**: For navigation and routing.
  
### Backend
- **Node.js**: JavaScript runtime environment for building server-side applications.
- **Express.js**: Web framework for building API routes.
- **MongoDB**: NoSQL database to store users, videos, channels, and comments.
- **Multer**: Middleware for handling video uploads.
- **JWT**: For secure user authentication.

## Installation

### Prerequisites

Ensure you have the following installed:

- **Node.js**: >= 14.x
- **MongoDB**: Local instance or MongoDB Atlas.
- **npm**: Node package manager.
- **Git**: For version control.

### Backend Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/youtube-clone.git
   cd youtube-clone/backend
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the `backend` folder and add the following variables:

   ```bash
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   ```

4. Start the backend server:

   ```bash
   npm run dev
   ```

### Frontend Setup

1. Navigate to the `frontend` folder:

   ```bash
   cd ../frontend
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Start the frontend development server:

   ```bash
   npm start
   ```

4. Access the app at `http://localhost:3000`.

## API Endpoints

### User Authentication
- **POST** `/api/auth/register`: Register a new user.
- **POST** `/api/auth/login`: Login user and issue JWT token.

### Channel Management
- **POST** `/api/channels/create`: Create a new channel.
- **GET** `/api/channels/:id`: Get channel details.

### Video Management
- **POST** `/api/videos/upload`: Upload a video.
- **GET** `/api/videos`: Fetch all videos.
- **PUT** `/api/videos/:id`: Edit video details.
- **DELETE** `/api/videos/:id`: Delete a video.

### Comments
- **POST** `/api/videos/:id/comments`: Add a comment to a video.
- **GET** `/api/videos/:id/comments`: Fetch all comments for a video.

## Sample Data

Sample Video Data:

```json
[
  {
    "videoId": "video01",
    "title": "Learn React in 30 Minutes",
    "thumbnailUrl": "https://example.com/thumbnails/react30min.png",
    "description": "A quick tutorial to get started with React.",
    "channelId": "channel01",
    "uploader": "user01",
    "views": 15200,
    "likes": 1023,
    "dislikes": 45,
    "uploadDate": "2024-09-20",
    "comments": [
      {
        "commentId": "comment01",
        "userId": "user02",
        "text": "Great video! Very helpful.",
        "timestamp": "2024-09-21T08:30:00Z"
      }
    ]
  }
]
```

Sample User Data:

```json
{
  "userId": "user01",
  "username": "JohnDoe",
  "email": "john@example.com",
  "password": "hashedPassword123",
  "avatar": "https://example.com/avatar/johndoe.png",
  "channels": ["channel01"]
}
```

## Contributing

Contributions are welcome! If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
