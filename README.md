# Instagram Mini - MERN Stack Social Media Platform

A full-stack Instagram-like social media application built with the MERN stack (MongoDB, Express.js, React, Node.js).

## Features

- User authentication (register/login)
- Create, view, like, and comment on posts
- User profiles with post grids
- Responsive design
- Image upload functionality
- Real-time post interactions

## Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT authentication
- bcryptjs for password hashing
- Multer for file uploads

### Frontend
- React 18
- React Router for navigation
- Axios for API calls
- CSS3 with responsive design

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas)
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd instagram-mini
```

2. Install backend dependencies:
```bash
npm install
```

3. Install frontend dependencies:
```bash
npm run install-client
```

4. Set up environment variables:
Create a `.env` file in the root directory with:
```env
MONGODB_URI=mongodb://localhost:27017/instagram-mini
JWT_SECRET=your-super-secret-jwt-key-here
NODE_ENV=development
PORT=5000
```

## Running the Application

### Development Mode
Run both backend and frontend concurrently:
```bash
npm run dev
```

This will start:
- Backend server on http://localhost:5000
- Frontend on http://localhost:3000

### Production Mode
1. Build the frontend:
```bash
npm run build
```

2. Start the production server:
```bash
npm start
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/user` - Get current user (protected)

### Posts
- `GET /api/posts` - Get all posts (protected)
- `POST /api/posts` - Create new post (protected)
- `GET /api/posts/:id` - Get post by ID (protected)
- `DELETE /api/posts/:id` - Delete post (protected)
- `PUT /api/posts/like/:id` - Like post (protected)
- `PUT /api/posts/unlike/:id` - Unlike post (protected)
- `POST /api/posts/comment/:id` - Comment on post (protected)
- `DELETE /api/posts/comment/:id/:comment_id` - Delete comment (protected)

### Users
- `GET /api/users` - Get all users (protected)
- `GET /api/users/:id` - Get user by ID (protected)
- `PUT /api/users/:id` - Update user profile (protected)
- `GET /api/users/profile/:username` - Get user profile by username (protected)

## Project Structure

```
instagram-mini/
├── client/                 # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── context/        # React context
│   │   ├── App.js
│   │   └── index.js
├── models/                 # MongoDB models
├── routes/                 # Express routes
├── middleware/             # Custom middleware
├── server.js              # Express server
├── package.json
└── README.md
```

## Usage

1. Register a new account or login
2. Create posts with images and captions
3. Like and comment on posts
4. View user profiles and their posts
5. Navigate through the feed

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

MIT License
