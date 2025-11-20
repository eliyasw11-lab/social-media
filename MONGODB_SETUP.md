# MongoDB Setup Guide

## Option 1: MongoDB Atlas (Cloud - Recommended - Free)

### Step 1: Create MongoDB Atlas Account
1. Go to https://www.mongodb.com/cloud/atlas/register
2. Sign up for a free account
3. Verify your email

### Step 2: Create a Free Cluster
1. Click "Build a Database"
2. Choose "FREE" (M0) cluster
3. Select a cloud provider (AWS recommended) and region closest to you
4. Click "Create"

### Step 3: Create Database User
1. Go to "Database Access" (left sidebar)
2. Click "Add New Database User"
3. Authentication Method: Password
4. Username: `socialmediauser` (or any username)
5. Password: Create a strong password (save it!)
6. Database User Privileges: "Read and write to any database"
7. Click "Add User"

### Step 4: Network Access
1. Go to "Network Access" (left sidebar)
2. Click "Add IP Address"
3. Click "Allow Access from Anywhere" (or add your IP address)
4. Click "Confirm"

### Step 5: Get Connection String
1. Go to "Database" (left sidebar)
2. Click "Connect" on your cluster
3. Choose "Connect your application"
4. Driver: Node.js, Version: 4.1 or later
5. Copy the connection string (looks like: `mongodb+srv://username:password@cluster0.xxxxx.mongodb.net/?retryWrites=true&w=majority`)
6. Replace `<password>` with your database user password
7. Replace `<dbname>` with `socialmedia` or add it at the end: `...mongodb.net/socialmedia?retryWrites=true&w=majority`

### Step 6: Update .env File
Update your `backend/.env` file:
```
PORT=5000
MONGODB_URI=mongodb+srv://socialmediauser:YOUR_PASSWORD@cluster0.xxxxx.mongodb.net/socialmedia?retryWrites=true&w=majority
JWT_SECRET=your_secret_key_here
JWT_EXPIRE=7d
NODE_ENV=development
```

Replace `YOUR_PASSWORD` with your database user password and update the cluster URL.

---

## Option 2: Local MongoDB Installation

### For Windows:
1. Download MongoDB Community Server: https://www.mongodb.com/try/download/community
2. Install with default settings
3. MongoDB will run as a Windows service automatically

### Update .env File:
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/socialmedia
JWT_SECRET=your_secret_key_here
JWT_EXPIRE=7d
NODE_ENV=development
```

---

## Test Connection

After setting up, restart your backend server:
```bash
cd backend
npm start
```

You should see: "MongoDB connected" in the console.

