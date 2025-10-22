# 📘 CipherStudio - Complete Documentation

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [Architecture](#architecture)
5. [Installation & Setup](#installation--setup)
6. [Environment Variables](#environment-variables)
7. [API Documentation](#api-documentation)
8. [Frontend Documentation](#frontend-documentation)
9. [Database Schema](#database-schema)
10. [Deployment Guide](#deployment-guide)
11. [Usage Guide](#usage-guide)
12. [Troubleshooting](#troubleshooting)

---

## Project Overview

**CipherStudio** is a modern, cloud-based code editor platform that allows users to create, edit, and preview web projects in real-time. Built with the MERN stack, it provides an integrated development environment (IDE) directly in the browser using Sandpack.

### Key Capabilities
- 🔐 Secure user authentication with JWT
- 📁 Project and file management system
- 💻 Live code editing with syntax highlighting
- 👀 Real-time preview of code changes
- 🌐 Multi-language support (JavaScript, JSX, CSS, HTML, JSON)
- 💾 Auto-save functionality
- 🎨 Modern, responsive UI

---

## Features

### User Management
- User registration with email validation
- Secure login with JWT tokens
- Password hashing with bcrypt
- Token-based authentication
- Auto-login on page refresh
- Secure logout

### Project Management
- Create unlimited projects
- Update project names
- Delete projects (cascade delete all files)
- View all user projects
- Unique project slugs with nanoid

### File System
- Create files and folders
- Hierarchical folder structure
- Update file content
- Delete files/folders (recursive)
- Duplicate name prevention
- File size tracking
- Language detection from file extension

### Code Editor
- Live code preview with Sandpack
- Syntax highlighting
- Multi-tab support
- Error display
- Auto-refresh preview
- Closable tabs
- Line numbers
- Code wrapping

---

## Tech Stack

### Frontend
```json
{
  "framework": "React 18.3.1",
  "build-tool": "Vite 6.0.5",
  "styling": "TailwindCSS 3.4.17",
  "routing": "React Router DOM 7.1.1",
  "editor": "Sandpack React 2.22.2",
  "http-client": "Axios 1.7.9",
  "notifications": "React Hot Toast 2.4.1",
  "state": "Context API"
}
```

### Backend
```json
{
  "runtime": "Node.js 18+",
  "framework": "Express 4.21.2",
  "database": "MongoDB with Mongoose 8.9.5",
  "authentication": "JWT (jsonwebtoken 9.0.2)",
  "password": "bcryptjs 2.4.3",
  "id-generation": "nanoid 5.0.9",
  "cors": "cors 2.8.5"
}
```

---

## Architecture

### System Architecture
```
┌─────────────────────────────────────────────────────────┐
│                    Frontend (Vercel)                    │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐   │
│  │  React App   │  │   Context    │  │  Components  │   │
│  │  (Vite)      │─▶│   Provider   │─▶│  & Pages     │   │
│  └──────────────┘  └──────────────┘  └──────────────┘   │
│         │                                      │        │
│         └───────────── Axios ──────────────────┘        │
└─────────────────────────────────────────────────────────┘
                            │
                            ▼ HTTPS/REST API
┌─────────────────────────────────────────────────────────┐
│                    Backend (Render)                     │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐   │
│  │   Express    │─▶│   Routes     │─▶│ Controllers  │   │
│  │   Server     │  │              │  │              │   │
│  └──────────────┘  └──────────────┘  └──────────────┘   │
│         │                  │                  │         │
│         ▼                  ▼                  ▼         │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐   │
│  │  Middleware  │  │    Models    │  │   MongoDB    │   │
│  │  (Auth/CORS) │  │  (Mongoose)  │─▶│   Database   │   │
│  └──────────────┘  └──────────────┘  └──────────────┘   │
└─────────────────────────────────────────────────────────┘
```

### Folder Structure
```
CipherStudio/
├── backend/
│   └── server/
│       ├── config/          # Database configuration
│       │   └── db.js
│       ├── controllers/     # Business logic
│       │   ├── auth.controller.js
│       │   ├── File.controller.js
│       │   └── project.controller.js
│       ├── middlewares/     # Authentication middleware
│       │   └── auth.middleware.js
│       ├── models/          # Mongoose schemas
│       │   ├── User.model.js
│       │   ├── project.model.js
│       │   └── files.model.js
│       ├── routes/          # API routes
│       │   ├── auth.routes.js
│       │   ├── project.routes.js
│       │   └── File.routes.js
│       ├── .env            # Environment variables
│       ├── .env.sample     # Environment template
│       └── app.js          # Express app entry
│
└── frontend/
    └── cipherStudio/
        ├── public/          # Static assets
        ├── src/
        │   ├── assets/      # Images, icons
        │   ├── components/  # React components
        │   │   ├── Login.jsx
        │   │   ├── Navbar.jsx
        │   │   ├── CodeEditor.jsx
        │   │   └── SandpackEditor.jsx
        │   ├── context/     # Context API
        │   │   └── AppContext.jsx
        │   ├── pages/       # Page components
        │   │   ├── Home.jsx
        │   │   ├── Editor.jsx
        │   │   └── NotFound.jsx
        │   ├── App.jsx      # Main app
        │   ├── main.jsx     # Entry point
        │   ├── App.css
        │   └── index.css
        ├── .env            # Environment variables
        └── vite.config.js  # Vite configuration
```

---

## Installation & Setup

### Prerequisites
- **Node.js** 18.x or higher
- **MongoDB** 4.4 or higher (local or Atlas)
- **Git** for version control
- **npm** or **yarn** package manager

### Step 1: Clone Repository
```bash
git clone https://github.com/kulwantolkha/cipherstudio.git
cd CipherStudio
```

### Step 2: Backend Setup

#### Install Dependencies
```bash
cd backend/server
npm install
```

#### Create Environment File
```bash
cp .env.sample .env
```

Edit `.env`:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/cipherstudio
JWT_SECRET=your_super_secret_jwt_key_minimum_32_characters_long
```

#### Start Backend Server
```bash
# Development mode with auto-reload
npm run dev

# Production mode
npm start
```

Server runs on: `http://localhost:5000`

### Step 3: Frontend Setup

#### Install Dependencies
```bash
cd ../../frontend/cipherStudio
npm install
```

#### Create Environment File
```bash
cp .env.sample .env
```

Edit `.env`:
```env
VITE_API_URL=http://localhost:5000
```

#### Start Development Server
```bash
npm run dev
```

Frontend runs on: `http://localhost:5173`

### Step 4: Verify Installation

1. **Backend Health Check**
   ```bash
   curl http://localhost:5000/test
   ```
   
   Should return:
   ```json
   {
     "success": true,
     "message": "Backend is working!",
     "cors": "enabled"
   }
   ```

2. **Frontend Access**
   - Open browser: `http://localhost:5173`
   - Should see CipherStudio homepage

3. **Database Connection**
   - Check backend terminal logs
   - Should see: `MongoDB Connected: <your-db-name>`

---

## Environment Variables

### Backend (.env)

| Variable | Description | Required | Example |
|----------|-------------|----------|---------|
| `PORT` | Server port number | ✅ | `5000` |
| `MONGODB_URI` | MongoDB connection string | ✅ | `mongodb://localhost:27017/cipherstudio` |
| `JWT_SECRET` | Secret key for JWT tokens | ✅ | `your_super_secret_key_here` |
| `FRONTEND_URL` | Allowed frontend origins | ❌ | `http://localhost:5173,https://yourdomain.com` |

**Security Notes:**
- Use a strong JWT_SECRET (minimum 32 characters)
- Never commit `.env` file to Git
- Use different secrets for development and production

### Frontend (.env)

| Variable | Description | Required | Example |
|----------|-------------|----------|---------|
| `VITE_API_URL` | Backend API base URL | ✅ | `http://localhost:5000` |

**Notes:**
- In production, set to your deployed backend URL
- No trailing slash
- Must start with `VITE_` to be accessible in code

---

## API Documentation

### Base URL
- **Development:** `http://localhost:5000`
- **Production:** `https://your-backend-url.com`

### Authentication

All authenticated routes require a JWT token in the Authorization header:
```
Authorization: Bearer <token>
```

---

### Auth Endpoints

#### 1. Register User
```http
POST /api/auth/register
```

**Request Body:**
```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com",
  "password": "password123",
  "mobile": "1234567890"
}
```

**Response (201):**
```json
{
  "success": true,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "user": {
    "_id": "60d5ec49f1b2c72b8c8e4f3a",
    "firstName": "John",
    "lastName": "Doe",
    "email": "john@example.com",
    "mobile": "1234567890"
  }
}
```

**Error Responses:**
- `400` - Missing fields or user already exists
- `500` - Server error

---

#### 2. Login User
```http
POST /api/auth/login
```

**Request Body:**
```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

**Response (200):**
```json
{
  "success": true,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "user": {
    "_id": "60d5ec49f1b2c72b8c8e4f3a",
    "firstName": "John",
    "lastName": "Doe",
    "email": "john@example.com",
    "mobile": "1234567890"
  }
}
```

**Error Responses:**
- `400` - Missing email or password
- `401` - Invalid credentials
- `500` - Server error

---

#### 3. Get Current User
```http
GET /api/auth/user
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "success": true,
  "user": {
    "_id": "60d5ec49f1b2c72b8c8e4f3a",
    "firstName": "John",
    "lastName": "Doe",
    "email": "john@example.com",
    "mobile": "1234567890"
  }
}
```

**Error Responses:**
- `401` - Not authenticated or invalid token
- `500` - Server error

---

### Project Endpoints

#### 1. Create Project
```http
POST /api/projects
Authorization: Bearer <token>
```

**Request Body:**
```json
{
  "name": "My React App"
}
```

**Response (201):**
```json
{
  "success": true,
  "project": {
    "_id": "60d5ec49f1b2c72b8c8e4f3b",
    "name": "My React App",
    "slug": "abc123xyz",
    "userId": "60d5ec49f1b2c72b8c8e4f3a",
    "createdAt": "2025-01-22T10:00:00.000Z",
    "updatedAt": "2025-01-22T10:00:00.000Z"
  }
}
```

---

#### 2. Get User Projects
```http
GET /api/projects/user/:userId
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "success": true,
  "projects": [
    {
      "_id": "60d5ec49f1b2c72b8c8e4f3b",
      "name": "My React App",
      "slug": "abc123xyz",
      "userId": "60d5ec49f1b2c72b8c8e4f3a",
      "createdAt": "2025-01-22T10:00:00.000Z",
      "updatedAt": "2025-01-22T10:00:00.000Z"
    }
  ]
}
```

---

#### 3. Get Project by ID
```http
GET /api/projects/:id
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "success": true,
  "project": {
    "_id": "60d5ec49f1b2c72b8c8e4f3b",
    "name": "My React App",
    "slug": "abc123xyz",
    "userId": "60d5ec49f1b2c72b8c8e4f3a",
    "createdAt": "2025-01-22T10:00:00.000Z",
    "updatedAt": "2025-01-22T10:00:00.000Z"
  }
}
```

---

#### 4. Update Project
```http
PUT /api/projects/:id
Authorization: Bearer <token>
```

**Request Body:**
```json
{
  "name": "Updated Project Name"
}
```

**Response (200):**
```json
{
  "success": true,
  "project": {
    "_id": "60d5ec49f1b2c72b8c8e4f3b",
    "name": "Updated Project Name",
    "slug": "abc123xyz",
    "userId": "60d5ec49f1b2c72b8c8e4f3a",
    "createdAt": "2025-01-22T10:00:00.000Z",
    "updatedAt": "2025-01-22T10:30:00.000Z"
  }
}
```

---

#### 5. Delete Project
```http
DELETE /api/projects/:id
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "success": true,
  "message": "Project deleted successfully"
}
```

---

### File Endpoints

#### 1. Create File/Folder
```http
POST /api/files
Authorization: Bearer <token>
```

**Request Body (File):**
```json
{
  "projectId": "60d5ec49f1b2c72b8c8e4f3b",
  "name": "App.jsx",
  "type": "file",
  "content": "export default function App() { return <div>Hello</div>; }",
  "language": "jsx",
  "parentId": null
}
```

**Request Body (Folder):**
```json
{
  "projectId": "60d5ec49f1b2c72b8c8e4f3b",
  "name": "components",
  "type": "folder",
  "parentId": null
}
```

**Response (201):**
```json
{
  "success": true,
  "file": {
    "_id": "60d5ec49f1b2c72b8c8e4f3c",
    "projectId": "60d5ec49f1b2c72b8c8e4f3b",
    "parentId": null,
    "name": "App.jsx",
    "type": "file",
    "content": "export default function App() { return <div>Hello</div>; }",
    "language": "jsx",
    "sizeInBytes": 52,
    "createdAt": "2025-01-22T10:00:00.000Z",
    "updatedAt": "2025-01-22T10:00:00.000Z"
  }
}
```

---

#### 2. Get Project Files
```http
GET /api/files/project/:projectId
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "success": true,
  "files": [
    {
      "_id": "60d5ec49f1b2c72b8c8e4f3c",
      "projectId": "60d5ec49f1b2c72b8c8e4f3b",
      "parentId": null,
      "name": "App.jsx",
      "type": "file",
      "content": "export default function App() { return <div>Hello</div>; }",
      "language": "jsx",
      "sizeInBytes": 52,
      "createdAt": "2025-01-22T10:00:00.000Z",
      "updatedAt": "2025-01-22T10:00:00.000Z"
    }
  ]
}
```

---

#### 3. Get Folder Contents
```http
GET /api/files/folder/:folderId
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "success": true,
  "contents": [
    {
      "_id": "60d5ec49f1b2c72b8c8e4f3d",
      "projectId": "60d5ec49f1b2c72b8c8e4f3b",
      "parentId": "60d5ec49f1b2c72b8c8e4f3c",
      "name": "Button.jsx",
      "type": "file",
      "content": "...",
      "language": "jsx",
      "sizeInBytes": 120
    }
  ]
}
```

---

#### 4. Get File by ID
```http
GET /api/files/:id
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "success": true,
  "file": {
    "_id": "60d5ec49f1b2c72b8c8e4f3c",
    "projectId": "60d5ec49f1b2c72b8c8e4f3b",
    "parentId": null,
    "name": "App.jsx",
    "type": "file",
    "content": "export default function App() { return <div>Hello</div>; }",
    "language": "jsx",
    "sizeInBytes": 52
  }
}
```

---

#### 5. Update File
```http
PUT /api/files/:id
Authorization: Bearer <token>
```

**Request Body:**
```json
{
  "content": "export default function App() { return <div>Updated!</div>; }",
  "name": "App.jsx"
}
```

**Response (200):**
```json
{
  "success": true,
  "file": {
    "_id": "60d5ec49f1b2c72b8c8e4f3c",
    "content": "export default function App() { return <div>Updated!</div>; }",
    "sizeInBytes": 58,
    "updatedAt": "2025-01-22T10:30:00.000Z"
  }
}
```

---

#### 6. Delete File/Folder
```http
DELETE /api/files/:id
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "success": true,
  "message": "file deleted successfully"
}
```

**Note:** Deleting a folder recursively deletes all its contents.

---

## Frontend Documentation

### Components

#### 1. **AppContext.jsx**
Global state management using Context API.

**Provides:**
- `user` - Current logged-in user
- `token` - JWT authentication token
- `showLogin` - Login modal visibility
- `loading` - Authentication loading state
- `login(email, password)` - Login function
- `register(...)` - Registration function
- `logout()` - Logout function
- `axios` - Configured axios instance

**Usage:**
```jsx
import { useAppContext } from '../context/AppContext';

function MyComponent() {
  const { user, login, logout } = useAppContext();
  
  if (!user) {
    return <button onClick={() => login('email', 'pass')}>Login</button>;
  }
  
  return <button onClick={logout}>Logout</button>;
}
```

---

#### 2. **Login.jsx**
Authentication modal for login and registration.

**Features:**
- Toggle between login/register
- Form validation
- Error handling with toast notifications
- Loading states

**Props:** None (uses context)

---

#### 3. **Navbar.jsx**
Top navigation bar.

**Features:**
- Logo/brand
- User info display
- Login/Logout button
- Responsive design

**Props:** None (uses context)

---

#### 4. **SandpackEditor.jsx**
Main code editor component using Sandpack.

**Features:**
- Live code preview
- Multi-file support
- Syntax highlighting
- Auto-save
- File creation/deletion
- Tab management

**Props:**
```typescript
{
  projectId: string;  // Project ID
  files: Array<File>; // File objects from API
}
```

**Usage:**
```jsx
<SandpackEditor 
  projectId="60d5ec49f1b2c72b8c8e4f3b"
  files={projectFiles}
/>
```

---

### Pages

#### 1. **Home.jsx**
Landing page showing user's projects.

**Features:**
- Project list grid
- Create new project
- Open editor
- Delete project
- Empty state

---

#### 2. **Editor.jsx**
Full-screen code editor page.

**Features:**
- Loads project by ID from URL
- Fetches project files
- Renders SandpackEditor
- Loading state
- Error handling

**Route:** `/editor/:projectId`

---

#### 3. **NotFound.jsx**
404 error page.

**Route:** `*` (catch-all)

---

### Routing

```jsx
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/editor/:projectId" element={<Editor />} />
  <Route path="*" element={<NotFound />} />
</Routes>
```

---

## Database Schema

### User Model
```javascript
{
  firstName: { type: String, required: true },
  lastName: { type: String, required: true },
  email: { 
    type: String, 
    required: true, 
    unique: true,
    lowercase: true,
    trim: true
  },
  password: { 
    type: String, 
    required: true,
    minLength: 6
  },
  mobile: { type: String },
  createdAt: { type: Date, default: Date.now },
  updatedAt: { type: Date, default: Date.now }
}
```

**Indexes:**
- `email` (unique)

---

### Project Model
```javascript
{
  name: { 
    type: String, 
    required: true,
    trim: true
  },
  slug: { 
    type: String, 
    required: true,
    unique: true
  },
  userId: { 
    type: ObjectId, 
    ref: 'User',
    required: true
  },
  createdAt: { type: Date, default: Date.now },
  updatedAt: { type: Date, default: Date.now }
}
```

**Indexes:**
- `slug` (unique)
- `userId`

---

### File Model
```javascript
{
  projectId: { 
    type: ObjectId, 
    ref: 'Project',
    required: true
  },
  parentId: { 
    type: ObjectId, 
    ref: 'File',
    default: null
  },
  name: { 
    type: String, 
    required: true,
    trim: true
  },
  type: { 
    type: String, 
    enum: ['file', 'folder'],
    required: true
  },
  content: { 
    type: String,
    default: ''
  },
  language: { 
    type: String,
    default: 'plaintext'
  },
  sizeInBytes: { 
    type: Number,
    default: 0
  },
  createdAt: { type: Date, default: Date.now },
  updatedAt: { type: Date, default: Date.now }
}
```

**Indexes:**
- `projectId`
- `parentId`
- Compound: `projectId + parentId + name` (unique)

---

## Deployment Guide

### Backend Deployment (Render)

#### Step 1: Prepare Backend
1. Ensure `.gitignore` excludes `.env` and `node_modules`
2. Commit all changes
3. Push to GitHub

#### Step 2: Create Render Service
1. Go to [Render Dashboard](https://dashboard.render.com/)
2. Click **New** → **Web Service**
3. Connect your GitHub repository
4. Configure:
   - **Name:** `cipherstudio-backend`
   - **Branch:** `main`
   - **Root Directory:** `backend/server`
   - **Build Command:** `npm install`
   - **Start Command:** `npm start`
   - **Environment:** `Node`

#### Step 3: Set Environment Variables
Add in Render dashboard:
```
PORT=5000
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/cipherstudio
JWT_SECRET=your_production_secret_key_here_minimum_32_chars
FRONTEND_URL=https://your-frontend-url.vercel.app
```

#### Step 4: Deploy
- Click **Create Web Service**
- Wait 5-10 minutes for deployment
- Note your backend URL: `https://your-app.onrender.com`

---

### Frontend Deployment (Vercel)

#### Step 1: Prepare Frontend
1. Update `.env`:
   ```env
   VITE_API_URL=https://your-backend.onrender.com
   ```
2. Commit changes
3. Push to GitHub

#### Step 2: Deploy to Vercel
1. Go to [Vercel Dashboard](https://vercel.com/dashboard)
2. Click **Add New** → **Project**
3. Import your GitHub repository
4. Configure:
   - **Framework Preset:** Vite
   - **Root Directory:** `frontend/cipherStudio`
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`

#### Step 3: Set Environment Variables
Add in Vercel:
```
VITE_API_URL=https://your-backend.onrender.com
```

#### Step 4: Deploy
- Click **Deploy**
- Wait 2-3 minutes
- Your app will be live at: `https://your-app.vercel.app`

---

### MongoDB Setup (Atlas)

1. Create account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create new cluster (free tier available)
3. Create database user
4. Whitelist IP: `0.0.0.0/0` (allow all)
5. Get connection string:
   ```
   mongodb+srv://username:password@cluster.mongodb.net/cipherstudio?retryWrites=true&w=majority
   ```
6. Add to backend environment variables

---

## Usage Guide

### For End Users

#### 1. Register Account
1. Click **Login** button
2. Click **Sign Up**
3. Enter details:
   - First Name
   - Last Name
   - Email
   - Password (min 6 characters)
4. Click **Create Account**

#### 2. Create Project
1. On homepage, click **New Project**
2. Enter project name
3. Click **Create**
4. Project created with default React files

#### 3. Edit Code
1. Click **Open Editor** on any project
2. See file list on top
3. Click file tabs to switch between files
4. Type code in left panel
5. See live preview in right panel
6. Click **Save All** to persist changes

#### 4. Add New File
1. In editor, click **+ New File**
2. Enter filename (e.g., `Button.jsx`)
3. Press Enter or click **Create**
4. File appears in tabs and file list

#### 5. Delete File
1. In file list, click **Delete** next to filename
2. Confirm deletion

#### 6. Delete Project
1. On homepage, click **Delete** on project card
2. Confirm deletion
3. All project files deleted

#### 7. Logout
1. Click your name in navbar
2. Click **Logout**
3. Redirected to homepage

---

### For Developers

#### Running Tests
```bash
# Backend
cd backend/server
npm test

# Frontend
cd frontend/cipherStudio
npm test
```

#### Linting
```bash
# Frontend
npm run lint
```

#### Building for Production
```bash
# Frontend
npm run build
# Creates optimized build in dist/
```

---

## Troubleshooting

### Common Issues

#### 1. **MongoDB Connection Failed**

**Error:**
```
MongooseServerSelectionError: connect ECONNREFUSED
```

**Solutions:**
- Check MongoDB is running: `mongod --version`
- Verify `MONGODB_URI` in `.env`
- For Atlas: check IP whitelist
- For local: start MongoDB: `mongod`

---

#### 2. **JWT Token Invalid**

**Error:**
```
401 Unauthorized - Invalid token
```

**Solutions:**
- Check `JWT_SECRET` is set
- Clear browser localStorage
- Login again
- Verify token hasn't expired (default 7 days)

---

#### 3. **CORS Error**

**Error:**
```
Access to XMLHttpRequest blocked by CORS policy
```

**Solutions:**
- Verify frontend URL in backend CORS config
- Check `VITE_API_URL` in frontend `.env`
- Restart both servers
- Clear browser cache

---

#### 4. **File Save Failed**

**Error:**
```
Failed to save files
```

**Solutions:**
- Check you're logged in
- Verify project ownership
- Check network tab for actual error
- Ensure backend is running

---

#### 5. **Sandpack Not Loading**

**Error:**
```
Preview shows blank screen
```

**Solutions:**
- Check browser console for errors
- Verify file syntax is valid
- Try refreshing preview
- Check network for CDN blocks (adblockers)

---

#### 6. **Login Loop/Logout on Refresh**

**Solutions:**
- Clear browser localStorage
- Check `VITE_API_URL` is correct
- Verify `/api/auth/user` endpoint works
- Check browser console for errors

---

### Debug Checklist

#### Backend Issues
- [ ] MongoDB connected (check logs)
- [ ] `.env` file exists with all variables
- [ ] Server running on correct port
- [ ] CORS configured for frontend URL
- [ ] Routes registered in `app.js`
- [ ] JWT_SECRET is set

#### Frontend Issues
- [ ] `.env` file has `VITE_API_URL`
- [ ] Server running (check terminal)
- [ ] Check browser console for errors
- [ ] Check Network tab for failed requests
- [ ] localStorage has token (if logged in)
- [ ] CORS errors in console

---

### Getting Help

1. **Check Logs**
   - Backend: Terminal running `npm run dev`
   - Frontend: Browser DevTools Console
   - Network: DevTools Network tab

2. **Common Log Locations**
   - Render: Dashboard → Logs tab
   - Vercel: Dashboard → Deployment → Build Logs

3. **Report Issues**
   - GitHub Issues: Include error message, steps to reproduce
   - Email: support@cipherstudio.com

---

## Security Best Practices

### Backend
- ✅ Password hashing with bcrypt (10 rounds)
- ✅ JWT tokens with expiration
- ✅ Protected routes with middleware
- ✅ Input validation
- ✅ Error handling without exposing internals
- ✅ CORS restricted to known origins

### Frontend
- ✅ XSS prevention (React escapes by default)
- ✅ Tokens in localStorage (consider httpOnly cookies for production)
- ✅ No sensitive data in client code
- ✅ HTTPS in production

### Recommendations
- Use environment-specific secrets
- Rotate JWT secrets periodically
- Implement rate limiting
- Add request logging
- Use HTTPS everywhere
- Validate all user input
- Sanitize file uploads

---

## Performance Optimization

### Backend
- Add database indexing
- Implement caching (Redis)
- Compress responses
- Optimize queries
- Use connection pooling

### Frontend
- Code splitting
- Lazy loading routes
- Optimize images
- Use production build
- CDN for static assets
- Memoize expensive operations

---

## Future Enhancements

### Planned Features
- [ ] Real-time collaboration (WebSockets)
- [ ] Code sharing via unique links
- [ ] Terminal integration
- [ ] Git integration
- [ ] Export projects as ZIP
- [ ] Theme customization
- [ ] Dark/Light mode
- [ ] Code snippets library
- [ ] Folder upload
- [ ] Search functionality
- [ ] Code formatting (Prettier)
- [ ] Multiple file upload
- [ ] Project templates
- [ ] Deployment integration

---

## Acknowledgments

- [Sandpack](https://sandpack.codesandbox.io/) - Live code editor
- [MongoDB](https://www.mongodb.com/) - Database
- [React](https://react.dev/) - UI Library
- [Express](https://expressjs.com/) - Backend framework
- [Vite](https://vitejs.dev/) - Build tool
