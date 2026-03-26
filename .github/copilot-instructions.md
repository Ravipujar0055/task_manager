# Task Manager - Development Instructions

## Project Setup Complete ✅

The Task Manager web application has been successfully scaffolded with all necessary files and dependencies installed.

## Quick Start

1. **Configure MongoDB**
   - Edit `.env` file and add your MongoDB connection string
   - For MongoDB Atlas: Get your connection string from Atlas dashboard
   - For local MongoDB: Use `mongodb://localhost:27017/taskmanager`

2. **Start the Server**
   ```bash
   npm start
   ```
   Server runs on http://localhost:5000

3. **Access the App**
   - Open browser to http://localhost:5000
   - Register a new account
   - Start creating tasks!

## Project Structure

- `server.js` - Express server entry point
- `models/` - User and Task database models
- `routes/` - Authentication and Task API routes
- `middleware/` - JWT authentication middleware
- `public/` - Frontend (HTML, CSS, JavaScript)
- `.env` - Environment configuration

## Tech Stack

- Frontend: HTML5, CSS3, Vanilla JavaScript
- Backend: Node.js + Express
- Database: MongoDB
- Authentication: JWT + bcryptjs

## Key Features

✨ User authentication (register/login)
📝 CRUD operations for tasks
🎨 Modern, responsive UI
⏱️ Task priorities and due dates
✅ Mark tasks complete/pending
🔒 Secure password hashing

## Troubleshooting

**MongoDB Connection Issue:**
- Verify MongoDB URI in `.env`
- Ensure MongoDB is running
- Check MongoDB Atlas IP whitelist

**Port 5000 Already in Use:**
- Change PORT in `.env`
- Find and kill process: `lsof -i :5000`

## Next Steps

1. Update `.env` with your MongoDB configuration
2. Run `npm start`
3. Open http://localhost:5000
4. Create an account and start managing tasks!

## Development Mode

For auto-restart on file changes, install nodemon:
```bash
npm install --save-dev nodemon
```

Then update package.json scripts:
```json
"dev": "nodemon server.js"
```

Run with: `npm run dev`

---

For detailed information, see README.md
