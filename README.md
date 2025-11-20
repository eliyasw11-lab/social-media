# Social Media Application

A full-stack social media web application built with modern web technologies.

## Project Overview

This is a complete social media platform where users can register, create profiles, share posts, interact with content, and connect with other users.

## Technology Stack

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT (JSON Web Tokens)** - Authentication and authorization
- **Bcryptjs** - Password hashing
- **Swagger** - API documentation
- **Express Validator** - Input validation

### Frontend
- **React.js** - JavaScript library for building user interfaces
- **React Router** - Routing for React applications
- **Axios** - HTTP client for API requests
- **Context API** - State management
- **CSS3** - Styling

## Features

### User Features
- User registration and authentication
- User profile creation and editing
- Profile pictures and bio
- Search for other users

### Social Features
- Create, edit, and delete posts
- Like and unlike posts
- Comment on posts
- Follow and unfollow users
- View personalized news feed

### Technical Features
- RESTful API architecture
- JWT-based authentication
- Swagger API documentation
- Responsive design
- Protected routes
- Error handling

## Project Structure

```
social-media/
├── backend/
│   ├── src/
│   │   ├── models/
│   │   ├── routes/
│   │   └── middleware/
│   ├── server.js
│   └── package.json
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── context/
│   └── package.json
└── README.md
```

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local installation or cloud instance like MongoDB Atlas)
- npm or yarn

### Backend Setup

1. Navigate to the backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file:
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/socialmedia
JWT_SECRET=your_secret_key_here
JWT_EXPIRE=7d
NODE_ENV=development
```

4. Start the backend server:
```bash
npm start
```

The API will be available at `http://localhost:5000`
Swagger documentation at `http://localhost:5000/api-docs`

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

The application will open at `http://localhost:3000`

## Deployment

### Backend Deployment

The backend can be deployed on platforms like:
- Heroku
- Render
- Railway
- AWS
- DigitalOcean

Update the `MONGODB_URI` in your deployment environment to point to your production database.

### Frontend Deployment

The frontend can be deployed on platforms like:
- Vercel
- Netlify
- GitHub Pages
- AWS S3

Update the API base URL in your frontend configuration to point to your deployed backend URL.

## API Documentation

Once the backend is running, access the Swagger API documentation at:
```
http://localhost:5000/api-docs
```

## Environment Variables

### Backend
- `PORT` - Server port
- `MONGODB_URI` - MongoDB connection string
- `JWT_SECRET` - Secret key for JWT tokens
- `JWT_EXPIRE` - JWT expiration time
- `NODE_ENV` - Environment mode

## Testing

1. Start MongoDB
2. Start the backend server
3. Start the frontend development server
4. Navigate to `http://localhost:3000`
5. Register a new account or login
6. Test all features through the UI

## License

This project is created for educational purposes.

## Contributing

This is a final project submission. For questions or issues, please refer to the documentation or contact the development team.

