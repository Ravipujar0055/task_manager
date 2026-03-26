# Task Manager Web App

A simple, elegant Task Manager web application with user authentication, built with Node.js, Express, MongoDB, and vanilla JavaScript.

## Features

✨ **User Authentication**
- Register new accounts
- Secure login with JWT
- Password hashing with bcryptjs

📝 **Task Management**
- Create, read, update, and delete tasks
- Set task priority (low, medium, high)
- Mark tasks as complete/pending
- Set due dates for tasks
- Add descriptions to tasks

🎨 **Modern UI**
- Clean and responsive design
- Task filtering (all, pending, completed)
- Modal for editing tasks
- Real-time task updates

## Tech Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Backend**: Node.js with Express
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Password Hashing**: bcryptjs

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

## Installation

1. **Clone or download the project**

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create a `.env` file in the root directory**
   
   Copy from `.env.example`:
   ```bash
   cp .env.example .env
   ```

4. **Configure your `.env` file**
   
   Update the following variables in `.env`:

   ```
   # MongoDB Connection String
   MONGO_URI=mongodb+srv://username:password@cluster0.mongodb.net/taskmanager?retryWrites=true&w=majority
   
   # JWT Secret (use any random string)
   JWT_SECRET=your_jwt_secret_key_here
   
   # Server Port
   PORT=5000
   
   # Environment
   NODE_ENV=development
   ```

### Getting MongoDB Connection String

#### Option 1: MongoDB Atlas (Cloud)
1. Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create a free account
3. Create a new cluster
4. Click "Connect" and select "Connect your application"
5. Choose Node.js driver
6. Copy the connection string and replace `<username>`, `<password>`, and database name

#### Option 2: Local MongoDB
If you have MongoDB installed locally:
```
MONGO_URI=mongodb://localhost:27017/taskmanager
```

## Running the Application

### Development Mode
```bash
npm start
```

The server will start on `http://localhost:5000`

### Access the Application
Open your browser and navigate to:
```
http://localhost:5000
```

## Project Structure

```
task-manager/
├── public/                 # Frontend files
│   ├── index.html         # Main HTML file
│   ├── styles.css         # CSS styles
│   └── script.js          # Frontend JavaScript
├── models/                 # Database models
│   ├── User.js            # User model
│   └── Task.js            # Task model
├── routes/                 # API routes
│   ├── auth.js            # Authentication routes
│   └── tasks.js           # Task routes
├── middleware/             # Custom middleware
│   └── auth.js            # JWT authentication middleware
├── server.js              # Express server setup
├── package.json           # Dependencies
├── .env                   # Environment variables
└── .env.example           # Environment template
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - User login

### Tasks
- `GET /api/tasks` - Get all tasks (requires auth)
- `GET /api/tasks/:id` - Get a single task (requires auth)
- `POST /api/tasks` - Create a new task (requires auth)
- `PUT /api/tasks/:id` - Update a task (requires auth)
- `DELETE /api/tasks/:id` - Delete a task (requires auth)

## Usage

1. **Register/Login**: Create an account or log in with existing credentials
2. **Add Task**: Fill in the task form with title, description, priority, and due date
3. **Manage Tasks**: 
   - Mark tasks as complete/pending using the toggle button
   - Edit tasks by clicking the edit button
   - Delete tasks using the delete button
4. **Filter Tasks**: Use filter buttons to view all, pending, or completed tasks

## Features in Detail

### Task Management
- **Priority Levels**: Low, Medium, High (color-coded)
- **Status**: Toggle between Pending and Completed
- **Due Dates**: Optional date setting for tasks
- **Descriptions**: Add detailed notes to tasks

### Security
- Passwords are hashed using bcryptjs
- JWT tokens for secure authentication
- Protected task routes require valid token

## Troubleshooting

### MongoDB Connection Error
- Verify MongoDB URI in `.env`
- Check MongoDB is running (for local setup)
- Ensure MongoDB Atlas cluster is accessible
- Check firewall/network settings

### Port Already in Use
- Change `PORT` in `.env` to a different number
- Or kill the process using port 5000

### CORS Errors
- Ensure both frontend and backend are running
- Check token is being sent in headers

## Development Notes

- Frontend data is stored in localStorage
- Tasks are filtered on the frontend for better UX
- Real-time updates on task changes
- Responsive design works on mobile devices

## Future Enhancements

- Categories/Tags for tasks
- Recurring tasks
- Task sharing between users
- Email notifications
- Dark mode
- Task search functionality

## License

ISC

## Support

For issues or questions, please check the console for error messages and ensure all environment variables are correctly set.
